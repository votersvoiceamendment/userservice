# User Service

This project is the **User Service** component of the **Voters Voice Amendment (VVA)** system. It handles all user-related functionalities such as registration, login, profile management, and user authentication for interacting with various services within the VVA ecosystem.

## Features

- **User Registration and Login**:
    - Create new user accounts.
    - User authentication via JWT.
    - Handle login and logout actions.

- **User Profile Management**:
    - Update user profiles.
    - Retrieve user information.

- **Session Management**:
    - Issue and validate JWT tokens for authentication.
    - Handle session expiration and token refresh.

## Technologies Used

- **Spring Boot** 3.3.4 (Java 23)
    - **Spring Web**: For building RESTful APIs.
    - **Spring Security**: For authentication and authorization.
    - **Spring Data JPA**: For interacting with the PostgreSQL database.
    - **PostgreSQL**: As the relational database to store user data.

## Project Setup

### Prerequisites

Before running this project, ensure you have the following installed:

- **Java 23**
- **Maven**
- **PostgreSQL** (If running locally)

### Build and Run the Project

1. **Clone the repository**:
    ```bash
    git clone https://github.com/your-username/userservice.git
    cd userservice
    ```

2. **Build the project**:
    ```bash
    mvn clean package
    ```

3. **Run the application**:
    ```bash
    mvn spring-boot:run
    ```

The application will start on [http://localhost:8080](http://localhost:8080) by default.

### Dockerization

This service is containerized using Docker. You can build and run the Docker container as follows:

1. **Build the Docker image**:
    ```bash
    docker build -t userservice .
    ```

2. **Run the Docker container**:
    ```bash
    docker run -p 8080:8080 userservice
    ```

### Database Configuration

The project is configured to use **PostgreSQL**. You can set the database credentials in the `application.properties` or use environment variables to override them.

**Example properties**:
```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/user_service
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
