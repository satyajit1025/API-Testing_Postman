# DummyJSON API Testing with Postman

This repository contains Postman collections and test scripts for testing the [DummyJSON](https://dummyjson.com) API. The goal is to validate CRUD operations (Create, Read, Update, Delete) on product resources and assert response attributes such as status codes and body content.

---

## API Base URL
https://dummyjson.com 

---

## Features Tested

### ✅ GET - Fetch All Products

- **Endpoint**: `/products`
- **Description**: Retrieves a list of all products.
- **Assertions**:
  - Status code is `200`
  - Status code name has string `OK`

---

### ✅ GET - Fetch Product by ID

- **Endpoint**: `/products/id`
- **Description**: Retrieves a single product using its ID.
- **Assertions**:
  - Status code is `200`
  - Response body includes expected data fields (e.g., title, price, etc.)

---

### ✅ GET - Filter with Query Parameters

- **Endpoint**: `/products/search?q=query`
- **Description**: Searches for products based on the query string.
- **Assertions**:
  - Status code is `200 OK`
  - Response body contains matching product

---

### ✅ POST - Create New Product

- **Endpoint**: `/products/add`
- **Description**: Creates a new product using a POST request.
- **Request Body Example**:
```json
{
  "title": "Wireless Headphones",
  "price": 129,
  "description": "Noise-cancelling over-ear headphones",
  "category": "audio"
}
```
- **Assertions**:
  - Status code is `201`
  - Updated fields reflect in response

---

### ✅ DELETE - Remove Product

- **Endpoint: /products/id**
- **Description**: Deletes the product with the given ID.
- **Assertions**:
  - Status code is `200`
  - Response confirms deletion

---

## Assertions and Validations
**Each request is tested using Postman test scripts to validate**:
- ✅ Status Code (e.g., 200, 201, 404)
- ✅ Content-Type is application/json
- ✅ Response body includes expected data fields (e.g., title, price, etc.)
