# Task Manager API

A RESTful Task Management API built with **Java** and **Spring Boot**.
This project allows users to create, view, update, delete, and manage tasks with status tracking.

---

## 🚀 Features

* Create a new task
* List all tasks
* Get a task by ID
* Update an existing task
* Delete a task
* Update task status (`PENDING` / `COMPLETED`)

---

## 🛠 Technologies Used

* Java 17
* Spring Boot
* Spring Web
* Spring Data JPA
* H2 Database
* Maven

---

## 📁 Project Structure

src/main/java/com/ozlem/taskmanager
├── controller
├── model
├── repository
├── service
└── TaskmanagerApplication.java

---

## 📌 API Endpoints

### ➕ Create Task

POST /tasks

```json
{
  "title": "Java proje çalış",
  "description": "Task Manager API tamamlanacak",
  "status": "PENDING"
}
```

---

### 📋 Get All Tasks

GET /tasks

---

### 🔍 Get Task By ID

GET /tasks/{id}

---

### ✏️ Update Task

PUT /tasks/{id}

```json
{
  "title": "Java proje bitti",
  "description": "Task Manager API güncellendi",
  "status": "COMPLETED"
}
```

---

### ❌ Delete Task

DELETE /tasks/{id}

---

### 🔄 Update Task Status

PATCH /tasks/{id}/status?status=COMPLETED

---

## 💾 Database

This project uses **H2 in-memory database**.

H2 Console:
http://localhost:8080/h2-console

Connection settings:

* JDBC URL: jdbc:h2:mem:testdb
* Username: sa
* Password: (leave empty)

---

## ▶️ How to Run

1. Clone the repository:

```
git clone https://github.com/your-username/task-manager-api.git
```

2. Open the project in IntelliJ IDEA

3. Run:

```
TaskmanagerApplication.java
```

4. API runs on:

```
http://localhost:8080
```

---

## 🔮 Future Improvements

* Input validation
* Global exception handling
* DTO structure
* MySQL integration
* Filtering tasks

---

## 👩‍💻 Author

Özlem Tunğ
