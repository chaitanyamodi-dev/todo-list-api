# Todo List API

A simple and scalable RESTful Todo List API built with **FastAPI**, **SQLAlchemy**, **Pydantic**, and **SQLite**.

This project demonstrates backend API development using a clean structure with separate models, schemas, services, and API routes.

## 🚀 Features

- Create a Todo
- Get all Todos
- Get a Todo by ID
- Update a Todo
- Delete a Todo
- Request validation using Pydantic
- SQLAlchemy ORM integration
- SQLite database
- Automatic API documentation with Swagger UI
- Reusable service layer
- Proper HTTP status codes and error handling

## 🛠️ Tech Stack

- **Python**
- **FastAPI**
- **SQLAlchemy**
- **Pydantic**
- **SQLite**
- **Uvicorn**

## 📁 Project Structure

```text
todo-list-api/
│
├── app/
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

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/your-username/todo-list-api.git
cd todo-list-api
```

### 2. Create a virtual environment

Windows:

```bash
python -m venv venv
```

### 3. Activate the virtual environment

Windows PowerShell:

```powershell
.\venv\Scripts\Activate.ps1
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

## ▶️ Run the Application

Start the FastAPI development server:

```bash
uvicorn main:app --reload
```

The API will be available at:

```text
http://127.0.0.1:8000
```

## 📚 API Documentation

FastAPI automatically provides interactive API documentation.

### Swagger UI

```text
http://127.0.0.1:8000/docs
```

### ReDoc

```text
http://127.0.0.1:8000/redoc
```

## 🔗 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/todos` | Create a Todo |
| GET | `/todos` | Get all Todos |
| GET | `/todos/{todo_id}` | Get a Todo by ID |
| PUT | `/todos/{todo_id}` | Update a Todo |
| DELETE | `/todos/{todo_id}` | Delete a Todo |

## 📝 Example Request

### Create Todo

**POST** `/todos`

```json
{
  "title": "Learn FastAPI",
  "description": "Build a Todo API",
  "completed": false
}
```

### Response

```json
{
  "id": 1,
  "title": "Learn FastAPI",
  "description": "Build a Todo API",
  "completed": false
}
```

## 🔍 Example API Flow

```text
Client
   │
   ▼
FastAPI Router
   │
   ▼
Pydantic Schema
   │
   ▼
Todo Service
   │
   ▼
SQLAlchemy ORM
   │
   ▼
SQLite Database
```

## 🧱 Architecture

The project follows a simple layered structure:

### API Layer

Handles HTTP requests, responses, status codes, and exceptions.

### Schema Layer

Uses Pydantic models for request validation and response serialization.

### Service Layer

Contains the application's Todo business logic and database operations.

### Model Layer

Defines the database structure using SQLAlchemy ORM.

### Database Layer

Creates the SQLAlchemy engine and database session.

## 🎯 Learning Objectives

This project was created to practice:

- FastAPI fundamentals
- REST API development
- CRUD operations
- Pydantic validation
- SQLAlchemy ORM
- Dependency injection
- Database sessions
- API error handling
- Backend project structure
- Interactive API documentation

## 🔮 Future Improvements

Possible future enhancements:

- PostgreSQL integration
- JWT authentication
- User-based Todos
- Pagination
- Search and filtering
- Todo categories
- Due dates
- Docker support
- Automated testing with Pytest
- Alembic database migrations
- CI/CD with GitHub Actions

## 👨‍💻 Author

**Chaitanya Modi**

Python Backend Developer

GitHub: [chaitanyamodi-dev](https://github.com/chaitanyamodi-dev)

LinkedIn: [chaitanya-modi](https://www.linkedin.com/in/chaitanya-modi/)

---

⭐ If you find this project useful, consider giving it a star.
