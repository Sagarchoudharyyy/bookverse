# Chapter 5 - Database Design

## Purpose of this Chapter

The purpose of this chapter is to design the relational database for the BookVerse application.
It identifies the entities, their attributes, relationships, primary keys, foreign keys, constraints, and normalization principles
that will be used to create a scalable and maintainable database. This database design serves as the foundation for the
Spring Data JPA entity models and the application's data management layer.

## Chapter Overview

This chapter presents the complete database design of the BookVerse application. It includes the database architecture,
entity identification, entity relationships, table structures, normalization, indexing strategy, business rules, and data integrity constraints. 
The database is designed to support efficient data storage, retrieval, and management while maintaining consistency and scalability.

## 5.1 Database Overview

BookVerse uses MySQL as its relational database management system. The database is designed using normalization principles to reduce redundancy and
maintain data consistency. Each table represents a business entity, and relationships between entities are established using foreign keys.

The database supports authentication, book management, shopping cart, order processing, and administration functionalities while maintaining 
scalability for future enhancements.

## 5.2 Entity Identification

The following entities have been identified for the BookVerse application:

| Entity | Description |
|---------|-------------|
| User | Stores customer and administrator information |
| Role | Stores user roles and permissions |
| Book | Stores book information |
| Category | Stores book categories |
| Author | Stores author details |
| Publisher | Stores publisher details |
| Cart | Stores customer shopping carts |
| Cart Item | Stores books added to a shopping cart |
| Order | Stores customer orders |
| Order Item | Stores books included in an order |
| Address | Stores customer delivery addresses |

## 5.3 Entity Relationship Diagram (ERD)

The complete Entity Relationship Diagram (ERD) will be designed after finalizing all database entities and their relationships.
The ERD will visually represent the relationships between tables and serve as the blueprint for creating JPA entity classes.

## 5.4 Table Design

The BookVerse database consists of the following tables:

- users
- roles
- books
- categories
- authors
- publishers
- carts
- cart_items
- orders
- order_items
- addresses

Each table is designed to represent a specific business entity while maintaining normalization and data integrity.

## 5.5 Relationships

The database contains the following relationships:

- One Role can have many Users.
- One Category can contain many Books.
- One Author can write many Books.
- One Publisher can publish many Books.
- One User can have one Shopping Cart.
- One Shopping Cart can contain many Cart Items.
- One User can place many Orders.
- One Order can contain many Order Items.
- One User can have multiple Addresses.

## 5.6 Primary Keys and Foreign Keys

Every table contains a primary key to uniquely identify each record.

Relationships between tables are maintained using foreign keys.

Examples:

- role_id → users
- category_id → books
- author_id → books
- publisher_id → books
- user_id → carts
- cart_id → cart_items
- order_id → order_items

## 5.7 Database Constraints

The following constraints will be applied:

- Primary Key
- Foreign Key
- Unique Constraint
- Not Null Constraint
- Default Values
- Check Constraints (where applicable)

These constraints ensure data consistency and integrity throughout the application.

## 5.8 Normalization

The database follows normalization principles to reduce redundancy and improve maintainability.

The design satisfies:

- First Normal Form (1NF)
- Second Normal Form (2NF)
- Third Normal Form (3NF)

Normalization ensures that data is stored efficiently and avoids unnecessary duplication.

## 5.9 Indexing Strategy

Indexes will be created on frequently searched columns to improve query performance.

Examples include:

- email
- username
- book_title
- category_name
- order_date

## 5.10 Business Rules

The following business rules apply to the database:

- Every user must have one role.
- Every book belongs to one category.
- Every book has one author.
- Every book has one publisher.
- A customer cannot place an order without logging in.
- A cart belongs to only one customer.
- Order items cannot exist without an order.
- Book stock cannot be negative.

## 5.11 Chapter Summary

This chapter defined the database design for the BookVerse application. It identified the entities, relationships, constraints, 
normalization strategy, indexing plan, and business rules that will guide the implementation of the MySQL database and Spring Data JPA entity classes.
