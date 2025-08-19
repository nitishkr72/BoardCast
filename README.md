# 📝 Riveto - Collaborative Project Management Platform (Monorepo)

A **realtime collaborative Kanban board** built with:  
- **Backend:** Java Spring Boot (microservices, gRPC, WebSockets, SNS/SQS)  
- **Frontend:** React + WebSockets (for live updates)  
- **Infra:** AWS Free Tier (Lambda, API Gateway, S3, CloudFront, SNS/SQS, DynamoDB/RDS)  
- **CI/CD:** GitHub Actions (monorepo setup)  


## 📂 Monorepo Structure

```text
riveto/
│── backend/                      # Spring Boot microservices
│   ├── auth-service/             # Authentication & users
│   ├── team-service/             # Team management
│   ├── board-service/            # Kanban boards
│   ├── task-service/             # Tasks & workflow
│   ├── collab-service/           # WebSocket collaboration
│   ├── notif-service/            # Notifications
│   └── common-libs/              # Shared DTOs & utils
│
│── frontend/                     # React app (Kanban UI)
│   ├── src/                      # Components, hooks, pages
│   └── package.json
│
│── infra/                        # Infrastructure as Code
│   ├── aws/                      # Terraform/CDK configs
│   ├── k8s/                      # (Optional) EKS manifests
│   └── ci-cd/                    # GitHub Actions workflows
│
│── scripts/                      # Dev/test helper scripts
│── README.md
```

## 🚀 Features

- Realtime updates (WebSocket + Observer pattern)  
- Task move events (event-driven via SNS/SQS)  
- Notifications & activity feed  
- In-memory caching (AWS Free Tier friendly)  
- Monorepo with shared codebase (frontend + backend + infra)  
- CI/CD pipeline with GitHub Actions  


## 🛠️ Tech Stack

- **Frontend:** React, Redux/React Query, WebSockets  
- **Backend:** Spring Boot (Java 17), gRPC, WebSockets, SNS/SQS  
- **Database:** PostgreSQL (RDS Free Tier) / DynamoDB (optional)  
- **Caching:** In-memory (to stay free-tier)  
- **Infra:** AWS Lambda, API Gateway, S3, CloudFront, SNS/SQS  
- **DevOps:** Docker, GitHub Actions, Terraform/CDK  
