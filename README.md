🚀 Next.js Application Deployment using Docker, GitHub Actions, and Kubernetes (Minikube on AWS EC2)
📘 Project Overview

This project showcases a complete DevOps workflow for containerizing, automating, and deploying a modern web application.

I developed a Next.js application, containerized it using Docker, automated image building and pushing with GitHub Actions, and deployed it on a Kubernetes (Minikube) cluster hosted on an AWS EC2 instance.

The primary objective of this project was to gain practical experience in containerization, CI/CD automation, and Kubernetes-based deployment within a cloud environment.

🎯 Objectives

Containerize a Next.js application using Docker.

Automate the build and push process through GitHub Actions and GitHub Container Registry (GHCR).

Deploy the containerized app to a Kubernetes cluster running on Minikube.

Access the live application through a web browser using port forwarding or NodePort.

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

AWS EC2 (Ubuntu) – Cloud host for the cluster

YAML – Deployment and service configuration

🧱 Setup Summary

Cloned the repository and initialized a Next.js starter application.

Created a Dockerfile following best practices — using a lightweight base image, caching dependencies efficiently, and keeping image size minimal.

Designed a GitHub Actions workflow to automate Docker image build and push to GHCR upon each push to the main branch.

Built Kubernetes manifests inside a k8s/ folder —

deployment.yaml for defining replicas, container image, and probes

service.yaml for exposing the app to external traffic

Deployed the app on Minikube (running on AWS EC2) and verified accessibility via browser using port forwarding and NodePort.

☸️ Kubernetes Deployment Overview
Deployment Manifest

Defines the replica count, container image, and readiness/liveness probes.

Ensures app resilience and auto-restart on failure.

Service Manifest

Exposes the app through a NodePort service type for external access.

Allows the app to be reached through EC2’s public IP and the configured port.

After applying both manifests, the application successfully launched within the Minikube cluster.

🌍 Accessing the Application

Enabled inbound rules for port 3000 in the AWS EC2 Security Group.

Used the command:

minikube service nextjs-service --url


Accessed the app in a browser using the EC2 public IP or Minikube’s forwarded port.

Result: The application was fully functional and accessible externally.

✅ Results

Successfully containerized the Next.js app.

Automated CI/CD pipeline using GitHub Actions and GHCR.

Seamless Kubernetes deployment on Minikube running within AWS EC2.

Application accessible via browser, confirming end-to-end success.

🧠 Key Learnings

Through this project, I gained strong hands-on experience in:

Creating and optimizing Docker images for production.

Implementing CI/CD pipelines using GitHub Actions.

Managing and deploying workloads on Kubernetes clusters.

Resolving Minikube image pull and authentication challenges.

Exposing containerized apps securely on AWS EC2 instances.

🌐 Repository & Image Links

Repository URL: https://github.com/zainabkousar/nextjs-docker-app

GHCR Image URL: ghcr.io/zainabkousar/nextjs-docker-app:latest

Assessment Screenshots

### 🐳 Docker Container Running
![Docker Container Running](images/Docker container running.png)

### 🌍 Webpage Running
![Webpage Running](images/Webpage Running.png)

### ☸️ Kubernetes Pods Running
![Kubectl Pods Running](images/Kubectl pods running.png)

### 🤖 GitHub Actions Workflow
![Workflow Run](images/Workflow run.png)


📜 Author

Zainab Kousar
AWS & DevOps Engineer
📍 Hyderabad, India
