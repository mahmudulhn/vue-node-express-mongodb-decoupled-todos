# Node.js Express MongoDB Todo REST API

## Project Overview
This project is a REST API for managing todo items. It allows users to perform CRUD (Create, Read, Update, Delete) operations on a todo list. The API is built using Node.js with the Express framework, and it uses MongoDB for data storage.

## Technologies Used
- **Node.js**: A JavaScript runtime built on Chrome's V8 JavaScript engine.
- **Express.js**: A minimal and flexible Node.js web application framework.
- **MongoDB**: A NoSQL database program that uses JSON-like documents with optional schemas.
- **Mongoose**: An ODM (Object Data Modeling) library for MongoDB and Node.js.
- **cors**: A Node.js package for providing a Connect/Express middleware that can be used to enable CORS with various options.

## Project Structure

```

node-express-mongodb-todo-rest-api/
├── controllers/
│ └── todos.controller.js # Controller for handling todo-related logic
├── data/
│ └── database.js # MongoDB connection setup
├── middlewares/
│ └── cors.js # Middleware for handling CORS
├── models/
│ └── todo.model.js # Mongoose model for todo items
├── routes/
│ └── todos.routes.js # Routes for todo API endpoints
├── app.js # Main application file
├── package.json # Project metadata and dependencies
├── package-lock.json # Dependency tree
└── README.md # Project documentation

```


## API Endpoints
- **GET /todos**: Retrieve all todo items.
- **POST /todos**: Create a new todo item.
- **GET /todos/:id**: Retrieve a specific todo item by ID.
- **PUT /todos/:id**: Update a specific todo item by ID.
- **DELETE /todos/:id**: Delete a specific todo item by ID.

## Example Usage
To create a new todo item, send a POST request to `http://localhost:3000/todos` with a JSON body like:
```json
{
  "title": "Buy groceries",
  "description": "Milk, Bread, Cheese",
  "completed": false
}

```

To retrieve all todo items, send a GET request to `http://localhost:3000/todos`.

## Source Code Details

- **app.js**: The entry point of the application. It sets up the Express server, middleware, and routes.
- **controllers/todos.controller.js**: Contains the logic for handling requests and responses for todo items.
- **data/database.js**: Configures and establishes the connection to the MongoDB database.
- **middlewares/cors.js**: Configures CORS settings to allow cross-origin requests.
- **models/todo.model.js**: Defines the schema for todo items using Mongoose.
- **routes/todos.routes.js**: Defines the API endpoints and links them to the corresponding controller functions.

## Additional Notes

- Ensure to have MongoDB installed and running locally, or configure the connection string to connect to a remote MongoDB instance.
- Use tools like Postman or curl to test the API endpoints.
