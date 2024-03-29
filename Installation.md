==============================================
# Installing MYSQL in Ubuntu 20.04
==============================================
````
#!/bin/bash
sleep 60
sudo apt update -y
sudo apt install mysql-server -y
sudo systemctl start mysql.service
mysql --version
````
-------------
# Connecting Database Server from Bastion Server
-------------
# Login to your Bastion Server
# (Copy the pem key in Bastion Server '/home/ubuntu' location)
````
sudo ssh –i ‘Keyname.pem’ ubuntu@<database-Private-IP>
````
# (Now we will enter inside your Database Server)

==============================================
# Installing MYSQL in Amazon Linux 2023
==============================================
````
#!/bin/bash
sleep 60
sudo wget https://dev.mysql.com/get/mysql80-community-release-el9-1.noarch.rpm
sudo yum install mysql80-community-release-el9-1.noarch.rpm -y
yum repolist enabled | grep "mysql.*-community.*"
sudo yum install mysql-community-server -y
sudo systemctl start mysqld
mysql --version
````
-------------
# Connecting Database Server from Bastion Server
-------------
# Login to your Bastion Server
# (Copy the pem key in Bastion Server '/home/ec2-user' location)
````
sudo ssh –i ‘Keyname.pem’ ec2-user@<database-Private-IP>
````
# (Now we will enter inside your Database Server)

==============================================
# Installing MYSQL in Amazon Linux 2
==============================================
````
#!/bin/bash
sleep 60
sudo amazon-linux-extras install epel -ysudo yum install mysql80-community-release-el9-1.noarch.rpm -y
sudo yum install https://dev.mysql.com/get/mysql80-community-release-el7-5.noarch.rpm
sudo yum install mysql-community-server 
systemctl active mysqld 
systemctl start mysqld 
systemctl status mysqld 
cat /var/log/mysql.log | grep "A temporary password" 
sudo mysql_secure_installation
````
# Set root password
````
mysql -u root -p 
mysql --version
````
-------------
# Connecting Database Server from Bastion Server
-------------
# Login to your Bastion Server
# (Copy the pem key in Bastion Server '/home/ec2-user' location)
````
sudo ssh –i ‘Keyname.pem’ ec2-user@<database-Private-IP>
````
# (Now we will enter inside your Database Server)
