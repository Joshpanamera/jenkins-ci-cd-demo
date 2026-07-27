# Jenkins CI/CD Pipeline Demo

## Overview

This project demonstrates a complete CI/CD pipeline built with Jenkins, Docker, GitHub, and AWS EC2.

Whenever code is pushed to GitHub, a GitHub Webhook automatically triggers Jenkins. Jenkins checks out the latest source code, builds a Docker image, and deploys the application inside a Docker container running Nginx.

The application is then immediately available through the EC2 public IP.

---

## Technologies

- Jenkins
- Docker
- Nginx
- Git
- GitHub
- GitHub Webhooks
- AWS EC2
- Ubuntu Linux

---

## Project Structure

```
jenkins-ci-cd-demo
│
├── app/
│   └── index.html
├── Dockerfile
├── Jenkinsfile
├── README.md
└── .gitignore
```

---

## CI/CD Workflow

```
Developer
    │
git add
git commit
git push
    │
    ▼
GitHub Repository
    │
Webhook
    ▼
Jenkins
    │
Checkout Source Code
    │
Build Docker Image
    │
Run Docker Container
    ▼
Live Website
```

---

## Jenkins Pipeline Stages

### Checkout SCM

Jenkins clones the latest version of the GitHub repository.

### Build Docker Image

Docker builds a new image using the Dockerfile.

### Run Docker Container

The previous container is removed and replaced with the latest version.

---

## Features

- Automated builds
- Dockerized application
- Continuous Deployment
- GitHub Webhook integration
- Jenkins Pipeline as Code
- Nginx web server
- AWS EC2 deployment

---

## Lessons Learned

During this project I learned:

- GitHub Webhooks
- Jenkins Pipelines
- Docker image creation
- Docker container deployment
- Linux server administration
- Git authentication using Personal Access Tokens
- Jenkins permissions with Docker
- Troubleshooting CI/CD pipelines

---

## Future Improvements

- Add automated testing
- Push Docker images to Docker Hub
- Deploy to Kubernetes
- Add image versioning
- Deploy to multiple environments
## Screenshots

### GitHub Repository

![GitHub Repository](screenshots/github-repository.png)

---

### Jenkins Pipeline

![Jenkins Pipeline](screenshots/jenkins-pipeline.png)

---

### Successful Build Logs

![Console Output](screenshots/console-output.png)

---

### Live Website

![Live Website](screenshots/deployed-website.png)