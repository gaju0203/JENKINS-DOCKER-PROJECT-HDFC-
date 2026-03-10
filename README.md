### 🚀 Jenkins Docker Swarm CI/CD Project – HDFC Use Case
📌 Project Overview

This project demonstrates a real-world CI/CD pipeline using Jenkins, Docker, Docker Swarm, and DockerHub to build, push, and deploy containerized applications in a High Availability (HA) environment.

Multiple developers push code to GitHub. Jenkins automatically pulls the code, builds Docker images, pushes them to DockerHub, and deploys containers across Docker Swarm worker nodes using Docker Compose.


## 🏗️ Project Architecture

<img width="1536" height="1024" alt="ChatGPT Image Mar 3, 2026, 03_45_04 PM" src="https://github.com/user-attachments/assets/9d38c14c-f1b7-4e9f-89a6-c653933a5e89" />


# Architecture Flow:

-Multiple developers (dev-1, dev-2, dev-3) push code to GitHub

-Jenkins (running on Docker Swarm Manager) pulls the code

-Jenkins builds Docker images using Dockerfile

-Images are pushed to DockerHub

-Docker Swarm deploys containers in HA mode across Worker Nodes

-Application runs with load distribution and fault tolerance



## 🛠️ Tools & Technologies

-Jenkins (CI/CD Automation)

-Docker (Containerization)

-Docker Swarm (Orchestration & HA)

-Docker Compose (Service deployment)

-DockerHub (Image Registry)

-GitHub (Source Control)

-Linux (Deployment Environment)

-HTML (Sample Web Application)

## 📂 Project Structure

JENKINS-DOCKER-PROJECT-HDFC/
|
|- Dockerfile              # Build Docker image
|-JenkinsPipeline         # Jenkins CI/CD pipeline script
|-docker-compose.yml      # Swarm service deployment
|- index.html              # Application source
|-PROCESS                 # Pipeline execution steps



## ⚙️ Jenkins Pipeline Stages

1.The Jenkins pipeline automates the following stages:

2.Code Checkout – Pulls latest code from GitHub

3.Build Image – Builds Docker image using Dockerfile

4.Push Image – Pushes image to DockerHub

5.Deploy to Swarm – Deploys services using Docker Compose

6.High Availability – Containers run across multiple workers

## 🐳 Docker Swarm Deployment

-Jenkins runs on Docker Swarm Manager

-Containers are deployed on Worker1 & Worker2

-Swarm ensures:

-High availability

-Load balancing

-Automatic container rescheduling

## Steps
git clone https://github.com/gaju0203/JENKINS-DOCKER-PROJECT-HDFC.git
cd dockerproject-master
docker stack deploy -c docker-compose.yml hdfc-app

## Access the application
http://manager-or-worker-ip:exposed-port(80-81-82-83)
