# 🛒 Store API Testing — Assignment #4

> University QA Training Assignment — API Testing with FakeStoreAPI

---

## 📌 Overview

This repository contains a hands-on API testing assignment completed as part of a university QA (Quality Assurance) training program. The goal was to practice testing a RESTful e-commerce API by designing and executing test cases that validate various endpoints and behaviors of the [Fake Store API](https://fakestoreapi.com/).

---

## 📁 Repository Structure

```
Store-API-test/
└── Assignment#4/       # Test cases, test plan, and related files
```

---

## 🌐 API Under Test

**Base URL:** `https://fakestoreapi.com`

The Fake Store API is a free, publicly available REST API that simulates an e-commerce store backend. It provides endpoints for:

| Resource    | Endpoint             |
|-------------|----------------------|
| Products    | `/products`          |
| Categories  | `/products/categories` |
| Carts       | `/carts`             |
| Users       | `/users`             |
| Auth/Login  | `/auth/login`        |

---

## 🧪 What Was Tested

The assignment covers testing across the following areas:

- **GET requests** — Retrieving products, users, and cart data
- **POST requests** — Adding new products and user login
- **PUT / PATCH requests** — Updating existing resources
- **DELETE requests** — Removing products or cart items
- **Status code validation** — Verifying correct HTTP responses
- **Response body validation** — Checking structure and data accuracy
- **Edge cases** — Invalid IDs, missing fields, unauthorized requests

---

## 🛠️ Tools & Technologies

- **Postman** — API request execution and collection management
- **Manual Testing** — Test case design and execution

---

## ▶️ How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/dialashami/Store-API-test.git
   ```

2. Navigate to the assignment folder:
   ```bash
   cd Store-API-test/Assignment#4
   ```

3. Open any Postman collection files (`.json`) in Postman via **Import**.

4. Run the collection or execute individual requests against `https://fakestoreapi.com`.

---

## 👤 Author

**Dia Lashami**  
University QA Training Program  
[GitHub Profile](https://github.com/dialashami)

---

## 📄 License

This project is for educational purposes only.
