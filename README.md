# ERD-Kiwilytics-Project
ERD for a sample relational database including Orders, Customers, Products, and Suppliers.

# 🗄️ Relational Database Schema

This repository contains an **Entity-Relationship Diagram (ERD)** showing how data is structured and connected in a sample relational database.

---

## 📊 Tables Overview

| Table | Primary Key | Foreign Keys |
|-------|--------------|--------------|
| **Categories** | CategoryID | — |
| **Customers** | CustomerID | — |
| **Employees** | EmployeeID | — |
| **Orders** | OrderID | CustomerID → Customers.CustomerID<br>EmployeeID → Employees.EmployeeID<br>ShipperID → Shippers.ShipperID |
| **Order_Details** | OrderLineID | OrderID → Orders.OrderID<br>ProductID → Products.ProductID |
| **Products** | ProductID | CategoryID → Categories.CategoryID<br>SupplierID → Suppliers.SupplierID |
| **Shippers** | ShipperID | — |
| **Suppliers** | SupplierID | — |

---

## 🗺️ ERD Diagram

![ERD Diagram](ERD_kiwilytics.webp)

---

## 💡 Description

This schema models a small retail or e-commerce database:
- **Customers** place **Orders**
- **Orders** are handled by **Employees** and shipped via **Shippers**
- Each order has multiple **Order_Details** referencing **Products**
- **Products** belong to **Categories** and are provided by **Suppliers**
