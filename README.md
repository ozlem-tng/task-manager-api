# Task Manager API

A RESTful Task Management API built with **Java** and **Spring Boot**.
This project allows users to create, view, update, delete, and manage tasks with status tracking.

---

## Features

* Create a new task
* List all tasks
* Get a task by ID
* Update an existing task
* Delete a task
* Update task status (`PENDING` / `COMPLETED`)
* Input validation for task fields
* Global exception handling for validation errors
* Custom exception handling for non-existing tasks

---

## Technologies Used

* Java 17
* Spring Boot
* Spring Web
* Spring Data JPA
* H2 Database
* Maven

---

## Project Structure

```bash
src/main/java/com/ozlem/taskmanager
├── controller
├── exception
├── model
├── repository
├── service
└── TaskmanagerApplication.java
```

---

## API Endpoints

### Create Task

**POST** `/tasks`

Example request body:

```json
{
  "title": "Java proje çalış",
  "description": "Task Manager API tamamlanacak",
  "status": "PENDING"
}
```

### Get All Tasks

**GET** `/tasks`

### Get Task By ID

**GET** `/tasks/{id}`

### Update Task

**PUT** `/tasks/{id}`

Example request body:

```json
{
  "title": "Java proje bitti",
  "description": "Task Manager API güncellendi",
  "status": "COMPLETED"
}
```

### Delete Task

**DELETE** `/tasks/{id}`

### Update Task Status

**PATCH** `/tasks/{id}/status?status=COMPLETED`

---

## Validation Example

If an invalid request is sent, the API returns a validation error response.

Example response:

```json
{
  "title": "Title must be between 3 and 100 characters"
}
```

---

## Not Found Example

If a task with a given ID does not exist, the API returns:

```json
{
  "error": "Task not found with id: 999"
}
```

---

## Database

This project uses **H2 in-memory database**.

H2 Console:
`http://localhost:8080/h2-console`

Connection settings:

* JDBC URL: `jdbc:h2:mem:testdb`
* Username: `sa`
* Password: leave empty

---

## How to Run

1. Clone the repository:

```bash
git clone https://github.com/ozlem-tng/task-manager-api.git
```

2. Open the project in IntelliJ IDEA

3. Run:

```bash
TaskmanagerApplication.java
```

4. The API runs on:

```bash
http://localhost:8080
```

---

## Future Improvements

* Filter tasks by status
* Add due date and priority support
* DTO structure for request/response separation
* MySQL integration

---

## Author

Özlem Tunğ
