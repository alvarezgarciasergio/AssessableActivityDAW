# AssessableActivityDAW
1- Crate the instance
2- Configure the elastic IP
3- Acces the instance
   ssh -i labsuser.pem ubuntu@ec2-44-196-21-18.compute-1.amazonaws.com
4- Update the list available package sources and ther versions.
   sudo apt-get update
5- Installs the Apache2 web server on the system.
   sudo apt-get install apache2
6- Installs MySQL server, PHP, Apache PHP module, and PHP-MySQL extension.
   sudo apt-get install mysql-server php libapache2-mod-php php-mysql 
7- Configured the database so it doesn't ask us for a username or password:
   Starts the MySQL service on the syste
   sudo service mysql start
   Launches the MySQL command-line client as the root user
   sudo mysql
   mysql> USE mysql
   mysql> UPDATE user SET plugin='mysql_native_password' WHERE User='root';
   mysql>FLUSH PRIVILEGES;
   mysql>exit
8- Restarts the MySQL service on the system.
   sudo service mysql restart
9- Installs the Firefox web browser on the system
   sudo apt-get install firefox 
10- Downloads the file from the given URL
    wget -U "Firefox" "https://phpgurukul.com/?sdm_process_download=1&download_id=7210" -O file.zip
11- Installs the 'unzip' utility on the system.
    sudo apt install unzip
12- Extracts the contents of the file 'file.zip' 
    unzip file.zip
13- We access the downloaded folder and move the 'hostel' folder to /var/www/html/.
    sudo mv hostel/ /var/www/html
14- We change the permissions for user www-data.
    sudo chown -R www-data /var/www/html/hostel/
15- Database creation:
    sudo mysql
    Mysql> CREATE DATABASE hostel;
    MYsql> USE hostel;
    source /var/Hostel management System Project/SQL File/hostel.sql
    exit
16- Access to the folder “sites-avilable”
    cd /etc/apache2/sites-available/
17- Copy and rename the file 000-default.conf.
    sudo cp 000-default.conf 001-burukul.conf
18- Move to the folder “sites-enabled”
    cd ../sites-enabled/
19- Disable the default file.
    sudo a2dissite 000-default.conf
20- Enable the one we have created
    sudo a2ensite 001-burukul.conf
21- Modify the file 001-burukul.conf
    sudo nano 001-burukul.conf
   Set our elastic IP as the ServerName and modify the DocumentRoot.
22- Restarts the Apache2 web server service
    sudo service apache2 restart
23- We access the browser with our elastic IP and we can already access.
