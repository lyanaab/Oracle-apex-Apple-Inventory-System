# 🍎 Apple Inventory System  
### Enterprise Inventory & Order Management System – Oracle APEX

---

## 📌 About The Application

Apple Inventory System is a full-stack web application built using **Oracle APEX** to manage products, inventory, customers, and sales orders in a structured enterprise-style environment.

The system simulates a real-world inventory and order management solution where administrators can:

- Manage product catalog and categories
- Track stock levels in real time
- Create multi-step sales orders
- Monitor order statuses
- Analyze sales and inventory performance
- Manage admin users and internal notes
- Integrate external exchange rate APIs

This project demonstrates strong knowledge in:

- Relational Database Design
- Oracle SQL & PL/SQL
- Oracle APEX Page Development
- Business Logic Implementation
- REST API Integration
- Reporting & Data Visualization

---

## 🚀 Application Features

### 📊 Dashboard
- Summary cards (products, orders, customers)
- Status overview
- System metrics

### 📦 Product Management
- Products Report (Interactive Report)
- Product Form (Create / Update / Delete)
- Product Image Details
- Products by Category View

### 🗂️ Category Management
- Categories Report
- Create New Category

### 👥 Customer Management
- Customers Report
- Customer Form (CRUD Operations)

### 🛒 Order Management (Wizard-Based Flow)

Multi-step order creation process:

1. Choose Customer  
2. Add Items (Cart Logic)  
3. Review & Confirm  
4. Finish & Update Order Status  

Additional order features:
- Order Details Page
- Change Order Status
- Status + Customer Filters
- Date Range Filtering

### 📈 Analytics & Reports
- Inventory Valuation
- Orders Analysis
- Category-based statistics
- Date-based filtering

### 🌍 Exchange Rates Integration
- REST API integration
- External currency data retrieval

### 🔐 Security & Administration
- Login Page
- Admin Users Management
- Internal Admin Notes

---

## 🗄️ Database Design

The system is built using a fully normalized relational schema with proper constraints and relationships.

### Main Tables

#### 1️⃣ Categories
- `category_id` (Primary Key)
- `category_name` (Unique)
- `description`

#### 2️⃣ Products
- `product_id` (Primary Key)
- `name`
- `description`
- `category_id` (Foreign Key → Categories)
- `unit_price`
- `stock_quantity`
- `image_url`

#### 3️⃣ Customers
- `customer_id` (Primary Key)
- `name`
- `email`
- `phone`
- `address`

#### 4️⃣ Orders
- `order_id` (Primary Key)
- `customer_id` (Foreign Key → Customers)
- `order_date`
- `status`
- `total_amount`

#### 5️⃣ Order_Items
- `order_item_id` (Primary Key)
- `order_id` (Foreign Key → Orders)
- `product_id` (Foreign Key → Products)
- `quantity`
- `unit_price`

#### 6️⃣ Admin_Users
- Stores system administrators

#### 7️⃣ Admin_Notes
- Stores internal system notes

---

## 🔗 Relationships

- One Category → Many Products  
- One Customer → Many Orders  
- One Order → Many Order Items  
- One Product → Many Order Items  

All relationships are enforced using **Foreign Key Constraints**.

No database triggers are used.  
All business logic is implemented inside Oracle APEX processes.

---

## 🏗️ System Architecture

### 1️⃣ Database Layer
- Relational schema
- Identity columns
- Check constraints
- Foreign key enforcement

### 2️⃣ Application Logic Layer
- APEX Processes
- PL/SQL blocks
- Dynamic Actions
- Session State management

### 3️⃣ Presentation Layer
- Interactive Reports
- Forms
- Wizard Pages
- Cards
- Charts
- Filters

---

## 📂 Project Structure

| File | Description |
|------|------------|
| `database_Schema.sql` | Database tables, constraints, and seed data |
| `application_export.sql` | Full Oracle APEX application export |
| `README.md` | Project documentation |

---

## 🛠️ How to Run the Project

1. Import `database_Schema.sql` into Oracle Database.
2. Import `application_export.sql` into Oracle APEX.
3. Run the application from APEX App Builder.

---

## 🎓 Academic Context

Developed as part of a Database Systems and Oracle APEX academic project.  
The system demonstrates enterprise-style database application development without using database triggers, keeping business logic inside the APEX layer.
