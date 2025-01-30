# First Laravel App

## Overview
This is a simple Laravel project created using the Laravel Installer, Breeze for authentication scaffolding, and Blade for the view engine. This project demonstrates basic features such as user authentication and registration.

## Prerequisite(s)

- [Composer](https://getcomposer.org/download/)
- [PHP](https://www.php.net/downloads.php)
- [node.js](https://nodejs.org/en/download)
- [XAMPP](https://www.apachefriends.org/download.html)

## Local Setup

### 1. Create Database in phpMyAdmin
1. Run Apache and MySQL via XAMPP Control Panel.
2. Open your browser and go to [http://localhost/phpmyadmin](http://localhost/phpmyadmin).
3. Log in using the default MySQL username (`root`) and leave the password field empty (if no password is set).
4. Click on **Databases** in the top menu.
5. Create a new database (e.g., `your_database_name`).
6. Once created, note the database name for later use in the `.env` file.

### 2. Clone the Repository
You can clone the full repository or use sparse checkout to get only this project:

#### Full Clone

```
git clone https://github.com/christalsofia/ojt-projects.git
cd ojt-projects/ec-firstLaravelApp
```

#### Sparse Checkout (Only This Folder)

```
git clone --no-checkout https://github.com/christalsofia/ojt-projects.git
cd ojt-projects
git sparse-checkout init --cone
git sparse-checkout set ec-firstLaravelApp
git checkout
cd ec-firstLaravelApp
```

### 3. Install Dependencies
Run the following commands to install PHP and JavaScript dependencies:

```
composer install
npm install
```

### 4. Set Up Environment
1. Duplicate the example environment file:

    ```
    cp .env.example .env
    ```

2. Run the following command to generate an `APP_KEY`:

    ```
    php artisan key:generate
    ```

3. Clear the config cache to ensure the new key is properly loaded:

    ```
    php artisan config:clear
    ```

4. Update the `.env` file with your XAMPP MySQL database credentials. Replace `your_database_name` with the name of the database you created in phpMyAdmin. If your MySQL user has no password, leave `DB_PASSWORD` empty.

    ```
    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=your_database_name
    DB_USERNAME=root
    DB_PASSWORD=
    ```

### 5. Run Migrations
Run this command to create database tables:

```
php artisan migrate
```


### 6. Start Local Servers
1. Ensure Apache and MySQL are running via XAMPP Control Panel.
2. Start Laravel's development server:

    ```
    php artisan serve
    ```

3. Start Vite for live asset building and hot reloading:

    ```
    npm run dev
    ```

### 7. Access the Application
Open your browser and visit the application:

```
http://localhost:8000
```
