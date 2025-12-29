# Dance Workshop Management System – AWS ECS Deployment

This project is a **PHP + MySQL web application** deployed on **AWS ECS (Fargate)** using **Docker, Amazon ECR, RDS, and GitHub Actions CI/CD**.  
The goal of this repository is to demonstrate **real-world DevOps practices** such as containerization, CI/CD automation, cloud deployment, and infrastructure understanding.


## 🚀 Project Overview

The **Dance Workshop Management System** allows users to manage dance workshops, registrations, and related information using a PHP-based web application backed by a MySQL database.


## 🛠 Tech Stack

### Application
- PHP 8.1
- Apache Web Server
- MySQL

### DevOps & Cloud
- Docker
- GitHub Actions (CI)
- Amazon ECR (Container Registry)
- Amazon ECS (Fargate)
- Application Load Balancer (ALB)
- Amazon RDS (MySQL)
- Amazon S3 (DB backup/import)
- Amazon CloudWatch (Logs & Monitoring)


## 🧱 Architecture

GitHub Repository
↓
GitHub Actions (CI)
↓
Docker Image
↓
Amazon ECR
↓
Amazon ECS (Fargate)
↓
Application Load Balancer
↓
Public Application URL

Database:
Amazon RDS (MySQL)


## 📁 Repository Structure

.
├── danceworkshop-master/
│ └── danceworkshop/ # PHP application source code
├── Dockerfile # Docker image definition
├── .dockerignore
├── .github/
│ └── workflows/
│ └── docker-ecr.yml # GitHub Actions CI pipeline
└── README.md


## 🐳 Dockerization

The application is containerized using Docker.

### Dockerfile
- Uses `php:8.1-apache`
- Installs required MySQL PHP extensions
- Copies application code to `/var/www/html`
- Exposes port `80`

---

## 🔁 CI Pipeline (GitHub Actions)

The CI pipeline automatically:
1. Checks out the code
2. Builds the Docker image
3. Logs in to Amazon ECR
4. Pushes the image to ECR

Pipeline runs on every push to the `main` branch.

---

## 🗄 Database Setup (Amazon RDS)

- Engine: MySQL
- Database name: `danceworkshop`
- Credentials provided via ECS environment variables
- Database initialized using an SQL dump file

### Database Import Flow
SQL File → Amazon S3 → EC2 (MySQL Client) → Amazon RDS


## 🚢 Deployment on AWS ECS (Fargate)

### ECS Components Used
- ECS Cluster (Fargate)
- Task Definition
- ECS Service
- Application Load Balancer
- IAM Roles
- CloudWatch Logs

### Environment Variables Used
DB_HOST
DB_NAME
DB_USER
DB_PASS


## 🌐 Application Access

The application is exposed using an **Application Load Balancer**.

http://<ALB-DNS-NAME>


## 📊 Monitoring & Logs

- Logs are stored in **Amazon CloudWatch**
- ECS task logs can be used for debugging and monitoring


## 🔐 Security Best Practices

- IAM roles used instead of hardcoded credentials
- Database access restricted via security groups
- GitHub Secrets used for AWS credentials
- RDS not publicly accessibl

## 🧠 DevOps Learning Outcomes

This project demonstrates:
- Dockerizing legacy PHP applications
- CI automation using GitHub Actions
- Container image management with Amazon ECR
- Serverless container deployment with ECS Fargate
- Database provisioning with Amazon RDS
- Secure cloud deployments using IAM
- Real-world DevOps workflow and architecture


## 🧹 Cleanup (Cost Optimization)

To avoid unnecessary AWS costs:
- Scale ECS service to 0
- Stop or delete RDS instance
- Delete ALB and ECR images when not in use


## 📌 Future Enhancements

- Infrastructure as Code using Terraform
- CD pipeline to auto-deploy to ECS
- HTTPS using ACM
- Secrets Manager integration
- Auto Scaling policies

---

## 👨‍💻 Author

**DevOps Engineer Project**  
Built to demonstrate hands-on DevOps and AWS ECS deployment skills.
