# 🚀 Jenkins CI/CD Pipeline for Virtual Browser Project

## 📌 Project Overview
This project demonstrates a **CI/CD pipeline built using Jenkins** to automate the build, test, scan, and deployment of the [Virtual Browser](https://github.com/sid-295/Vitual-Browser.git) application.  

---

## 🏗️ CI/CD Pipeline Workflow

### 1️⃣ Git Checkout
- Fetches the latest source code from the GitHub repository.  
- Ensures the pipeline always works on the latest committed code.

### 2️⃣ OWASP Dependency Check
- Performs **vulnerability scanning** of dependencies.  
- Generates security reports.  
- Ensures no critical CVEs make it to production.  

### 3️⃣ SonarQube Analysis
- Runs **static code analysis** using SonarQube.  
- Checks for code smells, bugs, and maintainability issues.  
- Enforces **quality gates** before proceeding.

### 4️⃣ Docker Build
- Builds a **Docker image** of the application.  
- Uses a custom **Dockerfile** located in `.docker/firefox/`.  
- Tags the image as `cyber295/wb:latest`.

### 5️⃣ Trivy Image Scan
- Scans the Docker image for vulnerabilities.  
- Ensures the container is **secure before pushing**.

### 6️⃣ Docker Push
- Authenticates with **Docker Hub** using Jenkins credentials.  
- Pushes the built image to [Docker Hub Registry](https://hub.docker.com/).  

### 7️⃣ Deploy with Docker Compose
- Deploys the application using **docker-compose**.  
- Ensures the application is running inside containers.

---

## ⚙️ Tools & Technologies Used
- **Jenkins** – CI/CD Orchestration  
- **OWASP Dependency Check** – Dependency vulnerability scanning  
- **SonarQube** – Static code analysis  
- **Docker** – Containerization  
- **Trivy** – Docker image vulnerability scanning  
- **Docker Hub** – Container registry  
- **Docker Compose** – Deployment  

---


