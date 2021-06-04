# ORACLE-DEVELOPER-FIX
How to fix 'ORA-12705: Cannot access NLS data files or invalid environment specified'


If you are using SQL Developer you have to follow this steps:

   1 Open SQL Developer package content. Go to Applications, right click on SQL Developer and select "Show Package Contents".
   2 Go to Contents/Resources/sqldeveloper/sqldeveloper/bin/
   3 Open sqldeveloper.conf using a text editor.
   4 Add the following lines:

            # Options to avoid "ORA-12705: Cannot access NLS data files or invalid environment specified."
            AddVMOption -Duser.language=en
            AddVMOption -Duser.region=US
            AddVMOption -Duser.country=en

   5 Restart SQL Developer
   
   
   CREATE A USER ORACLE
   
   1 DROP IF EXISTS
               DROP USER USER;
   2 CREATE USER WITH PASSWORD
               create user USER identified by PASSWORD;
   3 GRANT PRIVILEGES
              grant CREATE SESSION, ALTER SESSION, ALTER USER, CREATE DATABASE LINK, CREATE  MATERIALIZED VIEW,
              CREATE PROCEDURE, CREATE PUBLIC SYNONYM, CREATE ROLE, CREATE SEQUENCE, CREATE SYNONYM, CREATE TABLE, 
              CREATE TRIGGER, CREATE TYPE, CREATE VIEW, CREATE ANY INDEX, UNLIMITED TABLESPACE to USER;



