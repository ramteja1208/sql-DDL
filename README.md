# sql-DDL
Microsoft Windows [Version 10.0.22621.1992]
(c) Microsoft Corporation. All rights reserved.

C:\Users\KUDUPUDI RAMTEJA>cd..

C:\Users>cd..

C:\>cd msql
The system cannot find the path specified.

C:\>mysql.exe -u root
'mysql.exe' is not recognized as an internal or external command,
operable program or batch file.

C:\>mysql -u root -p
'mysql' is not recognized as an internal or external command,
operable program or batch file.

C:\>cd xampp

C:\xampp>cd mysql

C:\xampp\mysql>cd bin

C:\xampp\mysql\bin>msql.exe -u root
'msql.exe' is not recognized as an internal or external command,
operable program or batch file.

C:\xampp\mysql\bin> mysql -u root -p
Enter password:
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 8
Server version: 10.4.24-MariaDB mariadb.org binary distribution

Copyright (c) 2000, 2018, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MariaDB [(none)]> create database customer;
Query OK, 1 row affected (0.001 sec)

MariaDB [(none)]> show databases;
+--------------------+
| Database           |
+--------------------+
| collage            |
| collage1           |
| customer           |
| information_schema |
| mysql              |
| performance_schema |
| phpmyadmin         |
| test               |
| univ               |
+--------------------+
9 rows in set (0.004 sec)

MariaDB [(none)]> use customer;
Database changed
MariaDB [customer]> create table user(id int,name,password,);
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near 'password,)' at line 1
MariaDB [customer]> create table user(id int,name,password,)
    -> desc customer;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near 'password,)
desc customer' at line 1
MariaDB [customer]> desc user;
ERROR 1146 (42S02): Table 'customer.user' doesn't exist
MariaDB [customer]> create table user(id int,name,password)
    -> desc user;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near 'password)
desc user' at line 1
MariaDB [customer]> desc user;
ERROR 1146 (42S02): Table 'customer.user' doesn't exist
MariaDB [customer]> create table user(id int,name,password)
    -> create table user(id int,name,password);
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near 'password)
create table user(id int,name,password)' at line 1
MariaDB [customer]> create table user(id int(10),name varchar(100),password int(6));
Query OK, 0 rows affected (0.016 sec)

MariaDB [customer]> desc user;
+----------+--------------+------+-----+---------+-------+
| Field    | Type         | Null | Key | Default | Extra |
+----------+--------------+------+-----+---------+-------+
| id       | int(10)      | YES  |     | NULL    |       |
| name     | varchar(100) | YES  |     | NULL    |       |
| password | int(6)       | YES  |     | NULL    |       |
+----------+--------------+------+-----+---------+-------+
3 rows in set (0.012 sec)

MariaDB [customer]> alter table user add column age int(10);
Query OK, 0 rows affected (0.015 sec)
Records: 0  Duplicates: 0  Warnings: 0

MariaDB [customer]> desc user;
+----------+--------------+------+-----+---------+-------+
| Field    | Type         | Null | Key | Default | Extra |
+----------+--------------+------+-----+---------+-------+
| id       | int(10)      | YES  |     | NULL    |       |
| name     | varchar(100) | YES  |     | NULL    |       |
| password | int(6)       | YES  |     | NULL    |       |
| age      | int(10)      | YES  |     | NULL    |       |
+----------+--------------+------+-----+---------+-------+
4 rows in set (0.010 sec)

MariaDB [customer]> alter table user drop column age ;
Query OK, 0 rows affected (0.013 sec)
Records: 0  Duplicates: 0  Warnings: 0

MariaDB [customer]> desc user;
+----------+--------------+------+-----+---------+-------+
| Field    | Type         | Null | Key | Default | Extra |
+----------+--------------+------+-----+---------+-------+
| id       | int(10)      | YES  |     | NULL    |       |
| name     | varchar(100) | YES  |     | NULL    |       |
| password | int(6)       | YES  |     | NULL    |       |
+----------+--------------+------+-----+---------+-------+
3 rows in set (0.008 sec)

MariaDB [customer]>
