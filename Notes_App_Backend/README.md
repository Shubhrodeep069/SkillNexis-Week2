# Notes App Backend 🔐

A RESTful backend API for a notes-taking application built using Node.js, Express.js, and MongoDB. The application supports user registration, login, JWT authentication, and secure CRUD operations for personal notes.

## 🚀 Features

* User registration and login
* Password hashing using bcryptjs
* JWT-based authentication
* Create, read, update, and delete notes
* MongoDB database integration using Mongoose
* Users can access and manage only their own notes
* Environment variables for sensitive configuration

## 🛠️ Tech Stack

* Node.js
* Express.js
* MongoDB Atlas
* Mongoose
* JSON Web Token (JWT)
* bcryptjs
* Thunder Client

## 📁 Project Structure

```
Notes_App_Backend/
├── middleware/
│   └── authMiddleware.js
├── models/
│   ├── User.js
│   └── Note.js
├── routes/
│   ├── authRoutes.js
│   └── noteRoutes.js
├── .env
├── .gitignore
├── package.json
└── server.js
```

## ⚙️ Installation and Setup

### 1. Clone the repository

```
git clone YOUR_GITHUB_REPOSITORY_URL
cd Notes_App_Backend
```

Replace `YOUR_GITHUB_REPOSITORY_URL` with your actual repository URL.

### 2. Install dependencies

```
npm install
```

### 3. Configure environment variables

Create a `.env` file in the project root:

```
MONGO_URI=your_mongodb_connection_string
PORT=5000
JWT_SECRET=your_long_random_secret
```

Replace the placeholder values with your own configuration. Never commit your `.env` file.

### 4. Start the server

```
npx nodemon server.js
```

The API will run at `http://localhost:5000` after a successful MongoDB connection.

## 🔑 API Endpoints

### Authentication

| Method | Endpoint             | Description              |
| ------ | -------------------- | ------------------------ |
| POST   | `/api/auth/register` | Register a new user      |
| POST   | `/api/auth/login`    | Log in and receive a JWT |

### Notes

All notes endpoints require a valid JWT in the `Authorization` header.

| Method | Endpoint         | Description             |
| ------ | ---------------- | ----------------------- |
| POST   | `/api/notes`     | Create a note           |
| GET    | `/api/notes`     | Retrieve all your notes |
| GET    | `/api/notes/:id` | Retrieve one note       |
| PUT    | `/api/notes/:id` | Update a note           |
| DELETE | `/api/notes/:id` | Delete a note           |

## 🧪 Testing with Thunder Client

1. Register a user using the registration endpoint.

2. Log in to obtain a JWT token.

3. Send the token in the `Authorization` header for notes requests:

   ```
   Authorization: Bearer YOUR_JWT_TOKEN
   ```

4. Test the create, read, update, and delete operations.

## 🔒 Security

* Passwords are hashed before storage.
* Protected endpoints require a valid JWT.
* Note queries are restricted to the authenticated user's ID.
* Environment variables are excluded from version control.

## 🎯 Learning Outcomes

This project demonstrates REST API development, database integration, password hashing, JWT authentication, middleware, and user-specific data access.

## 👨‍💻 Author

Add your name here.

## 📄 License

This project was developed for learning and internship purposes.
