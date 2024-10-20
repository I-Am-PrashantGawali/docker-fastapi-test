# FastAPI Docker Test

This repository contains a simple FastAPI application that has been dockerized. The application includes endpoints for managing user data, which is stored in a JSON file.

## Repository

[https://github.com/RohitPatil18/docker-fastapi-test](https://github.com/RohitPatil18/docker-fastapi-test)

## Overview

The FastAPI application provides the following endpoints:

### API Endpoints

| Method | Endpoint  | Description                                      |
|--------|-----------|--------------------------------------------------|
| GET    | `/`       | Returns a hello message                          |
| GET    | `/users`  | Returns a list of users stored in a JSON file   |
| POST   | `/users`  | Accepts and stores user data in a JSON file     |

## Running the Application

To find out more about running FastAPI applications, refer to the official documentation: [FastAPI Tutorial](https://fastapi.tiangolo.com/tutorial/first-steps/).

### Using Docker

This application can be run using Docker and Docker Compose. The application uses a `users.json` file located in the `data` directory to store user information. This file will be created automatically if it does not exist.

### Steps to Run

1. Build the Docker images:
   ```bash
   docker-compose build

2. Run the application:
   '''bash
   docker-compose up

3. Access the API documentation at: http://localhost:8000/users

### Data Persistence
After running the application, ensure to destroy the containers and recreate them to check if the previous data is still present. You can do this with the following commands:

1. Stop the application:
   '''bash
   docker-compose down

2. Recreate the containers:
   '''bash
   docker-compose up
   
This will help confirm that user data is persisted in the users.json file across container restarts.