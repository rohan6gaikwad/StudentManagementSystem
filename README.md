# Student Management System

A Java web application for managing student records, built with **Spring Boot**, **Spring Data JPA**, **Thymeleaf**, and **MySQL**.

> **Status:** 🚧 Early development — project scaffold is set up; core features (student CRUD, database schema, views) are in progress.

## Tech Stack

- **Backend:** Java 17, Spring Boot 3.5
- **Data:** Spring Data JPA (Hibernate), MySQL
- **Views:** Thymeleaf (server-side rendering)
- **Build tool:** Maven
- **Dev tooling:** Spring Boot DevTools (hot reload)

## Features

Planned functionality for this project:

- [ ] Add, view, edit, and delete student records
- [ ] Search / filter students
- [ ] Form validation on student data entry
- [ ] Persist data to MySQL via JPA repositories
- [ ] Server-rendered UI with Thymeleaf templates

*(Check these off as they're implemented — none are built yet.)*

## Prerequisites

- Java 17+
- Maven 3.8+ (or use the included `./mvnw` wrapper — no local Maven install needed)
- MySQL 8+ running locally

## Setup

### 1. Clone the repository

```bash
git clone https://github.com/rohan6gaiwad/StudentManagementSystem.git
cd StudentManagementSystem
```

### 2. Create the database

```sql
CREATE DATABASE student_management_system;
```

### 3. Configure the database connection

Add the following to `src/main/resources/application.properties` (not yet present — required before running):

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/student_management_system
spring.datasource.username=root
spring.datasource.password=your_mysql_password
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

### 4. Run the application

Using the Maven wrapper (recommended, no local Maven required):

```bash
./mvnw spring-boot:run
```

Or build and run the jar directly:

```bash
./mvnw clean package
java -jar target/StudentManagementSystem-0.0.1-SNAPSHOT.jar
```

The app will be available at `http://localhost:8080`.

## Project Structure

```
StudentManagementSystem/
├── pom.xml
├── mvnw / mvnw.cmd
├── src/
│   ├── main/
│   │   ├── java/com/StudentManagementSystem/
│   │   │   └── StudentManagementSystemApplication.java
│   │   └── resources/
│   │       └── application.properties
│   └── test/
│       └── java/com/StudentManagementSystem/
│           └── StudentManagementSystemApplicationTests.java
```

## Roadmap

- [ ] Define `Student` entity and JPA repository
- [ ] Build controller + service layer for student CRUD
- [ ] Add Thymeleaf templates (list, add/edit form, delete confirmation)
- [ ] Add basic validation and error handling
- [ ] Add unit/integration tests

## Author

**Rohan Gaikwad**

## License

Not yet specified.