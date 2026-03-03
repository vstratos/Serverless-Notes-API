# Serverless-Notes-API (AWS)

Production-ready Serverless REST API built on AWS using Lambda, API Gateway and DynamoDB.

This project demonstrates cloud-native backend development using Infrastructures as Code (AWS SAM) and implements full CRUD functionality with validation and pagination.

## Architecture

Client -> API Gateway -> AWS Lambda -> DynamoDB

- API Gateway: Handles HTTP requests
- AWS Lambda: executes Python backend logic
- DynamoDB: stores notes (NoSQL, PAY_PER_REQUEST)
- AWS SAM: manages infrastructure as code
- CloudFormation: provision resources

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|------------|
| POST | /notes | Create a new note |
| GET | /notes | List notes (supports pagination) |
| GET | /notes/{id} | Retrieve a specific note |
| PUT | /notes/{id} | Update a note |
| DELETE | /notes/{id} | Delete a note |
| GET | /hello | Health check |

## Features 

- Full CRUD implementation
- Input validation
- Proper HTTP status codes (200, 201, 400, 404)
- Pagination support
- Infrastructure as Code (SAM template)
- IAM rolew-based access control
- Free-tier friendly design

## Tech Stack

- Python 3.11
- AWS Lambda
- Amazon API Gateway
- Amazon DynamoDB
- AWS SAM
- CloudFormation

## Deployment

Build and deploy using AWS SAM 
'''bash
sam build
sam deploy
