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


