# ORACLE-DEVELOPER-FIX
How to fix 'ORA-12705: Cannot access NLS data files or invalid environment specified'




If you are using SQL Developer you have to follow this steps:

    Open SQL Developer package content. Go to Applications, right click on SQL Developer and select "Show Package Contents".
    Go to Contents/Resources/sqldeveloper/sqldeveloper/bin/
    Open sqldeveloper.conf using a text editor.
    Add the following lines:

# Options to avoid "ORA-12705: Cannot access NLS data files or invalid environment specified."
AddVMOption -Duser.language=en
AddVMOption -Duser.region=US
AddVMOption -Duser.country=en

    Restart SQL Developer


