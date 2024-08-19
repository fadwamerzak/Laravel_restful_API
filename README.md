<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

# 🚀 Laravel RESTful API

## 📄 Description
This project is a RESTful API built with Laravel, designed to manage a list of products. The API includes endpoints for creating, retrieving, updating, and deleting products. The database interactions are handled using Laravel's Eloquent ORM, and the API has been tested using Postman.

## ✨ Features
- **CRUD Operations**: Create, Read, Update, and Delete products.
- **Validation**: Server-side validation for product data.
- **Resourceful Responses**: Structured JSON responses using Laravel Resources.
- **Error Handling**: Comprehensive error handling with appropriate HTTP status codes.

## 🛠️ Installation

### Prerequisites
- PHP 8.x
- Composer
- MySQL
- Laravel 9.x

## 📦 Usage

### Testing with Postman
You can test the API endpoints using Postman:

1. **GET** `/api/products`: Retrieve all products.
2. **POST** `/api/products`: Create a new product.
3. **GET** `/api/products/{id}`: Retrieve a product by its ID.
4. **PUT** `/api/products/{id}`: Update a product by its ID.
5. **DELETE** `/api/products/{id}`: Delete a product by its ID.

### 🔗 Available Endpoints

#### 1. **GET** `/api/products`
   - Retrieves a list of all products.
   - Example response:
     ```json
     [
        {
            "id": 1,
            "name": "Apple",
            "description": "this is apple description",
            "price": 0,
            "created_at": "2024-07-10T15:44:30.000000Z"
        },
        {
            "id": 2,
            "name": "Mango",
            "description": "this is mango description",
            "price": 0,
            "created_at": "2024-07-10T15:51:20.000000Z"
        }
     ]
     ```

#### 2. **POST** `/api/products`
   - Creates a new product.
   - Example request:
     ```json
     {
        "name": "fadwa",
        "description": "this is fadwa description",
        "price": 100
     }
     ```
   - Example response:
     ```json
     {
        "message": "Product created successfully",
        "data": {
            "id": 4,
            "name": "fadwa",
            "description": "this is fadwa description",
            "price": null,
            "created_at": "2024-08-19T17:11:09.000000Z"
        }
     }
     ```

#### 3. **GET** `/api/products/1`
   - Retrieves a specific product by ID.
   - Example response:
     ```json
     {
        "data": {
            "id": 1,
            "name": "Apple",
            "description": "this is apple description",
            "price": 0,
            "created_at": "2024-07-10T15:44:30.000000Z"
        }
     }
     ```

#### 4. **PUT** `/api/products/2`
   - Updates a specific product by ID.
   - Example request:
     ```json
     {
        "name": "hiba",
        "description": "this is hiba description",
        "price": 111
     }
     ```
   - Example response:
     ```json
     {
        "message": "Product updated successfully",
        "data": {
            "id": 2,
            "name": "hiba",
            "description": "this is hiba description",
            "price": 0,
            "created_at": "2024-07-10T15:51:20.000000Z"
        }
     }
     ```

#### 5. **DELETE** `/api/products/2`
   - Deletes a specific product by ID.
   - Example response:
     ```json
     {
         "message": "Product deleted successfully"
     }
     ```
