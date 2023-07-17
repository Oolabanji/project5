## Implementing a Client Server Architecture Using MySQL server and MYSQL client

![EC2ubuntu](https://github.com/Oolabanji/test_/assets/136812420/67daaf09-964e-4a3d-a8ce-fda3283901df)
To demonstrate Client-Server architecture, I will be using two Ec2 instance with mysql-server and mysql-client respectively.


![EC2ubuntu2](https://github.com/Oolabanji/test_/assets/136812420/a2b38d6a-8868-4753-ba19-77ac03bc1901)

I created and configure two Linux-based virtual servers (EC2 instances in AWS).

On mysql server Linux Server, I installed MySQL Server software.
![mysqlserverinstallation](https://github.com/Oolabanji/test_/assets/136812420/3ecb5800-a239-4898-bbe7-568201d33de6)



![mysqlserverstatus](https://github.com/Oolabanji/test_/assets/136812420/cbb5f077-8a2c-49c4-91d1-e70a8b078a48)

On mysql client Linux Server, I  installed MySQL Client software.
![sqlclientinstallation](https://github.com/Oolabanji/test_/assets/136812420/51e9f14b-41a9-4309-b57e-ff1d9a55bca2)

I opened port 3306 on Mysql-server allow for connection. Both server can communicate using private IPs since they belong to the same subnet
![ec2port](https://github.com/Oolabanji/test_/assets/136812420/f22cac7c-6317-4239-a921-a0a21a626f10)

I changed bind-address on Mysql-server to allow for connection from any IP address. Set the bind-address to 0.0.0.0 using the command below:

'sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf'
![bindaddress](https://github.com/Oolabanji/test_/assets/136812420/9b014e99-896f-46d6-9721-caab21383539)
I configured MysQL server and create database and user

I set up password with sudo mysql_secure_installation and create a user

I created database
![showdatabase](https://github.com/Oolabanji/test_/assets/136812420/3b2e5d9e-159c-401c-8f15-90bbcc8811e3)
I granted all permission on database
![grantpriv](https://github.com/Oolabanji/test_/assets/136812420/ce0745f9-9d5f-4e7d-ab70-9aa5fde304bd)
From my mysql client Linux Server, I connected remotely to mysql server Database Engine using mysql utility.

![fromsqlclient](https://github.com/Oolabanji/test_/assets/136812420/e187c293-b8ca-4aa1-baae-63526aa57734)



