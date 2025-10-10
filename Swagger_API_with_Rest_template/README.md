# Employee Service & Employee Order - REST API Integration

This project demonstrates the integration of two microservices: **Employee Service** and **Employee Order Service**. Both services interact with each other via REST APIs and are tested using Swagger UI for seamless API documentation and testing.

## Table of Contents

- [Overview](#overview)
- [Architecture](#architecture)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [How to Run](#how-to-run)
- [API Documentation (Swagger)](#api-documentation-swagger)
- [Project Structure](#project-structure)
- [Contact](#contact)

---

## Overview

The project consists of two Spring Boot microservices:

1. **Employee Service**  
   Manages employee data such as creation, retrieval, updating, and deletion of employee records.

2. **Employee Order Service**  
   Handles orders placed by employees and interacts with the Employee Service to fetch employee details as needed.

These services communicate over REST APIs and are tested and documented using Swagger UI.

---

## Architecture

```plaintext
+-------------------+            REST API            +------------------------+
|                   | <--------------------------->  |                        |
|  Employee Service |                                |  Employee Order Service |
|                   | <--------------------------->  |                        |
+-------------------+                                +------------------------+
        ^                                                        ^
        |                                                        |
        |                Swagger UI (for both services)           |
        +--------------------------------------------------------+
```

---

## Features

- **Employee Service**
  - list employees
  - Exposes REST endpoints for employee management

- **Employee Order Service**
  - list orders for employees
  - Fetches employee information from Employee Service via REST API

- **RESTful Communication**
  - Uses `RestTemplate` to communicate between services

- **Swagger Integration**
  - Interactive documentation and testing for all APIs

---

## Technologies Used

- Java
- Spring Boot
- Spring Web
- Swagger 
- Maven

---

## How to Run

1. **Clone the Repository**

    ```bash
    git clone https://github.com/OmkarRMundhe/Daily_Assignment.git
    cd Daily_Assignment/Swagger_API_with_Rest_template
    ```

2. **Build and Run Each Service**

    - Each service should have its own Spring Boot application entry point.
    - Run each service on a different port (configure in `application.properties`).

    ```bash
    # For Employee Service:
    cd employee-service
    mvn spring-boot:run

    # For Employee Order Service:
    cd ../employee-order-service
    mvn spring-boot:run
    ```

3. **Access Swagger UI**

    - By default, Swagger UI can be accessed at:
      - `http://localhost:8083/swagger-ui.html` (Employee Service)
      - `http://localhost:8081/swagger-ui.html` (Employee Order Service)

    - Use the Swagger UI to test the APIs and see documentation.

---

## API Documentation (Swagger)

- **Interactive API documentation** is provided using Swagger UI for both services.
- You can:
  - Explore API endpoints
  - Execute API calls directly from the browser
  - View sample requests and responses

---

## Project Structure

```plaintext
Swagger_API_with_Rest_template/
│
├── employee-service/
│   ├── src/
│   ├── pom.xml
│   └── ...
│
├── employee-order-service/
│   ├── src/
│   ├── pom.xml
│   └── ...
│
└── README.md
```

---



- **Omkar R Mundhe**
- [GitHub Profile](https://github.com/OmkarRMundhe)

---
