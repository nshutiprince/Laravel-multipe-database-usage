## Using Multiple Databases in Laravel 8

Laravel 8 has many options to use different types of databases. For example, we can use SQLite, MYSQL, PostgreSQL, SQL Server, Laravel-OCI8 for Oracle Database. Sometimes, to Speed Up Our Application or Simplify Our Large-Database Application we needs to use Multiple Database for our Single Laravel Application.

## Step 1 – Create Configuration For Database in Laravel 8

Here we will create the config for MYSQL Database. You need to open the database.php file in config directory. Inside the connections array there is a mysql key by default for first database. You just need to create one more key mysql2 for second database and paste the code given below.

## Step 2 – Set Environment Variables in Laravel 8

Open .env file and set the database credentials as given below in code. Remember, DB_HOST2, DB_PORT2, DB_DATABASE2, DB_USERNAME2, DB_PASSWORD2 is for second database.

## Step 3 – Create Eloquent Model in Laravel 8

Before creating the models we will create two sample database tables.

In Database(laraveldb1) Create a table(Customers) with fields – id, customer_name, customer_email, created_at, updated_at, deleted_at.

In Database(laraveldb2) Create a table(Staff) with fields – id, staff_name, staff_email, created_at, updated_at, deleted_at.

Inside app\Models directory create a File Customer.php

Again inside app\Models directory create a File Staff.php

## Step 4 – Create Controllers in Laravel 8

First, inside the app\Http\Controllers directory create a file CustomerController.php , In create method we have used the Customer Model to insert data in customers table.

Now, inside the app\Http\Controllers directory create a file StaffController.php , Same, In create method we have used the Staff Model to insert data in staff table. You can also read about database queries using Eloquent Model(https://laravel.com/docs/8.x/eloquent#inserting-and-updating-models).

## Step 5 – Create Resource Route in Laravel 8

Inside the routes directory open api.php file ,

## Note

You can now use Multiple Databases in your any Laravel Applications. You can also now speed up and simplify your Laravel Application using Laravel 8 Multiple Database and Resource Routes with Controllers.


## Tags

php , laravel , mysql , database