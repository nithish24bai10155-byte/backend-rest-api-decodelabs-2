# backend-rest-api-decodelabs-2
# 🧠 Task Manager API

A simple, well-structured *backend REST API* built with *Node.js & Express, developed as **Project 2: Backend API Development* of the *DecodeLabs Full Stack Development — Industrial Training Kit (Batch 2026)*.

This project focuses on the "brain" of a full stack application — building robust API endpoints, handling data flow between client and server, and enforcing validation before any request reaches the data layer.

## 📌 Project Goal

> Develop a simple backend API to handle application logic — proving the ability to bridge the gap between user interaction and server-side processing through pure API logic.

## ✨ Features

- ✅ RESTful API design following proper naming conventions (resources are nouns, methods are verbs)
- ✅ GET and POST endpoints for managing tasks
- ✅ Server-side input validation ("never trust the client")
- ✅ Meaningful, semantic HTTP status codes (200, 201, 400, 404)
- ✅ Clean, consistent JSON request/response structure
- ✅ In-memory data store for quick local testing

## 🛠️ Tech Stack

| Layer     | Technology     |
|-----------|----------------|
| Runtime   | Node.js        |
| Framework | Express.js     |
| Data      | In-memory store (JSON) |

## 📂 Project Structure


task-manager-api/
├── server.js        # Main application & route logic
├── package.json      # Project metadata & dependencies
└── README.md


## 🚀 Getting Started

### 1. Clone the repository
bash
git clone https://github.com/<your-username>/task-manager-api.git
cd task-manager-api


### 2. Install dependencies
bash
npm install


### 3. Run the server
bash
npm start


The API will be running at http://localhost:3000

## 📡 API Endpoints

| Method | Endpoint            | Description                  |
|--------|----------------------|-------------------------------|
| GET    | /api/tasks         | Retrieve all tasks            |
| GET    | /api/tasks/:id     | Retrieve a single task by ID  |
| POST   | /api/tasks         | Create a new task             |

### Example — Get all tasks

GET /api/tasks

json
{
  "success": true,
  "count": 3,
  "data": [
    { "id": 1, "title": "Design API endpoints", "completed": true }
  ]
}


### Example — Create a task

POST /api/tasks
Content-Type: application/json

{
  "title": "Deploy to production"
}

json
{
  "success": true,
  "message": "Task created successfully",
  "data": { "id": 4, "title": "Deploy to production", "completed": false }
}


### Example — Validation error

POST /api/tasks
Content-Type: application/json

{}

json
{
  "success": false,
  "error": "Field \"title\" is required and must be a non-empty string."
}


## 🧪 Testing the API

You can test the endpoints using:
- *Postman* / *Insomnia* — import the routes above
- *cURL*
  bash
  curl http://localhost:3000/api/tasks
  
- *Thunder Client* (VS Code extension)

## 📚 Key Concepts Demonstrated

- Backend development & server-side logic
- RESTful API design principles
- Request/response data validation
- HTTP semantics (status codes, methods)

## 👩‍💻 Author

Built as part of the *DecodeLabs Full Stack Development Industrial Training Kit — Batch 2026*.

---
⭐ If you found this useful, consider giving the repo a star!
