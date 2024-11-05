# Student Database Project

A simple Java application to manage student data in a MySQL database. This program allows you to insert, view, and manage students' information, such as student ID, first name, last name, and enrollment date.

## Features

- Connects to a MySQL database.
- Allows insertion of student data into the database.
- Fetches and displays student data from the database.

## Prerequisites

Before running the program, make sure you have:

- **Java Development Kit (JDK)** installed on your computer (JDK 8 or later).
- **MySQL** installed and running on your machine.
- **MySQL database** with a table for storing student data. Below is the SQL schema to create the `students` table:

## Setup
1. Clone the Repository
- Open Your Terminal or Command Prompt
- Clone the repository to your local machine
- Paste the URL you copied from GitHub
```
git clone https://github.com/yourusername/StudentDatabaseProject.git
```


2. Set Up the MySQL Database
- Install MySQL on your machine if you don't have it already.
- Create a Database:
  - Log into MySQL and run the following commands to create a school database and a students table.

   ```sql
   CREATE DATABASE school;
   USE school;

   CREATE TABLE students (
       id INT AUTO_INCREMENT PRIMARY KEY,
       first_name VARCHAR(100),
       last_name VARCHAR(100),
       enrollment_date DATE
   );
  
3. Add the MySQL JDBC Connector

Download the MySQL JDBC connector (JAR file) from here. After downloading:

- In IntelliJ, go to **File > Project Structure > Libraries**. 
- Click on + to add the **JAR file** for the connector.
- Make sure the library is correctly added to the project dependencies. 

4. Configure Database Connection
   In the StudentDatabase.java file, update the database connection details:

```java
String jdbcUrl = "jdbc:mysql://localhost:3306/school"; // Database URL
String username = "root"; // MySQL username
String password = "yourpassword"; // MySQL password ;
```
- Make sure to replace "yourpassword" with your actual MySQL password.

## Running the Program
- Open the project in IntelliJ IDEA.
- Ensure the MySQL server is running.
- Run the StudentDatabase.java class. 
  - The program will connect to your MySQL database, retrieve student records, and display them in the console.

Example Output:
```
Student ID: 1
First Name: Nikki
Last Name: Brown
Enrollment Date: 2024-08-13
---------------------------
Student ID: 2
First Name: Breeze
Last Name: Johnson
Enrollment Date: 2024-08-14
---------------------------
```
## Contributing
- Fork this repository to your own GitHub account.
- Create a new branch (git checkout -b feature-name).
- Make changes and commit them (git commit -am 'Add new feature').
- Push to the branch (git push origin feature-name).
- Submit a pull request to the main repository.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
