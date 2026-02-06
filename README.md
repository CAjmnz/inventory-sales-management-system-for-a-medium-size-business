# Inventory & Sales Management System
**CodeIgniter 4 + MySQL**

A web-based inventory and sales management system designed for retail and distribution companies.  
This system focuses on **data integrity, role-based access control, and scalability**, with a REST API layer for future integrations such as POS systems or mobile applications.

---

## 📌 Project Purpose
This project was built to simulate a **real-world retail environment**, focusing on how businesses manage:
- Products and inventory
- Sales transactions
- User roles and permissions
- Reporting and audit logs

The goal is to demonstrate **production-ready backend development skills** using CodeIgniter 4.

---

## 🚀 Features

### 🔐 Authentication & Authorization
- Secure login system
- Role-Based Access Control (RBAC)
  - **Admin** – full system access
  - **Manager** – reports and inventory monitoring
  - **Staff** – sales operations only

### 📦 Inventory Management
- Product and category management
- Stock in / stock out operations
- Low-stock validation
- Soft delete support for products

### 💰 Sales Module
- Sales recording with itemized products
- Automatic stock deduction
- Database transactions to ensure data integrity
- Prevention of negative stock levels

### 📊 Reports & Dashboard
- Daily, weekly, and monthly sales reports
- Inventory summary
- Top-selling products

### 🧾 Audit Logging
- Logs critical system actions such as:
  - Stock adjustments
  - Sales transactions
  - User activity

### 🔌 REST API (Secured)
- API endpoints for:
  - Products
  - Sales
  - Reports
- Token-based authentication
- Role-based access enforcement

---

## 🧰 Tech Stack
- PHP 8+
- CodeIgniter 4
- MySQL
- Bootstrap
- REST API (JSON)
- Git & GitHub

---

## 🧠 System Architecture
The system follows the **MVC architecture** provided by CodeIgniter 4, enhanced with additional layers:

- **Controllers** – Handle HTTP requests and responses
- **Services** – Contain business logic (e.g., sales processing, stock updates)
- **Models** – Handle database interactions
- **Filters** – Enforce authentication and role-based authorization

This structure ensures:
- Clean separation of concerns
- Maintainable and scalable codebase

---

## 🗄️ Database Design
Key tables include:
- `users`
- `categories`
- `products`
- `sales`
- `sale_items`
- `audit_logs`

An Entity Relationship Diagram (ERD) is provided in the `/docs` folder.

---

🔌 REST API Overview
Authentication
POST /api/login


Authenticates users and returns an access token

Products
GET /api/products


Retrieves the list of products

Sales
POST /api/sales


Records a sales transaction

Automatically updates product stock

Reports
GET /api/reports/daily


Returns daily sales summary

Accessible by Admin and Manager roles only

GET /api/reports/monthly


Returns monthly sales summary

Accessible by Admin and Manager roles only

GET /api/reports/low-stock


Returns products below the stock threshold

Accessible by Admin and Manager roles only

All API endpoints:

Return JSON responses

Require authentication tokens

Enforce role-based permissions

⚙️ Installation & Setup
Requirements

PHP 8+

MySQL

Composer

Apache or Nginx

Setup Steps

Clone the repository

git clone https://github.com/yourusername/inventory-sales-ci4.git


Navigate to the project directory

cd inventory-sales-ci4


Copy environment configuration

cp env .env


Update .env with database credentials

Create the database

Run migrations

php spark migrate


Start the development server

php spark serve

🔐 Security Considerations

Passwords are securely hashed

Role-based access control (RBAC) is enforced

Server-side input validation is applied

Critical operations use database transactions

API endpoints are protected with authentication tokens

📈 Future Improvements

POS system integration

Mobile application support

Advanced analytics and reporting

Performance optimization and caching

CI/CD pipeline implementation

👨‍💻 Author

Christian Augustus Jimenez
Computer Engineering Graduate
Aspiring Software Developer / Cybersecurity Professional

📄 License

This project is for educational and portfolio purposes only.
