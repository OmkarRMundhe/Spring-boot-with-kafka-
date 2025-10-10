# Spring Security Examples

This directory contains examples and configurations for securing a Spring Boot application using Spring Security.

## Overview

Spring Security is a powerful and customizable authentication and access-control framework for Java applications, especially Spring-based projects. The examples here demonstrate how to implement various security mechanisms in a Spring Boot application.

## Features Demonstrated

- **Authentication:**  
  How to secure endpoints using in-memory, JDBC, or custom user details service.

- **Authorization:**  
  Role-based access control for REST APIs or web endpoints.

- **Password Encoding:**  
  Using password encoders to securely store and validate user credentials.

- **JWT:**  
  Examples of securing APIs using JSON Web Tokens.

## Folder Structure

```
spring_security/
├── src/
│   └── main/
│       ├── java/
│       │   └── [com.example.demo]/SpringSecurityApplication.java
│                                  ├──config/SecurityConfig.java
│                                  ├──controller/authcontroller.java
│                                               /UserController.java 
│                                  ├──entity/Role.java
│                                           /User.java 
│                                  ├──repository/UserRepository.java
│                                  ├──service/CustomeUserDetails.java
│                                  ├──utils/JwtFilter.java
│                                          /JwtService.java
│                                          /LoggingFilter.java    
│       └── resources/
│           └── application.properties
├── README.md
```

## Getting Started

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/OmkarRMundhe/Daily_Assignment.git
   cd Daily_Assignment/spring_security
   ```

2. **Configure Properties:**
   Update `application.properties` for your database, security settings, and other configurations as needed.

3. **Run the Application:**
   ```bash
   ./mvnw spring-boot:run
   ```
   or
   ```bash
   ./gradlew bootRun
   ```

4. **Access the Endpoints:**
   Test the secured endpoints using Postman, curl, or your browser.

## Example Endpoints

- `/login` - Form-based authentication
- `/api/secure` - Endpoint protected by roles
- `/logout` - Logout functionality

## Customization

- Modify security configurations in `SecurityConfig.java` for custom requirements.
- Add or modify roles and users as per your needs.

