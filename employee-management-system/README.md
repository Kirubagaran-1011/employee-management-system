# Employee Management System

A Spring Boot REST application for managing employee records with full CRUD operations, using a layered architecture and MySQL for persistent storage.

## Tech Stack
Java 17, Spring Boot 3, Spring Data JPA, Hibernate, MySQL, Maven

## Architecture
`Controller -> Service -> Repository -> MySQL`

## Setup
1. Install Java 17+, Maven and MySQL.
2. Open `src/main/resources/application.properties` and set your MySQL username and password. The database `employee_db` is created automatically.
3. Run:
   ```bash
   mvn spring-boot:run
   ```
4. The API runs at `http://localhost:8080`.

## API Endpoints
| Method | URL | Description |
|--------|-----|-------------|
| GET | `/api/employees` | List all employees (optional `?department=IT`) |
| GET | `/api/employees/{id}` | Get one employee |
| POST | `/api/employees` | Create employee |
| PUT | `/api/employees/{id}` | Update employee |
| DELETE | `/api/employees/{id}` | Delete employee |

### Sample request body
```json
{
  "firstName": "Arun",
  "lastName": "Kumar",
  "email": "arun@example.com",
  "department": "IT",
  "salary": 45000
}
```

## Author
Kirubagaran S
