# java-GUI

Java program to get students details from MySQL database.
## Installation
* Download and install Mysql, java
* Download mysql-connector-java-8.0.26
* Add the jar file in your project structure module

## Setting files and Database

After downloading Mysql in Windows, run thr following
commands to create the database of students

```bash
CREATE DATABASE student;
use students
create table stud (student_name VARCHAR(20), branch_name VARCHAR(25));

INSERT INTO student
VALUES ('Vishal', 'CSE');
\q
```
### Java File Description
In the given Java Code

For importing useful packages
```bash
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.ResultSet;
import java.sql.SQLException;
import java.sql.Statement;
```
or directly install all sql packages using
```bash
import sql.*
```
Create connection to database using:- \
Connection con =DriverManager.getConnection(DB_URL, USER, PASSWORD);

To run the Query in the database:- \
Statement stmt = con.createStatement();\
ResultSet rs = stmt.executeQuery(QUERY);

Variable rs points to a row in the table and hence used in printing 
data from each column of the table
```bash
System.out.print("stuydent_Name: " + rs.getString("student_name"));
System.out.print(", Roll_no: " + rs.getString("branch_name"));
```
**Run the program and you will get the required result**
