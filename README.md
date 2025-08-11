# intern-project-task3

## Overview

This project is a simple **Book Management REST API** built with Node.js and Express. It demonstrates basic CRUD (Create, Read, Update, Delete) operations for managing a collection of books using an in-memory data store. The API is designed for educational purposes or as a boilerplate for more complex RESTful backend projects.

## Features

- **Get all books:** Retrieve a list of all books.
- **Get book by ID:** Retrieve details for a specific book.
- **Create book:** Add a new book to the collection.
- **Update book:** Edit details of an existing book.
- **Delete book:** Remove a book from the collection.

## Technologies Used

- [Node.js](https://nodejs.org/)
- [Express](https://expressjs.com/)

## Getting Started

### Prerequisites

- Node.js installed (v14 or above recommended)
- npm (comes with Node.js)

### Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/Kunal-Rawat1294/intern-project-task3.git
    cd intern-project-task3
    ```
2. Install dependencies:
    ```bash
    npm install
    ```

### Running the Application

Start the Express server:
```bash
node app.js
```
The server will start at `http://localhost:3000`.

## API Endpoints

| Method | Endpoint         | Description               |
|--------|------------------|---------------------------|
| GET    | `/`              | Welcome message & endpoints list |
| GET    | `/books`         | Get all books             |
| GET    | `/books/:id`     | Get a single book by ID   |
| POST   | `/books`         | Create a new book         |
| PUT    | `/books/:id`     | Update an existing book   |
| DELETE | `/books/:id`     | Delete a book             |

### Example Book Object

```json
{
  "id": 1,
  "title": "To Kill a Mockingbird",
  "author": "Harper Lee"
}
```

### Sample Requests

- **Create a Book**
    ```http
    POST /books
    Content-Type: application/json

    {
      "title": "New Book Title",
      "author": "Author Name"
    }
    ```

- **Update a Book**
    ```http
    PUT /books/1
    Content-Type: application/json

    {
      "title": "Updated Title"
    }
    ```

- **Delete a Book**
    ```http
    DELETE /books/1
    ```

## Notes

- The books are stored in memory; data will reset if the server restarts.
- For production use, integrate a persistent database.

## License

This project is open source and available under the [MIT License](LICENSE).

## Author

[Kunal Rawat](https://github.com/Kunal-Rawat1294)
