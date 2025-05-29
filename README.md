# 📚 Bookstore Management System – Go (Golang) REST API

A simple yet scalable **Bookstore Management System** built in **Go (Golang)** using **MySQL**, **GORM**, and **Gorilla Mux**. This project showcases the development of a fully functional RESTful API with CRUD operations and a clean, modular project structure, designed for ease of maintenance and extensibility.

---

## 🚀 Features

- 📖 **CRUD Operations** for Book management:
  - `GET /books` – Retrieve all books
  - `GET /books/{id}` – Retrieve a specific book
  - `POST /books` – Add a new book
  - `PUT /books/{id}` – Update an existing book
  - `DELETE /books/{id}` – Remove a book

- 📦 Structured project layout following Go best practices.
- 🔁 JSON marshalling and unmarshalling for request and response payloads.
- 🛠️ Clean separation of concerns using Go packages for config, models, controllers, routes, and utilities.
- 🌐 Routing using **Gorilla Mux**.
- 🗃️ Persistent storage with **MySQL** and ORM with **GORM**.

---

## 🧱 Project Structure

bookstore/
├── cmd/
│   └── main/
│       └── main.go               # Application entry point
├── pkg/
│   ├── config/
│   │   └── app.go               # Database connection and configuration
│   ├── controllers/
│   │   └── book-controller.go   # Handler functions for each API endpoint
│   ├── models/
│   │   └── book.go              # Book model definition
│   ├── routes/
│   │   └── bookstore-route.go   # Route declarations and bindings
│   └── utils/
│       └── utils.go             # Utility functions (e.g., response formatting)

---

## 🧪 Technologies Used

- **Go (Golang)** – Backend programming language
- **MySQL** – Relational database for persistent storage
- **GORM** – ORM for Go to interact with MySQL
- **Gorilla Mux** – Router for building RESTful services
- **JSON** – Payload format for request/response
- **Modular architecture** – Clean, maintainable codebase following Go conventions

---

## 📘 Book Model

Each book entity contains the following fields:

```go
type Book struct {
    gorm.Model
    Name        string `gorm:"" json:"name"`
    Author      string `json:"author"`
    Publication string `json:"publication"`
}
```

---

## 💡 Future Improvements

Here are some features I'm planning to implement:

- ✅ **Pagination & Filtering** for large datasets
- 🔐 **Authentication and Authorization** (JWT-based login system)
- 🧪 **Unit and Integration Tests** with Go’s testing framework
- 🧾 **Swagger Documentation** for interactive API usage
- 📊 **Logging & Monitoring** with structured logs
- 🌍 **Docker Containerization** for portability and deployment
- 🧵 **Concurrent Requests Handling** improvements using goroutines and channels

---

## 🧠 Additional Feature Suggestions

To further enhance the project and demonstrate deeper backend engineering skills, consider adding:

- 📘 **Category and Inventory Management**
- 🧾 **Order and Invoice Generation APIs**
- 📦 **Import/Export Functionality** (CSV or JSON for book data)
- 🕒 **Audit Trails** for book record modifications
- 🛒 **User Book Wishlist or Cart System**
- 📈 **Dashboard Endpoint** with statistics (e.g., total books, top authors)

---

## 👨‍💻 How to Run Locally

1. **Clone the repo:**

```bash
git clone https://github.com/yourusername/bookstore.git
cd bookstore
```

2. **Configure MySQL:**
   - Create a database (e.g., `bookstore`)
   - Update the DSN in `pkg/config/app.go`

```go
dsn := "username:password@tcp(127.0.0.1:3306)/bookstore?charset=utf8mb4&parseTime=True&loc=Local"
```

3. **Run the project:**

```bash
go run cmd/main/main.go
```
