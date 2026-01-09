## FastAPI Customer Management API

A simple Customer Management REST API built using FastAPI, following a clean layered architecture (Controller → Service → Repository → Model).
This project demonstrates CRUD operations using in-memory storage.

## 📌 Features

-Create a new customer

-Retrieve all customers

-Retrieve a customer by ID

-Update customer details

-Delete a customer

-Proper HTTP status codes and error handling

-Clean separation of concerns (Service & Repository pattern)


## 🏗 Project Architecture
```
project/
│
├── controller.py           # FastAPI application (API layer)
├── Customer.py             # Customer model (dataclass)
├── Services.py             # Business logic layer
├── repo.py                 # Repository / data access layer
└── README.md               # Project documentation

```

## 🧱 Tech Stack

-Python 3.9+
-FastAPI
-Uvicorn
-Dataclasses

## 📄 Customer Model
```
@dataclass
class Customer:
    id: int
    name: str
    email: str
    active: bool
```

## 🚀 API Endpoints

➕ Create Customer

POST /customers/
```
{
  "id": 1,
  "name": "John Doe",
  "email": "john@example.com",
  "active": true
}
```
Response: 201 Created

## 📄 Get All Customers

-GET /customers/

## 🔍 Get Customer by ID

-GET /customers/{customer_id}

-404 if customer not found

## ✏ Update Customer

PUT /customers/{customer_id}
```
{
  "id": 1,
  "name": "John Updated",
  "email": "john.updated@example.com",
  "active": false
}
```
-400 if ID mismatch

-404 if customer not found

🗑 Delete Customer

-DELETE /customers/{customer_id}

-404 if customer not found

## ▶ Running the Application

1️⃣ Install Dependencies
```
pip install fastapi uvicorn
```

2️⃣ Start the Server
```
uvicorn main:app --reload
```
3️⃣ Open Swagger UI 
```
http://127.0.0.1:8000/docs
```

## 🧠 Design Patterns Used

-Service Layer Pattern

-Repository Pattern

-Dependency Separation

-RESTful API Design

## ⚠ Notes

-Uses in-memory storage (data resets on restart)

-Suitable for learning, interviews, and prototyping

-Can be extended with:

-Database (PostgreSQL / MySQL)

-SQLAlchemy

-Pydantic models

-Authentication (JWT)

## 📌 Future Enhancements

-Persistent database integration

-Validation using Pydantic schemas

-Pagination & filtering

-Unit testing with Pytest

-Docker support

👤 Author

Raj Mohan R
Python | FastAPI | Backend Development
