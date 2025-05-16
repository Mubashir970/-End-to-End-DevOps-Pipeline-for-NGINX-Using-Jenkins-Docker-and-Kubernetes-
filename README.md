# -End-to-End-DevOps-Pipeline-for-NGINX-Using-Jenkins-Docker-and-Kubernetes-
This project demonstrates a complete CI/CD pipeline implementation for automating the deployment of a containerized NGINX web server using Docker, Jenkins, and Kubernetes. The objective is to enable consistent, repeatable, and scalable deployment workflows across different environments such as development and production.

The pipeline is parameterized to accept an environment type (dev or prod) and is triggered automatically via a GitHub webhook. Upon a code change (e.g., update to the Dockerfile), Jenkins performs the following tasks:

Clones the GitHub repository containing the Dockerfile

Builds a Docker image for NGINX on Ubuntu or RedHat

Runs a container and performs a health check using the curl command (expects HTTP 200 OK)

Pushes the validated image to a container registry like DockerHub or Amazon ECR

Deploys the image either to a Docker host or a Kubernetes cluster using kubectl apply

Exposes the application to external users via IP and port for real-time access

The project is designed to align with DevOps best practices including automation, environment consistency, health checks, and clean rollouts.
