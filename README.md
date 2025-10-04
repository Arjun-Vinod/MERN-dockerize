
# MERN Stack Dockerized Application

## Overview
This project demonstrates the containerization of a MERN stack application using Docker. The application is split into three separate containers:

- Frontend: React application
- Backend: Node.js
- Database: MongoDB

All containers are connected through a custom Docker network, enabling seamless communication between services.

## Prerequisites
Before running this project, ensure you have the following installed:

- Docker 
- Git (to clone the repository)

## Getting Started

1. Clone the Repository

```bash
   git clone <repository-url>

   cd <project-directory>
```
2. Environment Variables:
Create a .env file in the `backend/` directory to configure environment variables (e.g., MongoDB URI).

```bash
   MONGO_URI=<your URI>
```

2. Build and Run with Docker Compose

```bash
   docker-compose up -d
```

This command will:

- Build Docker images for both frontend and backend
- Pull the MongoDB image
- Create a custom network
- Start all containers
- Mount volumes for persistent data storage

## Docker Configuration
**Frontend Dockerfile :**

Located in `frontend/Dockerfile`, this file:

- Uses Node.js as the base image
- Installs dependencies
- Builds the React application

**Backend Dockerfile :**

Located in `Backend/Dockerfile`, this file:

- Uses Node.js as the base image
- Installs dependencies
- Exposes the API port
- Starts the Express server

**Docker Compose :**

The docker-compose.yml file orchestrates:

- Three services: frontend, backend, and MongoDB
- Custom network: Enables inter-container communication
- Volume mounting: Persists MongoDB data
- Port mapping: Exposes services to the host machine

## Running the Application

1. Start the Containers: Use Docker Compose to start the frontend, backend, and MongoDB containers:

```bash
   docker-compose up -d
```

2. Stop the Containers: To stop the running containers:

```bash
   docker-compose down
```


