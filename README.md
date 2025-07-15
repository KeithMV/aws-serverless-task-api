# Enterprise Serverless Task Management API

A complete, production-ready serverless web application built with AWS Lambda, DynamoDB, S3, and Cognito. Demonstrates enterprise-grade architecture, Infrastructure as Code, and modern serverless development practices.

![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Terraform](https://img.shields.io/badge/terraform-%235835CC.svg?style=for-the-badge&logo=terraform&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

## 🏗️ Architecture
Internet → API Gateway → Lambda Functions → DynamoDB + S3 + Cognito
↓              ↓         ↓        ↓
Hello World      Tasks    Files    Users

## ✨ Features

### 🔐 User Management
- User registration with JWT tokens
- Secure login and authentication
- Password policies and security
- Protected API endpoints

### 📋 Task Management
- Create, read, update, delete tasks
- Task status tracking
- Priority levels and descriptions

### 📎 File Management
- Upload files and attach to tasks
- Secure S3 storage
- File download and deletion

### 🚀 Serverless Architecture
- Auto-scaling from zero to millions of users
- Pay-per-use pricing model
- No server management required

## 🛠️ Technology Stack

- **AWS Lambda** - Serverless compute
- **API Gateway** - REST API management
- **DynamoDB** - NoSQL database
- **S3** - File storage
- **Cognito** - User authentication
- **Terraform** - Infrastructure as Code

## 🚀 Quick Start

### Prerequisites
- AWS Account with CLI configured
- Terraform installed

### Deployment
```bash
git clone https://github.com/KeithMV/aws-serverless-task-api.git
cd aws-serverless-task-api
terraform init
terraform apply

📋 API Endpoints
Authentication
POST /auth/register - Register user
POST /auth/login - Login user
GET /auth/user - Get user profile

Tasks
GET /tasks - List tasks
POST /tasks - Create task
PUT /tasks/{id} - Update task
DELETE /tasks/{id} - Delete task

Files
POST /tasks/{id}/files - Upload file
GET /tasks/{id}/files - List files
GET /files/{id} - Download file

🧪 Testing
bash# Register user
curl -X POST https://your-api/auth/register -d '{"email":"test@example.com","password":"Test123!"}'

# Login
curl -X POST https://your-api/auth/login -d '{"email":"test@example.com","password":"Test123!"}'

# Create task
curl -X POST https://your-api/tasks -d '{"title":"My Task","description":"Testing"}'
💰 Cost

Development/Testing: $1-10/month
Production: Scales with usage
Pay-per-use: No idle server costs

🔒 Security

✅ JWT token authentication
✅ Encrypted storage
✅ IAM roles with least privilege
✅ Password complexity requirements

📄 License
MIT License - see LICENSE file for details.
👨‍💻 Author
Keith Vose

Email: kmvose@gmail.com



⭐ Star this repository if you found it helpful!