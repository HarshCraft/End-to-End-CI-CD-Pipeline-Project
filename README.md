# End-to-End 3-Stage CI/CD Pipeline Automation on AWS
Project Overview

This project demonstrates the design and implementation of a fully automated 3-stage CI/CD pipeline on AWS, integrating Continuous Integration (CI), Infrastructure as Code (IaC), and Continuous Deployment (CD).
The pipeline automates the complete software delivery lifecycle from source code integration to infrastructure provisioning and Kubernetes deployment using Jenkins, Terraform, Docker, Amazon EKS, and Kubernetes.

Stage 1 — Continuous Integration (CI Pipeline)
GitHub Repository Link: https://github.com/HarshCraft/studentapp-project
Objective:

Automate source code integration, testing, code quality analysis, and artifact storage.

Process:
Developer pushes source code to GitHub repository
GitHub Webhook triggers Jenkins pipeline automatically
Jenkins pulls latest source code
Maven performs build and dependency management
Automated test cases are executed
SonarQube performs static code analysis and quality gate validation
Build artifact is stored in Amazon S3 for versioned storage
Tools Used:
GitHub
GitHub Webhooks
Jenkins
Maven
SonarQube
Amazon S3


Stage 2 — Infrastructure Provisioning (Terraform + AWS EKS)
GitHub Repository Link: https://github.com/HarshCraft/Infrastructure-repp
Objective:

Provision production-ready Kubernetes infrastructure using Infrastructure as Code.
Process:
Jenkins executes Terraform Init
Terraform downloads required providers
Terraform Plan validates infrastructure changes
Terraform Apply provisions infrastructure on AWS
Amazon EKS Cluster is created
Worker Node Groups are configured


Stage 3 — Continuous Deployment (Docker + Kubernetes)
GitHub Repository Link: https://github.com/HarshCraft/Thirdstagepipeline
Objective:

Containerize application and deploy it on Kubernetes cluster.

Process:
Docker image is built from application source code
Docker image is pushed to Amazon ECR
Kubernetes deployment YAML files are applied
Pods are created on Amazon EKS
Kubernetes Services expose application
Application becomes available in scalable containerized environment
