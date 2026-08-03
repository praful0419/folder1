# DevOps CI/CD Pipeline with Jenkins, Docker, AWS ECR & EC2

## 📌 Project Overview

This project demonstrates a complete CI/CD pipeline that automates the process of building, storing, and deploying a Dockerized application using Jenkins and AWS services.

Whenever code is pushed to GitHub, Jenkins automatically builds a Docker image, pushes it to Amazon ECR, and deploys the latest version on an AWS EC2 instance.

---

## 🏗️ Architecture

Developer
    │
    ▼
GitHub Repository
    │
    ▼
GitHub Webhook
    │
    ▼
Jenkins
    │
    ├── Checkout Source Code
    ├── Build Docker Image
    ├── Push Image to Amazon ECR
    └── Connect to Target EC2
                │
                ▼
        Pull Latest Image
                │
                ▼
        Run Docker Container
                │
                ▼
          Web Application
```

---

## 🚀 Technologies Used

* Jenkins
* Docker
* Git & GitHub
* Amazon EC2
* Amazon ECR
* AWS CLI
* Linux (Ubuntu)
* Shell Scripting

---

## 📂 Pipeline Workflow

1. Developer pushes code to GitHub.
2. GitHub Webhook triggers Jenkins.
3. Jenkins checks out the latest source code.
4. Docker image is built.
5. Jenkins authenticates with Amazon ECR.
6. Docker image is pushed to Amazon ECR.
7. Jenkins connects to the target EC2 instance using SSH.
8. Target EC2 pulls the latest Docker image.
9. Existing container is stopped and removed.
10. A new container is started with the latest image.

---

## 📁 Project Structure

```text
.
├── Dockerfile
├── Jenkinsfile
├── index.html
└── README.md
```

---

## ⚙️ Prerequisites

* AWS Account
* Docker installed
* Jenkins installed
* AWS CLI configured
* Amazon ECR repository
* Two EC2 instances (Jenkins Server & Target Server)
* GitHub repository

---

## ▶️ Deployment Steps

1. Clone the repository.
2. Configure Jenkins credentials.
3. Create an Amazon ECR repository.
4. Configure IAM permissions for EC2/Jenkins.
5. Configure GitHub Webhook.
6. Run the Jenkins pipeline.
7. Access the application using the target EC2 public IP.

---

## 🔐 AWS Services Used

* Amazon EC2
* Amazon ECR
* IAM

---

## 📸 Future Improvements

* Kubernetes Deployment
* Helm Charts
* Terraform Infrastructure
* SonarQube Code Analysis
* Trivy Image Scanning
* Blue-Green Deployment
* Monitoring with Prometheus & Grafana

---

If you found this project useful, consider giving it a ⭐ on GitHub.
