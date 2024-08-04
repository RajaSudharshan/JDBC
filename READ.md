# JDBC Operations with MySQL Workbench

This project demonstrates various JDBC operations with a MySQL database. The operations include reading, inserting, updating, deleting records, calling stored procedures, and batch processing.

## Prerequisites

1. **Java Development Kit (JDK)**: Ensure JDK is installed. You can download it from [Oracle's official site](https://www.oracle.com/java/technologies/javase-downloads.html).

2. **MySQL Server**: Ensure MySQL Server is installed. You can download it from [MySQL's official site](https://dev.mysql.com/downloads/mysql/).

3. **MySQL Workbench**: Ensure MySQL Workbench is installed. You can download it from [MySQL Workbench's official site](https://dev.mysql.com/downloads/workbench/).

4. **MySQL Connector/J (JAR file)**: Download the MySQL JDBC driver (Connector/J) from [here](https://dev.mysql.com/downloads/connector/j/).

## Setup Instructions

### Step 1: Install MySQL Server and Workbench

1. Install MySQL Server following the instructions for your operating system.
2. Install MySQL Workbench for database management.

### Step 2: Create Database and Table

1. Open MySQL Workbench and connect to your local MySQL server.
2. Execute the following SQL commands to create a database and table:

    ```sql
    CREATE DATABASE jdbcdemo;
    USE jdbcdemo;

    CREATE TABLE employee (
        emp_id INT PRIMARY KEY,
        name VARCHAR(50),
        salary INT
    );
    ```

### Step 3: Add MySQL Connector/J to Your Project

1. Place the downloaded MySQL Connector/J JAR file (e.g., `mysql-connector-java-8.0.26.jar`) in your project's `lib` directory (create one if it doesn't exist).

2. Add the JAR file to your project's classpath. If you're using an IDE like IntelliJ IDEA or Eclipse, you can add the JAR file to the project via Project Settings.

### Step 4: Compile and Run the Java Program

1. Compile the Java program:

    ```sh
    javac -cp .;lib/mysql-connector-java-8.0.26.jar Jdbc.java
    ```

2. Run the Java program:

    ```sh
    java -cp .;lib/mysql-connector-java-8.0.26.jar Jdbc
    ```

## JDBC Operations

The following methods are available in the `Jdbc` class:

- `readRecords()`: Reads and displays all records from the `employee` table.
- `insertRecord()`: Inserts a new record into the `employee` table.
- `insertVar()`: Inserts a new record using variables.
- `insertUsingPst()`: Inserts a new record using a prepared statement.
- `delete()`: Deletes a record from the `employee` table.
- `update()`: Updates a record in the `employee` table.
- `sp()`: Calls a stored procedure to get all employee records.
- `sp2()`: Calls a stored procedure with an input parameter.
- `sp3()`: Calls a stored procedure with input and output parameters.
- `commitdemo()`: Demonstrates transaction management with commit and rollback.
- `batchdemo()`: Demonstrates batch processing.

Uncomment the desired method calls in the `main` method to test them.

### Example Usage

```java
public static void main(String[] args) throws Exception {
    // Example of calling a method
    readRecords();
    insertRecord();

}
