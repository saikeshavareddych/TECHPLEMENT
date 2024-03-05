### Deploy application in monolithic and microservices architecture.

For monolithic : 1 EC2 instance, deploy wordpress and MYSQL on the same instances.
For microservices: 2 EC2 instances, 1 for wordpress and 1 for MYSQL.
Configure the necessary security group for the instances.

# MONOLOTHIC ARCHITECTURE

Install Apache server on Ubuntu

Install php runtime and php mysql connector

Install MySQL server

Login to MySQL server

Change authentication plugin to mysql_native_password (change the password to something strong)

Create a new database user for wordpress

Create a database for wordpress

Grant all privilges on the database 'wp' to the newly created user

Download wordpress

Unzip

Move wordpress folder to apache document root

Command to restart/reload apache server

# MICROSERVICE ARCHITECTURE 

## SQL in One Instance

Install MySQL Server

Login to MySQL server

Change authentication plugin to mysql_native_password (change the password to something strong)

Create a new database user for wordpress

Create a database for wordpress

Grant all privilges on the database 'wp' to the newly created user

## WORDPRESS in Another Instance

Install Apache server

Install php runtime and php mysql connector

Download wordpress

Unzip

Move wordpress folder to apache document root

Command to restart/reload apache server
