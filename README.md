# SQL-Injection
*	SQL injection is a code injection technique, used to attack data-driven applications, in which malicious SQL statements are inserted into an entry field for execution.
*	This is a method to attack web applications that have a data repository.
*	The attacker would send a specially crafted SQL statement that is designed to cause some malicious action.
*	It has many forms: extra queries, order by, unions , sub selects

## SQL
*	SQL is a special-purpose programming language designed for managing data held in a relational database management systems (RDBMS).
*	The scope of SQL includes data insert, query, update and delete, schema creation and modification, and data access control.

## Real World Examples
*	On August 17, 2009, the United States Justice Department charged an American citizen Albert Gonzalez and two Russians with the theft of 130 million credit card numbers using an SQL injection attack.
*	In 2008 a sweep of attacks began exploiting the SQL injection vulnerabilities of Microsoft's IIS web server and SQL database server. Over 500,000 sites were exploited.
## Impact of SQL Injection
*	Leakage of sensitive information.
*	Reputation decline.
*	Modification of sensitive information.
*	Loss of control of db server.
*	Data loss.
*	Denial of service.
## How SQL Injection Works?
Steps involved are:
1.	Information Gathering 
2.	SQL injection Vulnerability Detection
*	First attacker lists all the input fields, hidden fields and posts requests
*	Then attacker injects codes into the input field to generate an error
*	Attacker enter ('), (;), (––), AND and/or in input field, if it generates an error page then it means that the website is vulnerable towards the SQL injection.
3.	Launch SQL injection attack
4.	Extract the data
5.	Interact with operating system
6.	Compromise the system

![image](https://user-images.githubusercontent.com/61589430/204804536-e638f642-b0c6-4acb-b2f2-4f63951158c4.png)

## Main consequences of SQL Injection

| Confidentiality | SQL databases generally contains sensitive data, so loss of confidentiality is a big problem.   |
| :---   | :--- |
| Authentication | If poor SQL commands are used to check user names and passwords, authentication can be compromised.   |
| Authorization | SQL databases generally contains sensitive data, so loss of confidentiality is a big problem.   |
| Integrity | If poor SQL commands are used to check user names and passwords, authentication can be compromised.   |


Confidentiality	SQL databases generally contains sensitive data, so loss of confidentiality is a big problem.
Authentication	If poor SQL commands are used to check user names and passwords, authentication can be compromised.
Authorization	If authorization information is held in a SQL database, it can be exploited.
Integrity	SQL Injection attack can change or delete data.

Practices to prevent SQL Injection Attacks
1. Using Prepared Statements (with Parameterized Queries)
Using Prepared Statements is one of the best ways to prevent SQL injection. It’s also simple to write and easier to understand than dynamic SQL queries.
This is where the SQL Command uses a parameter instead of inserting the values directly into the command, thus prevent the backend from running malicious queries that are harmful to the database.
2. Using Stored Procedures
Stored Procedures adds an extra security layer to your database besides using Prepared Statements. It performs the escaping required so that the app treats input as data to be operated on rather than SQL code to be executed.
The difference between prepared statements and stored procedures is that the SQL code for a stored procedure is written and stored in the database server, and then called from the web app.
If user access to the database is only ever permitted via stored procedures, permission for users to directly access data doesn’t need to be explicitly granted on any database table. This way, your database is still safe.
3. Validating user input
Even when you are using Prepared Statements, you should do an input validation first to make sure the value is of the accepted type, length, format, etc. Only the input which passed the validation can be processed to the database. It’s like checking who is at the door of your house before you open it and let them in.
But remember, this method can only stop the most trivial attacks, it does not fix the underlying vulnerability.
4. Limiting privileges
Don’t connect to your database using an account with root access unless required because the attackers might have access to the entire system. Therefore, it’s best to use an account with limited privileges to limit the scope of damages in case of SQL Injection.
5. Hiding info from the error message
Error messages are useful for attackers to learn more about your database architecture, so be sure that you show only the necessary information. It’s better to show a generic error message telling something goes wrong and encourage users to contact the technical support team in case the problem persists.
6. Updating your system
SQL injection vulnerability is a frequent programming error and it’s discovered regularly, so it’s vital to apply patches and updates your system to the most up-to-date version as you can, especially for your SQL Server.
7. Keeping database credentials separate and encrypted
If you are considering where to store your database credentials, also consider how much damaging it can be if it falls into the wrong hands. So always store your database credentials in a separate file and encrypt it securely to make sure that the attackers can’t benefit much.
Also, don’t store sensitive data if you don’t need it and delete information when it’s no longer in use.

## Conclusion
*	SQL Injection is a dangerous vulnerability
*	Transform a normal SQL call to a malicious call
*	Leads to unauthorized access, change or delete data and data stolen
*	All programming languages and all SQL databases are potentially vulnerable

