Guide
The goal of ShopKit POS is to give an easy way to Inventory and Stock Management.

#Technologies Used
This system uses multiple technologies to give the best possible experience.

PHP with Laravel Framework
MySQL 5.6+
PHP 7.4+
Javascript
React
#Installation Guide
We tried our best to make the installation of the system as easy as possible. System Requirements It is assumed that you have primary knowledge Laravel installation knowledge since this application is built on Laravel.

#System Requirement
It is assumed that you have primary knowledge Laravel and JS application installation knowledge since this application is built on Laravel with JS.

You can read about laravel Requirements here(opens new window)

You need update below variables in php.ini file if you want to send bigger files (Optional).

upload_max_filesize = 50M

max_file_uploads = 50

post_max_size = 100M

#Setup ShopKit POS System
If you have purchased the ShopKit POS system then you will be able to find the zip named dist.zip

Now if you want to setup ShopKit POS on your server then you can directly copy the dist.zip folder to your web root directory on server and the following steps:

#1. Copy files to web server
Upload shopkit.zip to your web server's root (public_html) and extract it there.

#2. Setup Default DB
Open PHPMyAdmin on your server and do a login.
Setup Default DB

Click on the Databases tab.

Create a new database and specify a Database name of your choice and Click Create button.


Now on the left, select the database (pos) DB available in Database folder  OR the one that you have created.
Click Import in the top menu
Under Import, choose the default sql file from dist/database/pos.sql and click button Go.
#3. Setup environment .env file
Open .env file from your server's root folder.

You need to change the following information into your environment (.env) file.

- APP_NAME - Name of your Application/Library System
- APP_URL - Change this URL with your server URL (including trailing path if you are putting it in sub folder or root website)
- DB_HOST - Put your database hostname here
- DB_PORT - Put your database port here if it does not default to 3306
- DB_DATABASE - Change it to your database name
- DB_USERNAME - Name of your database user
- DB_PASSWORD - Password of your database user
You will also need to set up mail configuration, you can read more about here for that setup based on mail service that you use.

- MAIL_MAILER
- MAIL_HOST
- MAIL_PORT
- MAIL_USERNAME
- MAIL_PASSWORD
- MAIL_ENCRYPTION
- MAIL_FROM_ADDRESS 
- MAIL_FROM_NAME
If you want to store your files to direct your s3 bucket then you have to use following .env variables. You need to change FILESYSTEM_DRIVER and MEDIA_DISK value to s3 when you are using AWS file storage.

- AWS_ACCESS_KEY_ID=
- AWS_SECRET_ACCESS_KEY=
- AWS_DEFAULT_REGION=us-east-1
- AWS_BUCKET=
- AWS_ENDPOINT=
- AWS_URL=
Or you can use your choice of storage driver to store your media assets if you want. All of your attachments will be placed into that.

And you should be ready to go.

#4. Admin login
You can login as admin using below credentials.

Admin Credentials: Email / Password : admin@infy-pos.com / 123456
