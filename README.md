# Student Records Database System

A university student records management system developed using Python and MySQL.

The project combines relational database design with a Python interface to manage academic information such as students, faculty members, colleges, departments, courses, sections, enrollment, and teaching assignments.

The system demonstrates database modeling, normalization, SQL operations, relational queries, and Python–MySQL integration.

## Project Overview

Universities manage large amounts of interconnected academic information, including:

- Students
- Faculty members
- Colleges
- Departments
- Courses
- Course sections
- Student enrollment
- Faculty assignments

The Student Records Database System was designed to organize this information within a structured relational database and provide users with a Python-based interface for performing common academic operations.

## Project Objectives

The main objectives of the project are to:

- Design a relational database for university academic records
- Model relationships between students, faculty, departments, and courses
- Reduce data redundancy through normalization
- Maintain data consistency using database constraints
- Connect a Python application to a MySQL database
- Perform database operations using SQL queries
- Support student and faculty academic operations
- Provide course search and information retrieval functionality

## Database Design

The database was designed using entity-relationship modeling and a relational schema.

The main entities include:

- College
- Department
- Course
- Faculty
- Student
- Section

The database also contains relationship tables that connect these entities.

### Relationship Tables

#### `Offers`

Represents the relationship between departments and the courses they offer.

#### `Studies_in`

Represents student enrollment in course sections.

#### `Works_for`

Represents the relationship between faculty members and departments.

## Database Normalization

The database was designed in **Third Normal Form (3NF)**.

Normalization was used to:

- Reduce duplicate data
- Improve data organization
- Maintain consistency
- Minimize update anomalies
- Create clearer relationships between entities

Database constraints were also used to maintain data integrity.

## System Features

The Python application provides several student and faculty operations.

### View Courses

Displays the courses stored in the database.

### View Departments

Displays available university departments.

### Course Enrollment

Allows a student to enroll in a course section.

The enrollment is recorded in the `Studies_in` relationship table.

### Faculty Operations

Faculty functionality includes:

- Viewing teaching schedules
- Viewing students enrolled in a specific section

### View Student Information

Allows academic information for a specific student to be retrieved from the database.

### Search Courses

Users can search for courses by course name.

The application performs a dynamic SQL search and returns matching course records.

### Update Student Details

Student information can be updated through the application.

The implemented interface allows a student's major to be modified in the database.

### View Sections

Displays all course sections stored in the database.

## Application Menu

The Python application provides the following command-line menu:

```text
1. View Courses
2. View Departments
3. Enroll in Course
4. Faculty Operations
5. View Student Information
6. Search Courses
7. Update Student Details
8. View Sections
9. Exit
```

## Python and MySQL Integration

The application uses the `mysql.connector` Python package to communicate with the MySQL database.

The connection allows Python functions to execute SQL operations such as:

- `SELECT`
- `INSERT`
- `UPDATE`
- SQL joins
- Parameterized queries

The application retrieves information from MySQL, displays results to the user, and commits changes when database records are modified.

## Example Database Operations

### Retrieve Courses

The system retrieves course information from the `Course` table.

```sql
SELECT * FROM Course;
```

### Retrieve Departments

```sql
SELECT * FROM Department;
```

### Enroll a Student

Enrollment adds a relationship between a student and a section.

```sql
INSERT INTO Studies_in (StudentID, Section_number)
VALUES (...);
```

### Retrieve a Faculty Teaching Schedule

```sql
SELECT *
FROM Section
WHERE FacultyID = ...;
```

### Search for Courses

The application supports partial course-name searching using SQL `LIKE`.

```sql
SELECT *
FROM Course
WHERE Course_Name LIKE ...;
```

### Update Student Information

The application can update a student's major.

```sql
UPDATE Student
SET Major = ...
WHERE StudentID = ...;
```

## Technologies Used

- Python
- MySQL
- SQL
- MySQL Connector for Python
- XAMPP
- Visual Studio Code
- Relational Database Design
- Entity-Relationship Modeling
- Database Normalization

## Database Concepts Demonstrated

This project demonstrates several database concepts, including:

- Relational database design
- Entity-Relationship modeling
- Relational schemas
- Primary and foreign key relationships
- Database constraints
- Third Normal Form (3NF)
- SQL queries
- SQL joins
- Data insertion
- Data retrieval
- Data updates
- Relationship tables
- Python database connectivity
- Parameterized SQL queries

## Project Structure

```text
student-records-database-system/
│
├── database/
│   └── university3.sql
│
├── report/
│   └── Final Project Report.pdf
│
├── src/
│   └── university.py
│
└── README.md
```

## Main Files

- `database/university3.sql` — MySQL database file containing the university database structure and data
- `src/university.py` — Python application used to interact with the MySQL database
- `report/Final Project Report.pdf` — Project report documenting the database design, implementation, functionality, code, and outputs
- `README.md` — Repository documentation

## How to Run the Project

### 1. Install Python

Make sure Python is installed on your computer.

### 2. Install MySQL

Install MySQL or use a local environment such as XAMPP.

### 3. Install MySQL Connector

Install the Python MySQL connector:

```bash
pip install mysql-connector-python
```

### 4. Import the Database

Import:

```text
database/university3.sql
```

into your MySQL environment.

### 5. Configure the Database Connection

Configure the MySQL connection settings in:

```text
src/university.py
```

to match your local database environment.

Do not commit personal database credentials or passwords to a public repository.

### 6. Run the Application

From the project directory, run:

```bash
python src/university.py
```

The Student Records menu will appear in the terminal.

## Example Workflow

A user can:

1. Start the Python application.
2. View available courses.
3. Search for a specific course.
4. Enroll a student in a course section.
5. Retrieve student information.
6. View faculty teaching schedules.
7. View students enrolled in a section.
8. Update student information.
9. View available sections.
10. Exit the application.

## Key Learning Outcomes

This project provided experience with:

- Designing a database from an academic scenario
- Modeling complex relationships between entities
- Normalizing a relational database
- Writing SQL queries
- Connecting Python to MySQL
- Retrieving and modifying database records
- Building a menu-driven database application
- Debugging database and application errors
- Maintaining data consistency
- Collaborative software development

## Notes

- The system was developed as a university database project.
- MySQL is used for backend data storage.
- Python provides the application interface.
- MySQL Connector enables communication between Python and MySQL.
- The database is normalized to Third Normal Form (3NF).
- The application is intended for educational and demonstration purposes.

## Authors

- Ghala Alghamdi
- Hiba Amanulla
- Natali Soukh
- Effat University
- Computer Science Department
- Course: CS2071 – Database Systems
- Instructor: Dr. Zain Balfagih
