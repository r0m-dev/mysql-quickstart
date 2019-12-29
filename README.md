# MySQL Quick start

## Connection with Linux
```bash
mysql -u root -p
```

## Create database with dedicated user
```mysql
mysql> create database YOUR_DATABASE_NAME;
mysql> CREATE USER 'ME'@'localhost' IDENTIFIED BY 'Pa$$w0rd';
mysql> GRANT ALL PRIVILEGES ON YOUR_DATABASE_NAME.* TO 'ME'@'localhost';
mysql> flush privileges;
mysql> exit;
```

## List all users
```mysql
mysql> SELECT User,Host FROM mysql.user;
```

## List grant for MySQL user
```mysql
SHOW GRANTS FOR 'ME'@'localhost';
```

## Revoke all grants for MySQL user
```mysql
REVOKE ALL PRIVILEGES, GRANT OPTION FROM 'ME'@'localhost';
```

## Delete MySQL user from the user table
```mysql
DROP USER 'ME'@'localhost';
```
## Drop database
```mysql
DROP DATABASE YOUR_DATABASE_NAME;
```

## Connect MySQL root account with normal user
Connect with sudo
```bash
sudo mysql -u root -p
```
Alter root user
```mysql
mysql> ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'MY_PASS';
```
