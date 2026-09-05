# Banking-Management-System

A backend-based Banking Management System developed using Java and Spring Boot. The application provides essential banking operations such as customer management, account creation, deposits, withdrawals, fund transfers, and transaction tracking through RESTful APIs.

## Project Overview

The Banking Management System is designed to simplify and manage basic banking operations digitally.

The system allows users to create and manage bank accounts, perform financial transactions, and view transaction details. It also provides APIs for managing customers and accounts while maintaining transaction records in a MySQL database.

## Features

* Customer registration and management
* Bank account creation
* Account details management
* Deposit money
* Withdraw money
* Fund transfer between accounts
* Check account balance
* Transaction history
* CRUD operations
* RESTful APIs
* MySQL database integration
* Exception handling
* Input validation
* Layered architecture

## Technologies Used

### Backend

* Java
* Spring Boot
* Spring MVC
* Spring Data JPA
* Hibernate
* RESTful APIs

### Database

* MySQL

### Tools

* Maven
* Postman
* Git
* GitHub
* Eclipse / Spring Tool Suite
* MySQL Workbench

## Project Architecture

The application follows a layered architecture:

```text
Controller
    ↓
Service
    ↓
Repository
    ↓
Database
```

### Controller Layer

Handles HTTP requests and responses through REST APIs.

### Service Layer

Contains the application's business logic, including deposits, withdrawals, transfers, and account operations.

### Repository Layer

Uses Spring Data JPA to communicate with the MySQL database.

### Database Layer

MySQL stores customer, account, and transaction information.

## Main Modules

### Customer Management

* Create customer
* Get customer details
* Update customer information
* Delete customer
* Get all customers

### Account Management

* Create bank account
* Get account details
* Update account information
* Delete account
* Check account balance

### Banking Operations

* Deposit money
* Withdraw money
* Transfer money
* View transaction history

## Database Design

The application can contain the following main entities:

```text
Customer
   |
   | 1
   |
   | *
Account
   |
   | 1
   |
   | *
Transaction
```

### Customer

Stores customer information such as:

* Customer ID
* Name
* Email
* Phone
* Address

### Account

Stores account-related information such as:

* Account ID
* Account Number
* Account Type
* Balance
* Customer ID

### Transaction

Stores transaction details such as:

* Transaction ID
* Transaction Type
* Amount
* Date and Time
* Source Account
* Destination Account

## REST API Examples

### Customer APIs

```text
POST   /api/customers
GET    /api/customers
GET    /api/customers/{id}
PUT    /api/customers/{id}
DELETE /api/customers/{id}
```

### Account APIs

```text
POST   /api/accounts
GET    /api/accounts
GET    /api/accounts/{id}
PUT    /api/accounts/{id}
DELETE /api/accounts/{id}
```

### Banking APIs

```text
POST /api/accounts/{accountNumber}/deposit
POST /api/accounts/{accountNumber}/withdraw
POST /api/accounts/transfer
GET  /api/accounts/{accountNumber}/balance
GET  /api/accounts/{accountNumber}/transactions
```

## Example Banking Workflow

```text
Customer Registration
        ↓
Account Creation
        ↓
Account Number Generated
        ↓
Deposit Money
        ↓
Withdraw / Transfer Money
        ↓
Transaction Recorded
        ↓
View Transaction History
```

## Project Structure

```text
banking-management-system/
│
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/example/banking/
│   │   │       ├── controller/
│   │   │       ├── service/
│   │   │       ├── repository/
│   │   │       ├── entity/
│   │   │       ├── dto/
│   │   │       ├── exception/
│   │   │       └── BankingApplication.java
│   │   │
│   │   └── resources/
│   │       └── application.properties
│   │
│   └── test/
│
├── pom.xml
└── README.md
```

## Configuration

Update the `application.properties` file according to your MySQL configuration.

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/banking_db
spring.datasource.username=root
spring.datasource.password=your_password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

server.port=8080
```

## How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/banking-management-system.git
```

### 2. Open the Project

Open the project in:

* Eclipse
* Spring Tool Suite
* IntelliJ IDEA
* VS Code

### 3. Configure MySQL

Create a database:

```sql
CREATE DATABASE banking_db;
```

Update your MySQL username and password in `application.properties`.

### 4. Build the Project

```bash
mvn clean install
```

### 5. Run the Application

```bash
mvn spring-boot:run
```

The application will run on:

```text
http://localhost:8080
```

## Testing

The REST APIs can be tested using Postman.

Example:

```text
POST http://localhost:8080/api/customers
```

Request body:

```json
{
  "name": "Abhishek",
  "email": "abhishek@example.com",
  "phone": "9876543210",
  "address": "Noida"
}
```

## Key Concepts Implemented

This project demonstrates practical knowledge of:

* Core Java
* Object-Oriented Programming
* Collections
* Exception Handling
* Spring Boot
* Spring MVC
* REST API development
* Spring Data JPA
* Hibernate ORM
* CRUD operations
* MySQL
* Database relationships
* Layered architecture
* Business logic implementation
* API testing with Postman

## Future Enhancements

* JWT-based authentication
* Role-based authorization
* Admin dashboard
* Online bill payments
* Loan management
* Email/SMS notifications
* Account statement generation
* Transaction search and filtering
* Frontend using React.js
* Deployment using Render/AWS

## Author

**Abhishek**

B.Tech Computer Science and Engineering

Java Backend / Full Stack Developer

## License

This project is created for educational and portfolio purposes.
