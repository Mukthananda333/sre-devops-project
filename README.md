# SRE DevOps CI/CD Pipeline Project

## Overview

This project demonstrates a CI/CD automation workflow using GitHub, Jenkins, Docker, and Kubernetes manifests.

The pipeline automates:

* Docker image build
* Container deployment
* CI/CD workflow execution
* Deployment configuration management

---

## Technologies Used

* Git & GitHub
* Jenkins
* Docker
* Docker Hub
* Docker Compose
* Kubernetes YAML
* Node.js
* Express.js
* Ubuntu WSL2
* Groovy Pipeline

---

## Project Architecture

Developer Push → GitHub → Jenkins Pipeline → Docker Build → Docker Hub Push → Deployment

---

## Project Structure

```text
sre-devops-project/
│
├── app.js
├── package.json
├── Dockerfile
├── docker-compose.yml
├── Jenkinsfile
├── README.md
├── .gitignore
└── k8s/
    ├── deployment.yaml
    └── service.yaml
```

---

## CI/CD Pipeline Stages

1. Build Docker Image
2. Deploy Docker Container
3. Verify Deployment

---

## Docker Commands Used

### Build Docker Image

```bash
docker build -t sre-devops-project .
```

### Run Container

```bash
docker run -d -p 3000:3000 --name sre-container sre-devops-project
```

### Verify Running Containers

```bash
docker ps
```

---

## Kubernetes Configuration

Kubernetes manifests were prepared for deployment orchestration.

Files:

* deployment.yaml
* service.yaml

These manifests define:

* Deployment configuration
* Resource limits
* Replica settings
* Service exposure

---

## Challenges Faced

During implementation, Kubernetes local clusters such as Minikube and Docker Desktop Kubernetes became unstable due to 4 GB RAM limitations inside WSL2 virtualization.

Issues encountered:

* kube-apiserver instability
* TLS handshake timeout
* Node NotReady
* API connection resets
* Resource exhaustion

To maintain stable CI/CD functionality, Docker Compose deployment was used while Kubernetes manifests were still prepared and validated.

Additional troubleshooting was performed with:

* Minikube
* K3s
* kind
* WSL2 optimization
* kube-apiserver debugging
* cgroup v2 configuration

---

## Application Access

```text
http://localhost:3000
```

---

## Learning Outcomes

This project helped in understanding:

* CI/CD pipeline automation
* Jenkins pipeline scripting
* Docker containerization
* Kubernetes manifests
* Infrastructure troubleshooting
* WSL2 Linux environment
* DevOps workflows

---

## Final Status

Successfully Completed:

* Docker containerization
* Jenkins pipeline creation
* Node.js deployment
* Kubernetes YAML preparation
* CI/CD workflow implementation
* GitHub project integration

```
```
Webhook final test
Webhook working
Webhook final success
Webhook final success
