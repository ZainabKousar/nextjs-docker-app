🚀 Next.js Application Deployment using Docker, GitHub Actions, and Kubernetes (Minikube on AWS EC2)
📘 Project Overview

This project showcases a complete DevOps workflow for containerizing, automating, and deploying a modern web application.

I developed a Next.js application, containerized it using Docker, automated image building and pushing with GitHub Actions, and deployed it on a Kubernetes (Minikube) cluster hosted on an AWS EC2 instance.

The primary objective of this project was to gain practical experience in containerization, CI/CD automation, and Kubernetes-based deployment within a cloud environment.

🎯 Objectives

Containerize a Next.js application using Docker

Automate the build and push process through GitHub Actions and GitHub Container Registry (GHCR)

Deploy the containerized app to a Kubernetes cluster running on Minikube

Access the live application through a web browser using port forwarding or NodePort

🧩 Project Architecture

The workflow follows a smooth DevOps pipeline:

The Next.js app is built and packaged into a Docker container.

A GitHub Actions workflow triggers automatically on code pushes to the main branch — it builds the Docker image and pushes it to GHCR.

The latest image is then deployed to a Kubernetes cluster using YAML manifests for Deployment and Service configuration.

The app is finally exposed via NodePort or port forwarding for browser access from AWS EC2.

⚙️ Tools & Technologies

Next.js – Frontend framework

Docker – Containerization

GitHub Actions – CI/CD automation

GitHub Container Registry (GHCR) – Image storage

Kubernetes (Minikube) – Container orchestration

AWS EC2 (Ubuntu) – Cloud environment

YAML – Deployment and service manifests

🧱 Setup Summary

Cloned the repository and initialized a Next.js starter application.

Created a Dockerfile following best practices — lightweight base image, caching dependencies efficiently, minimal image size.

Designed a GitHub Actions workflow to automate Docker image build and push to GHCR on every push to main.

Built Kubernetes manifests in a k8s/ folder:

deployment.yaml → defines replicas, container image, and probes

service.yaml → exposes the app externally

Deployed the app on Minikube (running on AWS EC2) and verified accessibility via browser using port forwarding and NodePort.

☸️ Kubernetes Deployment Overview

Deployment Manifest: Defines replicas, container image, readiness/liveness probes. Ensures app resilience and auto-restart on failure.

Service Manifest: Exposes the app through NodePort for external access. Allows the app to be reached via EC2 public IP.

After applying both manifests, the application successfully launched in the Minikube cluster.

🌍 Accessing the Application

Enabled inbound rules for port 3000 in the AWS EC2 Security Group.

Used the command:

minikube service nextjs-service --url


Accessed the app in a browser using EC2 public IP or Minikube forwarded port.

✅ Results

Successfully containerized the Next.js app

Automated CI/CD pipeline with GitHub Actions and GHCR

Seamless Kubernetes deployment on Minikube running on AWS EC2

Application accessible externally through browser

🧠 Key Learnings

Creating and optimizing Docker images for production

Implementing CI/CD pipelines using GitHub Actions

Managing and deploying workloads on Kubernetes clusters

Resolving Minikube image pull and authentication challenges

Exposing containerized apps securely on AWS EC2 instances

📸 Project Screenshots

All key screenshots are shown below:

### 🐳 Docker Container Running
![Docker Container Running](images/Docker%20container%20running.png)

### 🌍 Webpage Running
![Webpage Running](images/Webpage%20Running.png)

### ☸️ Kubernetes Pods Running
![Kubectl Pods Running](images/Kubectl%20pods%20running.png)

### 🤖 GitHub Actions Workflow
![Workflow Run](images/Workflow%20run.png)


🌐 Repository & Image Links

Repository URL: https://github.com/zainabkousar/nextjs-docker-app

GHCR Image URL: [ghcr.io/zainabkousar/nextjs-docker-app:latest](https://ghcr.io/zainabkousar/nextjs-docker-app)


📜 Author

Zainab Kousar
AWS & DevOps Engineer
📍 Hyderabad, India
