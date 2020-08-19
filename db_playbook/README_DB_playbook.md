
<h2>Steps : </h2>

$ sudo apt-get update

$ sudo apt-get install mysql-server

$ sudo mysql_secure_installation utility

$ sudo ufw allow mysql

$ sudo systemctl start mysql

$ sudo systemctl enable mysql

$ vi /etc/mysql/mysql.conf.d/mysqld.cnf: bind-address = 0.0.0.0 ( All ip addresses. )

$ sudo systemctl restart mysql

$ sudo /usr/bin/mysql -u root -p

mysql> CREATE USER 'demo'@'localhost' IDENTIFIED BY 'Password@1';

mysql> GRANT ALL PRIVILEGES ON *.* TO 'demo'@'localhost' WITH GRANT OPTION;

mysql> CREATE USER 'demo'@'ip' IDENTIFIED BY 'Password@1';

mysql> GRANT ALL PRIVILEGES ON *.* TO 'demo'@'ip'  WITH GRANT OPTION;

 
 FLUSH PRIVILEGES;
 
 CREATE DATABASE db_name;
 
 create table demousers(
 id INT NOT NULL AUTO_INCREMENT,
 name VARCHAR(50) NOT NULL,
 mobile VARCHAR(20) NOT NULL,
 password VARCHAR(30) NOT NULL,
 introduction VARCHAR(100) NOT NULL,
 email VARCHAR(40) NOT NULL,
 PRIMARY KEY ( id )
 );
