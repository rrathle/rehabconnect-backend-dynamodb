// Project: RehabConnect - Patient Progress Tracker
// Backend: Java + Spring Boot + DynamoDB

# RehabConnect Backend – Java + Spring Boot + DynamoDB

A backend service for logging and tracking physical therapy sessions. Built with Java + Spring Boot and designed to be deployed on AWS (Lambda + API Gateway + Cognito) with DynamoDB as the primary NoSQL database.

---

## Features
- Patients can log daily rehab activities
- PTs can track progress and update rehab plans
- Secure user login with AWS Cognito
- RESTful API
- DynamoDB-powered data storage

---

## Tech Stack
- Java 17
- Spring Boot 3
- AWS: Lambda, API Gateway, Cognito, S3 (optional)
- Database: DynamoDB (NoSQL)
- Build Tool: Maven
- Deployment: SAM CLI / AWS Console / Docker

---

## Endpoints
| Method | Endpoint                 | Description                         |
|--------|--------------------------|-------------------------------------|
| POST   | `/log`                   | Log rehab activity session          |
| GET    | `/progress/{patientId}` | Retrieve progress logs              |
| PUT    | `/plan/{patientId}`     | Update patient rehab plan           |

---

## Folder Structure
```
rehabconnect-backend/
├── src/
│   └── main/java/com/rehabconnect/
│       ├── controller/
│       ├── model/
│       ├── service/
│       └── repository/
├── resources/
│   └── application.yml
├── pom.xml
└── README.md
```

---

## Setup Instructions
```bash
git clone https://github.com/yourusername/rehabconnect-backend.git
cd rehabconnect-backend
./mvnw spring-boot:run
```

Ensure AWS credentials and DynamoDB setup are configured properly.

---

## Coming Soon
- React Frontend (optional)
- GraphQL migration
- Docker deployment

---

## Architecture Overview
```
[Frontend (React/HTML)]
      ↓
[API Gateway (REST)]
      ↓
[AWS Lambda (Spring Boot)]
      ↓
[DynamoDB (NoSQL)]
      ↓
[Cognito (Auth)]
```

---

## Example Data Model (JSON)
```json
{
  "patientId": "abc-123",
  "date": "2025-06-23",
  "painLevel": 4,
  "exercises": ["Bridge", "Bird Dog"],
  "repsCompleted": 20
}
```

---

## License
MIT

