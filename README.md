# DATABASE-BACKUP-AND-RECOVERY

1) COMPANY : CODTECH IT SOLUTIONS
2) NAME : DIVYA RAJENDRA LOKHANDE
3) INTERN ID : CT08NRV
4) DOMAIN : SQL
5) DURATION : 4 WEEKS
6) MENTOR : NEELA SANTOSH

*** Description *** 

       This project demonstrates the process of database backup and recovery using MySQL (XAMPP). Backup and recovery are crucial to prevent data loss due to unexpected failures, corruption, or accidental deletions. The provided scripts and documentation explain how to take a backup of a MySQL database and restore it when needed. 

*** Objectives *** 

 1) Create a backup of a MySQL database.
 2) Restore the database from the backup in case of failure.

 *** Technologies Used ***

1) Database: MySQL (XAMPP)
2) Tools: Command Line, phpMyAdmin
3) Backup Method: mysqldump command
4) Recovery Method: mysql command

 *** Files Included ***

 1) backup.sql - SQL dump file containing the database backup.
 2) restore.sql - SQL file to restore the database from the backup.


 *** Backup using phpMyAdmin (Graphical Interface) ***

Step-by-Step Guide
1️⃣ Open XAMPP Control Panel
   Start Apache and MySQL services.

2️⃣ Access phpMyAdmin
   Open a web browser and go to:
     
        http://localhost/phpmyadmin/
        This will open phpMyAdmin.
        
3️⃣ Select the Database
   On the left panel, click on the database you want to back up.

4️⃣ Go to Export Tab
   Click on the Export tab from the top menu.

5️⃣ Choose Export Method
    Select Quick for a simple backup.
    Select Custom if you want to include/exclude specific tables.

6️⃣ Select Export Format
    Choose SQL (default format).

7️⃣ Download Backup
   Click Go, and the .sql file will be downloaded to your system.
   This file contains all the database structure and data.

*** Backup using Command Line (mysqldump) ***

1️⃣ Open Command Prompt (CMD) or Terminal
    Press Win + R, type cmd, and press Enter.
    Or go to the XAMPP folder and open shell.

2️⃣ Navigate to MySQL Bin Folder
    cd C:\xampp\mysql\bin

3️⃣ Run mysqldump Command
    mysqldump -u root -p database_name > C:\backup\database_backup.sql

   1) Replace database_name with your actual database name.
   2) You will be asked to enter the MySQL password (leave it empty if no password 
      is set).
      
4️⃣ Backup File Created

   1) The backup file database_backup.sql will be saved in C:\backup\.
   2) You can change the file path as per your requirement.

*** Tools Used ***
e.g., XAMPP MySQL, Command Line, phpMyAdmin

*** Commands Used ***
mysqldump




