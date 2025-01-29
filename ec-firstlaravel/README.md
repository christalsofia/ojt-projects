# **First Laravel Project**

## **Overview**
This is a simple Laravel project created using the Laravel Installer, Breeze for authentication scaffolding, and Blade for the view engine. This project demonstrates basic features such as user authentication and registration.

## **Features**
- User authentication (login, register)
- Blade templating engine for views
- Breeze UI for authentication
- Responsive design

## **Technologies Used**
- **Backend:** Laravel
- **Frontend:** Blade, TailwindCSS, AlpineJS (via Breeze)
- **Database:** MySQL (via XAMPP)
- **Development Tools:** Composer, npm, Vite (for front-end asset management)

## **Local Setup**

### **1. Install XAMPP**
Before setting up the Laravel project, make sure you have **XAMPP** installed to run Apache and MySQL:
1. Download XAMPP from [Apache Friends](https://www.apachefriends.org/index.html).
2. Install XAMPP and run **Apache** and **MySQL** from the XAMPP Control Panel.


### **2. Create Database in phpMyAdmin**
1. Open your browser and go to [http://localhost/phpmyadmin](http://localhost/phpmyadmin).
2. Log in using the default MySQL username (`root`) and leave the password field empty (if no password is set).
3. Click on **Databases** in the top menu.
4. Create a new database (e.g., `your_database_name`).
5. Once created, note the database name for later use in the `.env` file.

### **3. Clone the Repository**
You can clone the full repository or use **sparse checkout** to get only this project:

#### **Full Clone**

```
git clone https://github.com/christalsofia/ojt-projects.git
cd ojt-projects/ec-firstlaravel
```

#### **Sparse Checkout (Only This Folder)**

```
git clone --no-checkout https://github.com/christalsofia/ojt-projects.git
cd ojt-projects
git sparse-checkout init --cone
git sparse-checkout set ec-firstlaravel
git checkout
cd ec-firstlaravel
```

### **4. Install Dependencies**
Run the following commands to install PHP and JavaScript dependencies:

```
composer install
npm install
```

### **5. Set Up Environment**
1. Duplicate the example environment file:

    ```
    cp .env.example .env
    ```

2. Update the `.env` file with your **XAMPP MySQL** database credentials. Replace `your_database_name` with the name of the database you created in **phpMyAdmin**. If your MySQL user has no password, leave `DB_PASSWORD` empty.

    ```
    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=your_database_name
    DB_USERNAME=root
    DB_PASSWORD=
    ```

### **6. Run Migrations**
Run this command to create database tables:

```
php artisan migrate
```


### **7. Start Local Servers**
1. Ensure **Apache** and **MySQL** are running via XAMPP Control Panel.
2. Start Laravel's development server:

    ```
    php artisan serve
    ```

3. Start Vite for live asset building and hot reloading:

    ```
    npm run dev
    ```

### **8. Access the Application**
Open your browser and visit the application:

```
http://localhost:8000
```

## **Notes**
- You can modify `.env` to change the database connection settings.
