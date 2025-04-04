# Gym Management API

## Overview
The Gym Management API is a Spring Boot application designed to manage gym members. It provides a RESTful interface for performing CRUD operations on member data, leveraging Spring Data JPA for ORM capabilities.

## Features
- Create, read, update, and delete gym members.
- Utilizes Spring Data JPA for database interactions.
- Simple and intuitive RESTful API design.

## Technologies Used
- Java
- Spring Boot
- Spring Data JPA
- Maven
- H2 Database (for development and testing)

## Project Structure
```
gym-management-api
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com
│   │   │       └── gymmanagement
│   │   │           ├── GymManagementApplication.java
│   │   │           ├── controller
│   │   │           │   └── MemberController.java
│   │   │           ├── model
│   │   │           │   └── Member.java
│   │   │           ├── repository
│   │   │           │   └── MemberRepository.java
│   │   │           └── service
│   │   │               └── MemberService.java
│   │   └── resources
│   │       ├── application.properties
│   │       └── data.sql
│   └── test
│       └── java
│           └── com
│               └── gymmanagement
│                   └── GymManagementApplicationTests.java
├── pom.xml
└── README.md
```

## Setup Instructions
1. **Clone the repository:**
   ```
   git clone https://github.com/yourusername/gym-management-api.git
   cd gym-management-api
   ```

2. **Build the project:**
   ```
   mvn clean install
   ```

3. **Run the application:**
   ```
   mvn spring-boot:run
   ```

4. **Access the API:**
   The API will be available at `http://localhost:8080/api/members`.

## Usage
- **Create a Member:**
  - POST `/api/members`
  - Request Body: `{ "name": "John Doe", "email": "john@example.com", "membershipType": "Premium" }`

- **Get a Member:**
  - GET `/api/members/{id}`

- **Update a Member:**
  - PUT `/api/members/{id}`
  - Request Body: `{ "name": "John Doe", "email": "john.doe@example.com", "membershipType": "Standard" }`

- **Delete a Member:**
  - DELETE `/api/members/{id}`

## Testing
To run the tests, use the following command:
```
mvn test
```

## License
This project is licensed under the MIT License. See the LICENSE file for details.