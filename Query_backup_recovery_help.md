
Microsoft Windows [Version 10.0.19045.5247]
(c) Microsoft Corporation. All rights reserved.

C:\Users\dell>mysqldump --version
mysqldump  Ver 10.13 Distrib 5.5.16, for Win64 (x86)

C:\Users\dell>code .

\\Query for backup only employee table

C:\Users\dell>mysqldump -u root -pmanager company employees > C:\Users\dell\Downloads\employee.sql

C:\Users\dell>code .



\\ Query to restore that database in case of failure

C:\Users\dell>mysql -u root -p company_backup < C:\Users\dell\Downloads\employee.sql
Enter password: *******


\\Query for backup two or more tables from particular database

C:\Users\dell>mysqldump -u root -pmanager company employees departments > C:\Users\dell\Downloads\backup05.sql



\\Query for restore that database

C:\Users\dell>mysql -u root -p company_backup < C:\Users\dell\Downloads\backup05.sql
Enter password: *******

\\ Query to backup particular whole database

C:\Users\dell>mysqldump -u root -pmanager --databases Divya company > C:\Users\dell\Downloads\full_db_backup05.sql


\\ Query to backup two database

C:\Users\dell>mysqldump -u root -pmanager --all-databases > C:\Users\dell\Downloads\two_db_backup05.sql


\\Query to backup all databases present in our databases

C:\Users\dell>mysqldump -u root -pmanager --all-databases > C:\Users\dell\Downloads\all_db_backup05.sql


\\ Query to backup whole database with all routines,procedure and functions

C:\Users\dell>mysqldump -u root -pmanager --all-databases --routines > C:\Users\dell\Downloads\with_all_routines_db_backup05.sql


\\ Query to backup all databases with structure and without any data

C:\Users\dell>mysqldump -u root -pmanager --no-data --all-databases > C:\Users\dell\Downloads\all_nodata_db_backup05.sql









\\ Number of databases and table present in my database


Enter password: *******
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 8
Server version: 5.5.16 MySQL Community Server (GPL)

Copyright (c) 2000, 2011, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| company            |
| company_backup     |
| industry           |
| mysql              |
| performance_schema |
+--------------------+
6 rows in set (0.00 sec)

mysql> use company backup;
Database changed
mysql> show tables;
+-------------------+
| Tables_in_company |
+-------------------+
| departments       |
| employees         |
+-------------------+
2 rows in set (0.00 sec)

mysql> use company_backup;
Database changed
mysql> show tables;
+--------------------------+
| Tables_in_company_backup |
+--------------------------+
| employees                |
+--------------------------+
1 row in set (0.00 sec)


mysql> select * from employees;
+------------+-------------+--------------+----------+
| EmployeeID | Name        | DepartmentID | Salary   |
+------------+-------------+--------------+----------+
|          1 | John Doe    |          101 | 50000.00 |
|          2 | Jane Smith  |          102 | 60000.00 |
|          3 | Alice Jones |         NULL | 70000.00 |
|          4 | Bob Brown   |          103 | 55000.00 |
+------------+-------------+--------------+----------+
4 rows in set (0.00 sec)

mysql> use company_backup;
Database changed
mysql> show tables;
+--------------------------+
| Tables_in_company_backup |
+--------------------------+
| departments              |
| employees                |
+--------------------------+
2 rows in set (0.00 sec)

mysql> create database divya;
Query OK, 1 row affected (0.00 sec)

mysql> create table student(roll int(15),name varchar(20));
Query OK, 0 rows affected (0.01 sec)

mysql> insert into student values(01,"aaa");
Query OK, 1 row affected (0.00 sec)

mysql> insert into student values(02,"bbb");
Query OK, 1 row affected (0.00 sec)

mysql> insert into student values(03,"ccc");
Query OK, 1 row affected (0.00 sec)

mysql> insert into student values(04,"ddd");
Query OK, 1 row affected (0.00 sec)

mysql> insert into student values(05,"eee");
Query OK, 1 row affected (0.00 sec)

mysql> select * from student;
+------+------+
| roll | name |
+------+------+
|    1 | aaa  |
|    2 | bbb  |
|    3 | ccc  |
|    4 | ddd  |
|    5 | eee  |
+------+------+
5 rows in set (0.00 sec)

mysql>
