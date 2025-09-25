---
description: Repository Information Overview
alwaysApply: true
---

# WhatsApp Clone Information

## Repository Summary
This repository contains a full-stack WhatsApp clone application with a React frontend and Spring Boot backend. The application implements real-time chat functionality with features similar to WhatsApp, including user authentication, chat management, and message exchange.

## Repository Structure
The repository follows a typical client-server architecture with two main components:
- `frontend/`: React-based client application with UI components for chat interface
- `backend/`: Spring Boot Java application providing REST APIs and WebSocket support

### Main Repository Components
- **Frontend**: React application with Material UI and Tailwind CSS for styling
- **Backend**: Spring Boot application with JPA, Security, and WebSocket support
- **Docker**: Configuration for containerization of both frontend and backend

## Projects

### Backend (Spring Boot)
**Configuration File**: `backend/pom.xml`

#### Language & Runtime
**Language**: Java
**Version**: Java 17
**Build System**: Maven
**Package Manager**: Maven

#### Dependencies
**Main Dependencies**:
- Spring Boot 3.3.1 (Web, Security, JPA, WebSocket, Validation)
- MySQL Connector
- JWT (JSON Web Token) 0.11.5
- Spring Boot DevTools

#### Build & Installation
```bash
cd backend
mvn clean install
mvn spring-boot:run
```

#### Docker
**Dockerfile**: `backend/Dockerfile`
**Docker Compose**: `backend/docker-compose.yml`
**Configuration**: Multi-container setup with MySQL database and Spring Boot application

#### Database
**Type**: MySQL
**Configuration**: Configured via Docker Compose with volume persistence

### Frontend (React)
**Configuration File**: `frontend/package.json`

#### Language & Runtime
**Language**: JavaScript (React)
**Version**: React 18.2.0
**Package Manager**: npm/yarn

#### Dependencies
**Main Dependencies**:
- React 18.2.0
- React Router DOM 6.15.0
- Material UI 5.14.9
- Redux with Thunk
- SockJS and StompJS for WebSocket communication
- React Icons 4.11.0

**Development Dependencies**:
- Tailwind CSS 3.3.3

#### Build & Installation
```bash
cd frontend
npm install
npm start
```

#### Features
- Real-time messaging using WebSockets
- User authentication and profile management
- Group chat functionality
- Responsive UI design with Material UI and Tailwind CSS

## Integration
The frontend communicates with the backend through:
- REST APIs for user authentication, chat management, and message history
- WebSocket for real-time message exchange
- JWT-based authentication for secure API access

## Deployment
The application can be deployed using Docker:
```bash
cd backend
docker-compose up -d
```
This will start both the MySQL database and Spring Boot backend in containers. The frontend can be built and served separately or integrated into the Docker setup.