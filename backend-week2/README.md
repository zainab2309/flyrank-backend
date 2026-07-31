# Task API

A simple REST API built with **FastAPI** that manages a to-do list using CRUD (Create, Read, Update, Delete) operations.

This project was created as part of the FlyRank Backend Internship Week 2 assignment.

---

## Features

* Create a new task
* View all tasks
* View a single task by ID
* Update an existing task
* Delete a task
* Interactive Swagger UI documentation

---

## Technologies Used

* Python 3
* FastAPI
* Uvicorn

---

## Installation

Clone the repository:

```bash
git clone <your-repository-url>
cd <repository-name>
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate it.

Windows:

```bash
.venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Running the API

Start the server:

```bash
uvicorn main:app --reload
```

The API will be available at:

```
http://127.0.0.1:8000
```

Interactive Swagger documentation:

```
http://127.0.0.1:8000/docs
```

---

## API Endpoints

| Method | Endpoint         | Description       |
| ------ | ---------------- | ----------------- |
| GET    | /                | API information   |
| GET    | /health          | Health check      |
| GET    | /tasks           | Get all tasks     |
| GET    | /tasks/{task_id} | Get a task by ID  |
| POST   | /tasks           | Create a new task |
| PUT    | /tasks/{task_id} | Update a task     |
| DELETE | /tasks/{task_id} | Delete a task     |

---

## Example Request

Create a task:

```bash
curl -i -X POST http://127.0.0.1:8000/tasks ^
-H "Content-Type: application/json" ^
-d "{\"title\":\"Study FastAPI\"}"
```

Example response:

```
HTTP/1.1 201 Created

{
    "id": 4,
    "title": "Study FastAPI",
    "done": false
}
```

---

## Swagger UI

Open:

```
http://127.0.0.1:8000/docs
```
<img width="1297" height="633" alt="image" src="https://github.com/user-attachments/assets/a3fc4077-8413-408b-beba-c9d1c628b0fb" />

---

## Notes

* Tasks are stored in memory.
* Restarting the server resets the task list because no database is used.


