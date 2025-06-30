---
layout: "default"
title: "Salary REST Service: Secure FastAPI API for Salary Data 🌐💼"
description: "REST service for salary viewing with JWT authentication. Built with FastAPI, Docker, and GitLab CI/CD. Access your salary data securely. 🚀💻"
---
# Salary REST Service: Secure FastAPI API for Salary Data 🌐💼

![GitHub release](https://img.shields.io/github/release/DrFrancisOmonefe/salary-rest-service.svg)
[![Releases](https://img.shields.io/badge/Releases-View%20Latest%20Releases-brightgreen)](https://github.com/DrFrancisOmonefe/salary-rest-service/releases)

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Testing](#testing)
- [Contributing](#contributing)
- [License](#license)

## Overview
The **Salary REST Service** is a secure API built with FastAPI that allows users to view salary data. It employs JWT authentication to ensure that only authorized users can access sensitive information. This service is designed to be robust, efficient, and easy to use, making it ideal for developers and organizations that need a reliable way to manage salary data.

For the latest releases, visit [here](https://github.com/DrFrancisOmonefe/salary-rest-service/releases).

## Features
- **Secure Access**: JWT authentication for user verification.
- **FastAPI**: Built on FastAPI for high performance and easy scalability.
- **RESTful Design**: Follows REST principles for intuitive API design.
- **Docker Support**: Easily deployable using Docker containers.
- **Testing Framework**: Includes testing with Pytest for reliability.
- **Documentation**: Auto-generated documentation using Swagger UI.

## Technologies Used
- **FastAPI**: A modern, fast web framework for building APIs with Python 3.6+ based on standard Python type hints.
- **JWT**: JSON Web Tokens for secure user authentication.
- **Docker**: Containerization for easy deployment and scalability.
- **Poetry**: Dependency management and packaging in Python.
- **Pytest**: A testing framework for Python that makes it easy to write simple and scalable test cases.

## Installation
To get started with the Salary REST Service, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/DrFrancisOmonefe/salary-rest-service.git
   cd salary-rest-service
   ```

2. **Install Dependencies**:
   If you are using Poetry, run:
   ```bash
   poetry install
   ```

3. **Set Up Environment Variables**:
   Create a `.env` file in the root directory and set the following variables:
   ```env
   SECRET_KEY=your_secret_key
   DATABASE_URL=your_database_url
   ```

4. **Run the Application**:
   Use the following command to start the FastAPI server:
   ```bash
   uvicorn main:app --reload
   ```

5. **Docker Deployment** (Optional):
   To run the application in a Docker container, use:
   ```bash
   docker build -t salary-rest-service .
   docker run -p 8000:8000 salary-rest-service
   ```

## Usage
After starting the application, you can access the API at `http://localhost:8000`. You can also visit the interactive API documentation at `http://localhost:8000/docs`.

### Authentication
To access protected routes, you need to obtain a JWT token. Use the `/token` endpoint to log in with your credentials. You will receive a token that you can use in the Authorization header for subsequent requests.

### Example Request
Here’s how to make a request to the API:

```bash
curl -X GET "http://localhost:8000/salaries" -H "Authorization: Bearer your_jwt_token"
```

## API Endpoints
### Authentication
- **POST /token**: Obtain a JWT token.
  - **Request Body**: 
    ```json
    {
      "username": "your_username",
      "password": "your_password"
    }
    ```

### Salary Data
- **GET /salaries**: Retrieve a list of salaries.
- **GET /salaries/{id}**: Retrieve a specific salary by ID.
- **POST /salaries**: Create a new salary entry.
- **PUT /salaries/{id}**: Update an existing salary entry.
- **DELETE /salaries/{id}**: Delete a salary entry.

## Testing
To ensure the application works as expected, run the tests using Pytest. Use the following command:
```bash
pytest
```

You can also run tests in a Docker container if you prefer.

## Contributing
Contributions are welcome! If you would like to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push your branch to your forked repository.
5. Open a pull request.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

For the latest releases, visit [here](https://github.com/DrFrancisOmonefe/salary-rest-service/releases).