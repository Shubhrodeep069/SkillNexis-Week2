# To-Do List REST API

A simple REST API built using Node.js, Express.js, and MongoDB Atlas to create, retrieve, update, and delete tasks.

## Features

* Create new tasks
* Retrieve all tasks
* Retrieve a task by ID
* Update existing tasks
* Delete tasks
* Store task data in MongoDB Atlas
* Handle errors and validate required fields

## Technologies Used

* Node.js
* Express.js
* MongoDB Atlas
* Mongoose
* Thunder Client

## Project Structure

```text
to-do_rest/
├── models/
│   └── Task.js
├── .env
├── .gitignore
├── package.json
├── package-lock.json
├── README.md
└── server.js
```

## Installation and Setup

1. Install Node.js.

2. Clone or download this project.

3. Open the project folder in a terminal.

4. Install dependencies:

   ```bash
   npm install
   ```

5. Create a `.env` file and configure your MongoDB connection:

   ```env
   MONGO_URI=your_mongodb_connection_string
   PORT=5000
   ```

6. Start the server:

   ```bash
   npx nodemon server.js
   ```

The API runs at `http://localhost:5000`.

## API Endpoints

| Method | Endpoint         | Description           |
| ------ | ---------------- | --------------------- |
| POST   | `/api/tasks`     | Create a task         |
| GET    | `/api/tasks`     | Retrieve all tasks    |
| GET    | `/api/tasks/:id` | Retrieve a task by ID |
| PUT    | `/api/tasks/:id` | Update a task         |
| DELETE | `/api/tasks/:id` | Delete a task         |

## Sample Task

```json
{
  "title": "Complete SkillNexis Assignment",
  "description": "Build the To-Do REST API",
  "completed": false
}
```

## Testing

All API endpoints can be tested using Thunder Client in Visual Studio Code.

## Internship Assignment

**Program:** SkillNexis Internship
**Task:** To-Do List REST API
