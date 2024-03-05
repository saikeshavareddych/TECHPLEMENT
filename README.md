### Deploy application in monolithic and microservices architecture.

For monolithic : 1 EC2 instance, deploy wordpress and MYSQL on the same instances.
For microservices: 2 EC2 instances, 1 for wordpress and 1 for MYSQL.

# MONOLOTHIC ARCHITECTURE

**Install Apache server on Ubuntu**

`sudo apt install apache2`

**Install php runtime and php mysql connector**

`sudo apt install php libapache2-mod-php php-mysql`

**Install MySQL server**

`sudo apt install mysql-server` 

**Login to MySQL server**

`sudo mysql -u root`

**Change authentication plugin to mysql_native_password (change the password to something strong)**

`ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password by 'password';`

**Create a new database user for wordpress**

`CREATE USER 'username'@localhost IDENTIFIED BY 'password';`

**Create a database for wordpress**

`CREATE DATABASE name;`

**Grant all privilges on the database 'wp' to the newly created user**

`GRANT ALL PRIVILEGES ON databasename.* TO 'username'@localhost;`

**Download wordpress**

wget [https://wordpress.org/latest.tar.gz](url)

**Unzip**

`tar -xvf latest.tar.gz`

**Move wordpress folder to apache document root**

`sudo mv wordpress/ /var/www/html`

**Command to restart/reload apache server**

`sudo systemctl restart apache2`

`sudo systemctl reload apache2`

## OUTPUT

![Screenshot (39)](https://github.com/saikeshavareddych/TECHPLEMENT/assets/147091730/bcde21e8-bd69-4a98-a356-cfd582b8683d)



# MICROSERVICE ARCHITECTURE 

## SQL in One Instance

**Install MySQL Server**

`sudo apt install mysql-server` 

**Login to MySQL server**

`sudo mysql -u root`

**Change authentication plugin to mysql_native_password (change the password to something strong)**

`ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password by 'password';`

**Create a new database user for wordpress**

`CREATE USER 'username'@localhost IDENTIFIED BY 'password';`

**Create a database for wordpress**

`CREATE DATABASE name;`

**Grant all privilges on the database 'wp' to the newly created user**

`GRANT ALL PRIVILEGES ON databasename.* TO 'username'@localhost;`

## WORDPRESS in Another Instance

**Install Apache server**

`sudo apt install apache2`

**Install php runtime and php mysql connector**

`sudo apt install php libapache2-mod-php php-mysql`

**Download wordpress**

`cd /tmp
wget https://wordpress.org/latest.tar.gz`

**Unzip**

`tar -xvf latest.tar.gz`

**Move wordpress folder to apache document root**

`sudo mv wordpress/ /var/www/html`

**Command to restart/reload apache server**

`sudo systemctl restart apache2`

`sudo systemctl reload apache2`

## OUTPUT


![image](https://github.com/saikeshavareddych/TECHPLEMENT/assets/147091730/f15520fd-31f8-4b29-b6ec-78a245d1bd76)
