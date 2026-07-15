# Chapter 4 - System Design

## Purpose of this Chapter

The purpose of this chapter is to define the overall system design of the BookVerse application. 
It describes the architecture, major system components, module organization, request flow, backend and frontend structures, 
and design principles that will be followed during development. This chapter serves as the blueprint for implementing the application 
in a structured and maintainable manner.

## Chapter Overview

This chapter describes how the BookVerse application is designed from a high-level perspective. It explains the overall system architecture,
software components, module organization, backend and frontend structures, request processing flow, package organization, and software design 
principles that guide the implementation of the project.

## 4.1 System Architecture

BookVerse follows a three-tier architecture consisting of the Presentation Layer, Business Logic Layer, and Data Layer.

- The Presentation Layer is developed using Angular and provides the user interface.
- The Business Logic Layer is developed using Spring Boot and contains the application's business rules and REST APIs.
- The Data Layer uses MySQL to store and manage application data.

This architecture promotes scalability, maintainability, and separation of concerns by keeping each layer independent of the others.

## 4.2 Architecture Style

The BookVerse application follows a layered architecture combined with a client-server architecture.

### Layered Architecture

The backend is divided into multiple layers:

- Controller Layer
- Service Layer
- Repository Layer
- Database Layer

Each layer has a specific responsibility, making the application easier to maintain and extend.

### Client-Server Architecture

The Angular frontend acts as the client and communicates with the Spring Boot backend through RESTful APIs using HTTP requests and JSON responses.

## 4.3 System Components

The major components of the BookVerse application are:

### Frontend

- Angular
- TypeScript
- Bootstrap
- Angular Router
- HttpClient

### Backend

- Spring Boot
- Spring Security
- Spring Data JPA
- Hibernate

### Database

- MySQL

### Development Tools

- IntelliJ IDEA
- VS Code
- Postman
- Git
- GitHub

## 4.4 Module Design

The BookVerse application is divided into the following modules:

- Authentication Module
- User Management Module
- Book Management Module
- Category Management Module
- Author Management Module
- Publisher Management Module
- Shopping Cart Module
- Order Management Module
- Admin Dashboard Module

Each module is developed independently while maintaining communication through the application's service layer.

## 4.5 Backend Architecture

The backend follows Spring Boot's layered architecture.

Presentation Layer

- REST Controllers

Business Layer

- Services

Persistence Layer

- Repositories

Database Layer

- MySQL

Controllers receive HTTP requests, services process business logic, repositories interact with the database, and MySQL stores application data.

## 4.6 Frontend Architecture

The frontend is developed using Angular.

The application consists of:

- Components
- Services
- Models
- Guards
- Interceptors
- Routing Module
- Shared Components

Angular communicates with the backend through REST APIs using the HttpClient module.


## 4.7 Request Flow

The request processing flow is as follows:

1. The user performs an action on the Angular application.
2. Angular sends an HTTP request to the Spring Boot REST API.
3. The controller receives the request.
4. The controller forwards the request to the service layer.
5. The service layer executes the required business logic.
6. The repository accesses the MySQL database.
7. The database returns the requested data.
8. The repository sends the data back to the service.
9. The service returns the processed data to the controller.
10. The controller returns a JSON response to Angular.
11. Angular updates the user interface.

## 4.8 Package Structure

The backend project follows the package structure below:

com.bookverse

- config
- controller
- dto
- entity
- exception
- repository
- security
- service
- util

Each package has a specific responsibility, ensuring a clean and maintainable project structure.

## 4.9 Design Principles

The BookVerse project follows the following software design principles:

- Separation of Concerns (SoC)
- Single Responsibility Principle (SRP)
- Dependency Injection (DI)
- Layered Architecture
- Reusability
- Maintainability
- Scalability
- Clean Code Practices

These principles improve code quality, reduce coupling, and make the application easier to maintain and extend.

## 4.10 Chapter Summary

This chapter defined the overall system design of the BookVerse application. It described the application architecture, major software components,
module organization, backend and frontend structures, request flow, package organization, and software design principles that will guide
the implementation of the project.
