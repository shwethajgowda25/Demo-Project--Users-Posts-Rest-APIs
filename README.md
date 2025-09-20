# User & Post Management REST API
# Project Description
This project implements a **RESTful API** for managing user accounts and their associated posts. Developed using **Spring Boot and Gradle**, it provides a robust backend solution for applications requiring user and content management. The API adheres to REST principles, offering clear and predictable endpoints for performing CRUD (Create, Read, Update, Delete) operations on both User and Post entities.

# Features
# User Management:
  * Create new user accounts.
  * Retrieve user details by ID or list all users.
  * Update existing user information.
  * Delete user accounts.

# Post Management:
  * Create posts, associating them with a specific user.
  * Retrieve post details by ID or list all posts.
  * Retrieve all posts for a specific user.
  * Update existing post content.
  * Delete posts.

# RESTful Design: 
Adheres to standard HTTP methods and status codes for intuitive API interaction.

# Validation: 
Basic input validation to ensure data integrity.

# Embedded Database: 
Uses an in-memory database (e.g., Map) for easy setup and development.

# Built with Gradle: 
Leverages Gradle for efficient dependency management and build automation.

# Technologies Used
Language: Java 17+
Framework: Spring Boot 3.x
Build Tool: Gradle
Database: RAM Database (in-memory, for development)

# Testing: 
JUnit 5, Mockito

# API Documentation: 
(Potentially integrates with OpenAPI/Swagger for interactive documentation if added)

# Getting Started
Follow these instructions to get a copy of the project up and running on your local machine for development and testing purposes.

**Prerequisites**
Before you begin, ensure you have the following installed:

**Java Development Kit (JDK)**: Version 17 or higher.
**Git**: For cloning the repository.
(Optional) IDE: Eclipse.

# Running the Application
**Clone the repository**: git clone https://github.com/shwethajgowda25/Demo-Project--Users-Posts-Rest-APIs.git
**Navigate to the project directory**: cd Demo-Project--Users-Posts-Rest-APIs
**Build and run the application using Gradle**: ./gradlew bootRun

The application will start on http://localhost:8080 by default.

# API Endpoints
The API provides the following endpoints for interacting with User and Post resources.
Base URL: **http://localhost:8080**

**Users Endpoint**:
<img width="1651" height="447" alt="access this public github repository _https___git  - Google Sheets - Google Chrome 9_20_2025 1_12_03 PM" src="https://github.com/user-attachments/assets/51c9befc-dfb9-4c72-8756-efe4ce39deb2" />

**Posts Endpoint** :
<img width="1587" height="507" alt="access this public github repository _https___git  - Google Sheets - Google Chrome 9_20_2025 1_18_18 PM" src="https://github.com/user-attachments/assets/b5eb6fc6-aef1-4555-a886-6370d999ba3b" />




