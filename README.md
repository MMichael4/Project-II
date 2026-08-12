# 🛍️ Suzie Fashion – Relational Database Design (SQL)

## 📌 Project Overview
---
This project designs and implements a relational database for Suzie Fashion, a clothing retail business. The database models core business entities — products, customers, and orders — with proper normalization and referential integrity, forming the foundation for order management and sales tracking.



## 🧰 Tools & Technologies

---

SQL (MySQL-compatible syntax) – Database design & implementation
Relational database modeling – Primary keys, foreign keys, normalization

---

## 🗂️ Database Structure

Products

productID (Primary Key)
name, category, size, color, price
Stores catalog details for each clothing item

Customers

customerID (Primary Key)
name, phone, email
Stores customer contact information

Orders

orderID (Primary Key)
customerID (Foreign Key → Customers)
orderDate, totalAmount
Tracks individual customer orders

OrderDetails

Composite Primary Key: orderID + productID
orderID (Foreign Key → Orders)
productID (Foreign Key → Products)
quantity (defaults to 1)
Junction table resolving the many-to-many relationship between orders and products

---

## 🔗 Relationships

One customer can place many orders (Customers → Orders, one-to-many)
One order can include many products, and one product can appear in many orders (Orders ↔ Products, many-to-many via OrderDetails)

---

## 🧱 Key Design Concepts

Primary and foreign key constraints to enforce referential integrity
A composite key in OrderDetails to correctly model the many-to-many relationship
Sensible defaults (quantity DEFAULT 1) to simplify data entry
Normalized schema that avoids data duplication across products, customers, and orders

---

## 📁 Project Files

SuzieFashion.sql – Full schema creation script: builds the database and all four tables with their constraints and relationships

---

## 🚀 What This Project Demonstrates

Relational database design from a business scenario
Correct use of primary keys, foreign keys, and composite keys
Understanding of one-to-many and many-to-many relationships
Clean, normalized schema design as a foundation for future queries, reporting, or application development

---

## 👤 Author 
---
Michael Michael — BA | Data Analyst | SQL
