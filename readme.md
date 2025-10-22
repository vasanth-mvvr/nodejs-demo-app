# ** Task-1 Automate Code Deployment using CI/CD Pipeline (GitHub Actions)**

Overview
This project demonstrates the automation of deploying a Node.js application using a CI/CD pipeline powered by GitHub Actions.
The application is deployed on an AWS EC2 instance and runs on port 3000 inside a Docker container.

1. EC2 Instance Setup
   An AWS EC2 instance hosts the Node.js application.
   Security group rules allow inbound traffic on:
   Port 22 for SSH access.
   Port 3000 for accessing the application.
   Node.js and Docker are installed on the instance to run containerized applications.
2. Dockerfile
   Builds a lightweight and secure container image for the Node.js application.Uses Node:alpine as the base image for minimal storage.
   Uses a minimal base image to reduce storage requirements.
   Installs all required dependencies.
   Runs the application with a non-root user for improved security.
   The built image is pushed to Docker Hub, which acts as a container registry.
3. GitHub Actions (CI/CD Pipeline)
   Automates the process of building, testing, and deploying the application.
   Triggered automatically when changes are pushed to the repository.
   Steps include:
   Checking out the repository.
   Building the application.
   Creating a Docker image.
   Pushing the Docker image to Docker Hub.
   Deploying the container to the EC2 instance.
4. Result
   Every code update triggers an automated pipeline.
   The Node.js application is deployed and accessible on the configured port.
   Ensures secure, reliable, and consistent deployments.
