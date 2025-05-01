# Golang Book Management System

## Overview
A RESTful API service built with Go for managing a bookstore's inventory. This system provides endpoints for creating, reading, updating, and deleting books in a database.

## Features
- CRUD operations for books
- Database integration
- RESTful API design
- JSON response format
- Modular architecture

## Technologies Used
- Go (Golang)
- Gorilla Mux (for routing)
- GORM (Object Relational Mapper)
- MySQL (database)
- JSON for data interchange

## Setup & Installation
1. Clone the repository
   ```bash
   git clone https://github.com/yourusername/golang-book-management-system.git
   ```

2. Navigate to the project directory
   ```bash
   cd golang-book-management-system
   ```

3. Install dependencies
   ```bash
   go mod download
   ```

4. Configure the database connection in `config/app.go`

5. Run the application
   ```bash
   go run main.go
   ```

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET    | /api/books | Get all books |
| GET    | /api/books/{id} | Get a specific book by ID |
| POST   | /api/books | Create a new book |
| PUT    | /api/books/{id} | Update a book |
| DELETE | /api/books/{id} | Delete a book |

## Database Schema

### Books Table
- `ID` (Primary Key)
- `Name` (string)
- `Author` (string)
- `Publication` (string)
- `CreatedAt` (timestamp)
- `UpdatedAt` (timestamp)

## Usage Examples

### Creating a Book

```bash
curl -X POST http://localhost:8080/api/books \
  -H "Content-Type: application/json" \
  -d '{"name": "The Great Gatsby", "author": "F. Scott Fitzgerald", "publication": "Scribner"}'
```

### Getting All Books

```bash
curl http://localhost:8080/api/books
```

### Getting a Specific Book

```bash
curl http://localhost:8080/api/books/1
```

### Updating a Book

```bash
curl -X PUT http://localhost:8080/api/books/1 \
  -H "Content-Type: application/json" \
  -d '{"name": "The Great Gatsby", "author": "F. Scott Fitzgerald", "publication": "Scribner"}'
```

### Deleting a Book

```bash
curl -X DELETE http://localhost:8080/api/books/1
```


## Contributing
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Author
Sarthak Jain