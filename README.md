# 🗂 Task 7 – Java JDBC Employee Database App

## 🚀 Objective
Build a **Java console app** that connects to a database (MySQL/PostgreSQL) and performs **CRUD** (Create, Read, Update, Delete) operations on an Employee table.

---

## 🛠 Features
1. Add Employee (name, role, salary)  
2. View Employees (list all employees)  
3. Update Employee (role & salary by ID)  
4. Delete Employee (by ID)  

---

## ⚙️ Setup Instructions

### 1. Database Setup (MySQL example)
sql

CREATE DATABASE testdb;
USE testdb;

CREATE TABLE employee (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    role VARCHAR(100),
    salary DOUBLE
);
2. Update DB Config in EmployeeDBApp.java
private static final String URL = "jdbc:mysql://localhost:3306/testdb";
private static final String USER = "root";
private static final String PASSWORD = "yourpassword";

3. Add JDBC Driver in IntelliJ

Go to File > Project Structure > Libraries > + > From Maven

Search and add:

mysql:mysql-connector-java


(Use org.postgresql:postgresql if PostgreSQL)

▶️ Run the Program
javac EmployeeDBApp.java
java -cp .:mysql-connector-j.jar EmployeeDBApp


(On Windows use ; instead of : in classpath.)

In IntelliJ, simply Run the file after adding the JDBC driver.

📸 Sample Run
✅ Connected to Database
--- Employee Menu ---
1) Add Employee
2) View Employees
3) Update Employee
4) Delete Employee
0) Exit

Choice: 1
Enter name: Alice
Enter role: Developer
Enter salary: 55000
✅ Employee added.

Choice: 2
📋 Employee List:
[1] Alice | Developer | 55000.00
