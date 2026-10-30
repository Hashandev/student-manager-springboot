# Student Registration System

A Spring Boot web application for managing student records. Staff can add, view, edit and delete students through a simple web form. Data is stored in an H2 database.

Built for **COSC 32133 / BECS 32263 – Full-Stack Software Development**, Lab Sheet 04, University of Kelaniya.

## Features

- Register a student (name, email, phone, course, age)
- Form validation with error messages
- Duplicate email check
- View all students in a table
- Edit and update student details
- Delete a student
- H2 web console to view the database

## Tech Stack

- Java 21
- Spring Boot 4 (Spring Web, Spring Data JPA, Validation, DevTools)
- Thymeleaf
- H2 Database (in-memory)
- Maven

## How to Run

1. Install JDK 21 (or 17).
2. Clone the repository:
   ```bash
   git clone https://github.com/Hashandev/student-manager-springboot.git
   cd student-manager-springboot
   ```
3. Start the application:
   ```bash
   ./mvnw spring-boot:run
   ```
   On Windows use `mvnw.cmd spring-boot:run`.
4. Open http://localhost:8080 in your browser.

## H2 Console

Open http://localhost:8080/h2-console and use:

| Field | Value |
|---|---|
| JDBC URL | `jdbc:h2:mem:studentdb` |
| User Name | `sa` |
| Password | (leave empty) |

Run `SELECT * FROM STUDENTS;` to see the data.

> The database is in-memory, so data is cleared when the application stops.

## Project Structure