# AssessableActivityDAW  
## Description of the installation of the Apache HTTP Server, PHP and MySQL Server on the latest Ubuntu Server version.   
The first thing we need to do is update the list of available packages with --sudo apt-get update--.  
It's important to run it before installing new packages to ensure that you are getting the most up-to-date information about available packages.  
Next, you have to install Apache 2 with --sudo apt-get install apache2--. Once Apache is installed, it can respond to incoming web requests and serve web pages.  
To finish, run --sudo apt-get install mysql-server php libapache2-mod-php php-mysql--. This command installs MySQL, PHP, and the necessary extensions for PHP to work with Apache.  
The 'php-mysql' extension allows PHP to interact with MySQL databases.
With these three commands, we will have set up a web server environment with Apache, a database with MySQL, and the ability to run dynamic web applications with PHP on our Ubuntu server.

