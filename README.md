# Habit Tracker API - A RESTful Solution for Habit Management 🚀

![Habit Tracker API](https://img.shields.io/badge/Habit%20Tracker%20API-v1.0.0-blue.svg)  
[![Release](https://img.shields.io/badge/Release%20Notes-v1.0.0-orange.svg)](https://github.com/GGD-github/habit-tracker-api/releases)

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the Application](#running-the-application)
- [API Documentation](#api-documentation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Overview

The Habit Tracker API is a backend REST API designed to help users track their personal habits. Built with Java and Spring Boot, it provides robust features to manage habits effectively. Users can create habits, check in regularly, calculate streaks, and authenticate securely.

For the latest releases, visit [Releases Section](https://github.com/GGD-github/habit-tracker-api/releases).

## Features

- **Habit Creation**: Easily create and manage personal habits.
- **Recurring Check-Ins**: Set up regular check-ins for habits.
- **Streak Calculations**: Track your progress with streak calculations.
- **User Authentication**: Secure user authentication using JWT.
- **API Documentation**: Clear and comprehensive API documentation using Swagger.

## Technologies Used

- **Java**: The primary programming language.
- **Spring Boot**: Framework for building the REST API.
- **Spring Security**: For secure user authentication.
- **JPA**: Java Persistence API for database interactions.
- **PostgreSQL**: Database for storing user and habit data.
- **Docker**: For containerization of the application.
- **Flyway**: Database migration tool.
- **Gradle**: Build automation tool.
- **Testcontainers**: For integration testing.
- **Swagger**: For API documentation.

## Getting Started

### Prerequisites

Before you begin, ensure you have the following installed:

- Java 11 or higher
- Docker
- PostgreSQL
- Gradle

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/GGD-github/habit-tracker-api.git
   cd habit-tracker-api
   ```

2. Configure your PostgreSQL database. Create a database named `habit_tracker`.

3. Update the `application.properties` file in `src/main/resources` with your database credentials.

### Running the Application

You can run the application using Docker or directly with Gradle.

#### Using Docker

1. Build the Docker image:
   ```bash
   docker build -t habit-tracker-api .
   ```

2. Run the Docker container:
   ```bash
   docker run -p 8080:8080 habit-tracker-api
   ```

#### Using Gradle

1. Run the application:
   ```bash
   ./gradlew bootRun
   ```

The application will start on `http://localhost:8080`.

## API Documentation

The API is documented using Swagger. You can access the documentation by navigating to `http://localhost:8080/swagger-ui.html` after starting the application.

## Usage

### Authentication

To authenticate, send a POST request to `/api/auth/login` with the following JSON body:

```json
{
  "username": "your_username",
  "password": "your_password"
}
```

On successful login, you will receive a JWT token. Use this token for subsequent requests.

### Creating a Habit

To create a new habit, send a POST request to `/api/habits` with the following JSON body:

```json
{
  "name": "Exercise",
  "frequency": "Daily"
}
```

### Checking In

To check in for a habit, send a POST request to `/api/habits/{id}/checkin`.

### Calculating Streaks

To get streak information, send a GET request to `/api/habits/{id}/streak`.

## Contributing

Contributions are welcome! If you want to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

For the latest releases, visit [Releases Section](https://github.com/GGD-github/habit-tracker-api/releases).