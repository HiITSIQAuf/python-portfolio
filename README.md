# Flask REST API

## Overview
This project provides a simple Flask-based REST API for managing users and tasks. It allows users to perform CRUD operations on both users and tasks.

## Features
- **User Management**:
  - Create a user
  - Get a list of users
  - Retrieve a specific user by ID
  - Update user details
  - Delete a user

- **Task Management**:
  - Create a task
  - Get a list of tasks
  - Update task details (mark as done or edit task description)
  - Delete a task

## Installation
1. Clone the repository:
   ```bash
   git clone <repository_url>
   cd <repository_folder>
   ```
2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install flask
   ```
4. Run the application:
   ```bash
   python app.py
   ```

## API Endpoints
### User Endpoints
- `GET /users` - Retrieve all users
- `GET /users/<id>` - Retrieve a single user by ID
- `POST /users` - Create a new user
- `PUT /users/<id>` - Update an existing user
- `DELETE /users/<id>` - Delete a user

### Task Endpoints
- `GET /tasks` - Retrieve all tasks
- `POST /tasks` - Create a new task
- `PUT /tasks/<id>` - Update an existing task
- `DELETE /tasks/<id>` - Delete a task

## Example Request
**Create a new user:**
```bash
curl -X POST http://127.0.0.1:5000/users -H "Content-Type: application/json" -d '{"name": "Alice", "email": "alice@example.com"}'
```

**Create a new task:**
```bash
curl -X POST http://127.0.0.1:5000/tasks -H "Content-Type: application/json" -d '{"task": "Finish project"}'
```

## License
This project is licensed under the MIT License.
