# Student Management System

## Description
The **Student Management System** is a Java-based application that allows users to manage student records efficiently. It uses **JDBC (Java Database Connectivity)** to interact with a relational database. The system supports operations like adding, updating, deleting, and retrieving student information.

## Features
- Add new students
- Update student details
- Delete students from the system
- Retrieve and display student information
- Uses **JDBC** for database connectivity

## Technologies Used
- **Java SE**
- **JDBC**
- **MySQL (or any RDBMS)**
- **Eclipse/IntelliJ IDEA (or any preferred IDE)**

## Prerequisites
Before running the project, ensure you have the following installed:
- JDK (Java Development Kit) 8 or later
- MySQL Database (or any relational database)
- JDBC Driver for MySQL
- An IDE (Eclipse, IntelliJ IDEA, or NetBeans)

## Database Configuration
1. Create a database named `student_db`.
2. Run the following SQL script to create a `students` table:

```sql
CREATE DATABASE student_db;
USE student_db;

CREATE TABLE students (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100) NOT NULL,
    age INT NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL
);
```

3. Insert sample data if needed:

```sql
INSERT INTO students (name, age, email) VALUES
('John Doe', 20, 'john@example.com'),
('Jane Smith', 22, 'jane@example.com');
```

## Installation and Setup
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/student-management-system.git
   ```
2. Open the project in your preferred Java IDE.
3. Add the MySQL JDBC driver to the project dependencies.
4. Update database connection details in `DBConnection.java`:
   ```java
   String url = "jdbc:mysql://localhost:3306/student_db";
   String user = "root";
   String password = "your_password";
   ```
5. Run the `Main.java` file to start the application.

## Usage
- Run the Java application.
- Follow the menu options to perform CRUD operations on student records.

## Future Enhancements
- Implement a GUI using Java Swing or JavaFX
- Add authentication and user roles
- Integrate with a web interface

## License
This project is open-source and available under the [MIT License](LICENSE).
