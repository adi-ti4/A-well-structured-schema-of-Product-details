# A-well-structured-schema-of-Product-details

**Project Management**
This SQL project implements a relational database system for managing products and customer orders in a retail or inventory environment. 
It is built using MySQL, It is designed with a well-structured schema that separates product details from order transactions to ensure data integrity, flexibility, and scalability.

**Objectives of the project:**
Store and manage product information by category, name, and price.

Record customer orders including quantity, pricing, and total bill.

Maintain referential integrity using primary and foreign key constraints.

Enable easy data retrieval for reporting and analytics (e.g., total sales, product category performance).

**Core Components:**
Database Name: product_management

Tables: Tables created are Product and Orders

--> product
Stores master data about products.

Columns: 
Prod_Id(Primary Key), Prod_category, Prod_name, Price

--> Orders
Stores transactional data about customer purchases.

Columns: 
Ord_Id(Primary Key), Prod_Id (Foreign Key), Quantity, Price, Amount

--> Relationships:
Product ↔ Orders
Orders.Prod_Id is a foreign key referencing product.Prod_Id

Relationship Type: One-to-Many

One product can appear in many orders, but each order line refers to one product.

--> Foreign Key used:
Orders.Prod_Id → Product.Prod_Id
