# 🚀 Taskify — Task Management REST API

**Taskify** is a clean and scalable **Task Management REST API** built with **FastAPI, SQLAlchemy, Pydantic, and SQLite**.

The project provides a structured backend for creating, managing, updating, and tracking tasks through RESTful APIs.

It demonstrates backend development practices such as **layered architecture, request validation, ORM-based database operations, service-layer business logic, error handling, and automatic API documentation**.

---

## ✨ Features

* ✅ Create tasks
* 📋 Get all tasks
* 🔍 Get a task by ID
* ✏️ Update tasks
* 🗑️ Delete tasks
* ☑️ Track task completion
* 📝 Task title and description
* 🔐 Request validation using Pydantic
* 🗄️ SQLAlchemy ORM integration
* 💾 SQLite database
* ⚡ FastAPI RESTful APIs
* 📚 Automatic Swagger UI documentation
* 📖 ReDoc API documentation
* 🧩 Layered backend architecture
* ⚠️ HTTP status codes and error handling
* 🔄 Reusable service layer

---

## 🎨 Taskify Design

Taskify is designed with a **clean, minimal, and productivity-focused** approach.

### UI Concept



### Design Principles

* 🎯 Simple and focused task management
* 🧹 Clean and minimal interface
* 📱 Responsive design
* 🗂️ Organized task categories
* ⭐ Priority-based task management
* 📅 Date-based task organization
* ⚡ Fast and intuitive workflow

---

## 🛠️ Tech Stack

| Technology         | Purpose                     |
| ------------------ | --------------------------- |
| 🐍 **Python**      | Backend programming         |
| ⚡ **FastAPI**      | REST API framework          |
| 🗃️ **SQLAlchemy** | ORM and database operations |
| 🔐 **Pydantic**    | Request/response validation |
| 💾 **SQLite**      | Database                    |
| 🚀 **Uvicorn**     | ASGI server                 |
| 📚 **Swagger UI**  | API documentation           |

---

## 📁 Project Structure

```text
taskify/
│
├── app/
│   │
│   ├── core/
│   │   └── database.py
│   │
│   ├── models/
│   │   └── todo.py
│   │
│   ├── schemas/
│   │   └── todo.py
│   │
│   ├── services/
│   │   └── todo_service.py
│   │
│   ├── __init__.py
│   └── api.py
│
├── main.py
├── requirements.txt
├── .gitignore
├── todos.db
└── README.md
```

> **Note:** The current backend uses the existing `todo` model/service naming. These can later be renamed to `task` as the project evolves.

---

# ⚙️ Installation

## 1. Clone the Repository

```bash
git clone https://github.com/chaitanyamodi-dev/taskify.git
```

```bash
cd taskify
```

---

## 2. Create a Virtual Environment

### Windows

```bash
python -m venv venv
```

---

## 3. Activate the Virtual Environment

### Windows PowerShell

```powershell
.\venv\Scripts\Activate.ps1
```

---

## 4. Install Dependencies

```bash
pip install -r requirements.txt
```

---

# ▶️ Run the Application

Start the FastAPI development server:

```bash
uvicorn main:app --reload
```

The application will run at:

```text
http://127.0.0.1:8000
```

---

# 📚 API Documentation

FastAPI automatically generates interactive API documentation.

### 🔵 Swagger UI

```text
http://127.0.0.1:8000/docs
```

Swagger allows you to test all API endpoints directly from your browser.

### 🟢 ReDoc

```text
http://127.0.0.1:8000/redoc
```

---

# 🔗 API Endpoints

| Method   | Endpoint           | Description      |
| -------- | ------------------ | ---------------- |
| `POST`   | `/todos`           | Create a task    |
| `GET`    | `/todos`           | Get all tasks    |
| `GET`    | `/todos/{todo_id}` | Get a task by ID |
| `PUT`    | `/todos/{todo_id}` | Update a task    |
| `DELETE` | `/todos/{todo_id}` | Delete a task    |

---

# 📝 Example API Request

## Create a Task

### Request

```http
POST /todos
```

### JSON

```json
{
  "title": "Learn FastAPI",
  "description": "Build a Taskify REST API",
  "completed": false
}
```

### Response

```json
{
  "id": 1,
  "title": "Learn FastAPI",
  "description": "Build a Taskify REST API",
  "completed": false
}
```

---

# 🔄 API Flow

```text
             Client
                │
                ▼
        ┌─────────────────┐
        │  FastAPI Router │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │ Pydantic Schema │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │  Service Layer  │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │ SQLAlchemy ORM  │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │ SQLite Database │
        └─────────────────┘
```

---

# 🧱 Architecture

Taskify follows a simple **layered backend architecture**.

### 🌐 API Layer

Responsible for:

* HTTP requests
* HTTP responses
* Routes
* Status codes
* API-level exception handling

### 🔐 Schema Layer

Uses **Pydantic** for:

* Request validation
* Response serialization
* Data type validation

### ⚙️ Service Layer

Contains:

* Task business logic
* CRUD operations
* Database interaction logic

### 🗃️ Model Layer

Uses **SQLAlchemy ORM** to define:

* Database tables
* Columns
* Database relationships

### 💾 Database Layer

Responsible for:

* SQLAlchemy engine
* Database connection
* Database sessions

---

# 🎯 Learning Objectives

This project was built to practice and demonstrate:

* 🐍 Python backend development
* ⚡ FastAPI fundamentals
* 🌐 REST API development
* 🔄 CRUD operations
* 🔐 Pydantic validation
* 🗃️ SQLAlchemy ORM
* 💉 FastAPI dependency injection
* 💾 Database sessions
* ⚠️ API error handling
* 🧱 Layered architecture
* 📚 Swagger/OpenAPI documentation

---

# 🚀 Future Improvements

Taskify can be extended into a complete productivity platform.

### 🔐 Authentication

* JWT authentication
* User registration and login
* User-specific tasks
* Role-based access control

### 📋 Task Management

* Task priorities
* Categories
* Tags
* Due dates
* Reminders
* Search
* Filtering
* Sorting
* Pagination

### 📊 Productivity

* Productivity dashboard
* Completed-task statistics
* Daily/weekly progress
* Task analytics

### 🗄️ Backend Improvements

* PostgreSQL integration
* Alembic migrations
* Redis caching
* Background tasks
* Automated testing with Pytest

### 🐳 Deployment

* Docker
* Docker Compose
* GitHub Actions
* CI/CD
* Cloud deployment

### 🎨 Frontend

A dedicated frontend can later be added with:

* React
* Next.js
* Vue.js

---

# 🗺️ Project Roadmap

```text
Phase 1
───────
✅ FastAPI Setup
✅ Database Setup
✅ CRUD APIs
✅ Pydantic Validation
✅ SQLAlchemy ORM
✅ Swagger Documentation

        ↓

Phase 2
───────
🔲 JWT Authentication
🔲 User Management
🔲 User-specific Tasks
🔲 Task Categories
🔲 Priorities
🔲 Due Dates

        ↓

Phase 3
───────
🔲 Search & Filtering
🔲 Pagination
🔲 Task Statistics
🔲 Productivity Dashboard

        ↓

Phase 4
───────
🔲 React / Next.js Frontend
🔲 Docker
🔲 PostgreSQL
🔲 CI/CD
🔲 Cloud Deployment
```

---

# 📸 Screenshots

Add screenshots here after completing the UI:

```text
docs/
├── dashboard.png
├── task-list.png
├── add-task.png
└── swagger.png
```

Example:

```markdown
## 📸 Screenshots

### Dashboard

![Taskify Dashboard](docs/dashboard.png)

### Swagger API

![Taskify Swagger](docs/swagger.png)
```

---

# 👨‍💻 Author

**Chaitanya Modi**

🐍 Python Backend Developer

* 💻 GitHub: [chaitanyamodi-dev](https://github.com/chaitanyamodi-dev)
* 🔗 LinkedIn: [chaitanya-modi](https://www.linkedin.com/in/chaitanya-modi-dev/)

---

## ⭐ Support

If you find **Taskify** useful or interesting, consider giving the repository a ⭐ on GitHub.

---

**Taskify — Plan it. Track it. Get it done.** 🚀
