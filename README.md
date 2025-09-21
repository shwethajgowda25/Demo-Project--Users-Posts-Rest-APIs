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

# Cloud Deployment - GCP

Deploying a Spring Boot Gradle Java project to Google Cloud Platform (GCP) involves a few key steps. Fopr a stateless spring boot application I have used Cloud Run, as it's a serverless platform that handles containerization and scaling automatically. 
**Steps**:
1.** Preparing Project** ⚙️
First, need to prepare Spring Boot application for containerization. So prepared Dcokerfile. This file provides instructions for building a Docker image from the project.

2. **Google Cloud Setup** ☁️
Before deploying, GCP environment is set up.
**Installed the gcloud CLI**(This is the command-line interface for Google Cloud.)
Authentication: Ran **gcloud auth login** and "**gcloud config set project [YOUR_PROJECT_ID]**"
Enabled APIs: The **Cloud Run**, **Cloud Build**, and **Artifact Registry** APIs are enabled for the project

3. **Deploying to Cloud Run** 🚀
* Cloud Run can handle the containerization process for you using Cloud Buildpacks, which automatically create a container image from the source code.
* **Build and Deploy**: From the project's root directory and ran command:
   **"gcloud run deploy --source ."**
* Configuration: CLI prompted to choose a region, a service name, and whether to allow unauthenticated invocations.
* Build the executable JAR file.
* Created a container image from the JAR.
* Pushed the image to Artifact Registry.
* Deployed the container to Cloud Run.

This process handles the entire CI/CD pipeline from source code to a running service. Cloud Run then provides a URL for your deployed application.

**Accessing the API**
The API is deployed and publicly accessible via the following URL:
https://my-trase-demo-api-793270243363.us-central1.run.app

**Users Endpoint**:
https://my-trase-demo-api-793270243363.us-central1.run.app/users

**Posts Endpoint**:
https://my-trase-demo-api-793270243363.us-central1.run.app/posts

The http methods and POST/PUT request body is same as mentioned above. Used Insomnia to test the endpoints.

**Other setups and Challenges performed to support GCP deployment:**
1. Enabling Virtualization in windows
2. In local after first deployment, when had to make some more changes in code and do rebuild and deployment, faced issue where gradle refresh had issues from eclipse, refresh failed as gradle process was denied permission to read or write into files due to file locks.
   **Solution** : Had to delete the caches folder, stopped all the java tasks from task maanger and restarted the PC to remove this locking.
