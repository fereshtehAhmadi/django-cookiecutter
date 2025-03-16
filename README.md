# Project Name

A scalable, secure, and production-ready Django project template.

## Description

This is a Django-based web application template, designed to be easily customizable for your next project. It supports Docker for local development, background tasks with Celery, and modular architecture for scalability.

## Features

- **Django**: Fully featured web framework for Python.
- **Docker**: Easy local setup using Docker and Docker Compose.
- **Celery**: For asynchronous task processing.
- **PostgreSQL**: Production-ready database.
- **Whitenoise**: For serving static files in production.
- **Django REST Framework**: To build RESTful APIs.
- **Configurable Environments**: Supports different environments like local, production, etc.
- **Customizable Setup**: Can be adapted for different use cases like e-commerce, microservices, etc.

## Prerequisites

- Python 3.10 or higher
- Docker
- Docker Compose

## Setup

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/yourprojectname.git
cd yourprojectname
```

### 2. Install Docker & Docker Compose
Follow the instructions on the Docker [official website](https://www.docker.com/get-started) to install Docker and Docker Compose.

### 3. Start the Application with Docker
```bash
docker-compose -f local.yml up
```
This will build the Docker containers and start the application.

### 4. Run Migrations
```bash
docker-compose -f local.yml run --rm django python manage.py migrate
```
### 5. Create a Superuser
```bash
docker-compose -f local.yml run --rm django python manage.py createsuperuser
```
### 6. Access the Application
The application should now be available at http://localhost:8000. You can access the Django admin panel at http://localhost:8000/admin using the superuser credentials you created.

## Local Environment Setup
You can keep local environment files by setting keep local envs to y when prompted during setup. These files contain sensitive information such as your secret key and database credentials. Make sure to manage them securely.

## Development
For development, you can make changes directly in the application, and the Docker container will reload automatically.

## Deployment
For production, you can modify the production.py settings file and configure environment variables for security. The Docker setup is already optimized for production.

