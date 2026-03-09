# Finance Tracker API

A backend REST API for tracking personal financial transactions.  
Users can record income and expenses, retrieve transactions, update entries, and delete them. The application is built with **Spring Boot**, uses **PostgreSQL** for persistence, and is fully containerized using **Docker and Docker Compose**.

This project demonstrates backend development, API design, database integration, containerization, and deployment to AWS.

---

## Features

- Create financial transactions
- Retrieve all transactions
- Retrieve a transaction by ID
- Update existing transactions
- Delete transactions
- PostgreSQL database persistence
- Fully containerized backend with Docker
- Deployment-ready using Docker Compose
- Deployed on AWS EC2

---

## Tech Stack

### Backend
- Java
- Spring Boot
- Spring Data JPA
- REST APIs

### Database
- PostgreSQL

### Infrastructure & DevOps
- Docker
- Docker Compose
- AWS EC2

### Tools
- IntelliJ IDEA
- Postman
- Git / GitHub

---

## API Endpoints

Base URL:

```
/api/transactions
```

| Method | Endpoint | Description |
|------|------|------|
| GET | `/api/transactions` | Get all transactions |
| GET | `/api/transactions/{id}` | Get transaction by ID |
| POST | `/api/transactions` | Create a new transaction |
| PUT | `/api/transactions/{id}` | Update a transaction |
| DELETE | `/api/transactions/{id}` | Delete a transaction |

### Example POST Request

```json
{
  "amount": "50.00",
  "type": "Expense",
  "category": "Food",
  "description": "Chipotle",
  "date": "2026-01-01"
}
```

---

## Project Structure

```
finance-tracker
├── src
│   ├── controller
│   ├── model
│   ├── repository
│   └── service
├── Dockerfile
├── docker-compose.yml
├── pom.xml
└── README.md
```

---

## Running the Project Locally

### Requirements

- Docker
- Docker Compose

### Start the application

```bash
docker-compose up --build
```

This will:

1. Build the Spring Boot application
2. Start the PostgreSQL container
3. Start the backend API container

The API will be available at:

```
http://localhost:8080
```

Example endpoint:

```
http://localhost:8080/api/transactions
```

---

## Deployment (AWS EC2)

The application can be deployed to AWS using Docker Compose on an EC2 instance.

### Steps

1. Launch an EC2 instance
2. Install Docker
3. Clone the repository
4. Run:

```bash
docker-compose up --build -d
```

The API will then be accessible via:

```
http://<EC2_PUBLIC_IP>:8080
```

---

## Future Improvements

- Transaction categories and filtering
- Monthly spending summaries
- Authentication and user accounts
- Frontend UI for interacting with the API
- CI/CD pipeline for automatic deployments
- HTTPS with Nginx and a custom domain

---

## Author

**Elias Nemiri**  
