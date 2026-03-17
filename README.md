# Voting Application (Docker + Kubernetes)

This project demonstrates deployment of a microservices-based voting application using Docker and Kubernetes.

## Architecture
The application consists of multiple services:

- Vote (Python frontend) – allows users to vote
- Result (Node.js app) – displays voting results
- Worker (.NET service) – processes votes
- Redis – message queue
- PostgreSQL – database storage

## Technologies Used
- Docker (containerization)
- Docker Compose (local setup)
- Kubernetes (Deployments, Services)
- Microservices architecture

## How It Works
1. Users vote through the frontend application
2. Votes are stored temporarily in Redis
3. Worker service processes votes and stores them in PostgreSQL
4. Result service fetches data and displays real-time results

## Deployment
- Used Docker Compose for local multi-container setup
- Deployed services on Kubernetes using YAML configurations in `k8s-specifications/`

## Features
- Multi-service architecture
- Real-time result updates
- Scalable deployment using Kubernetes
- Containerized applications using Docker

## Architecture

![Architecture diagram](architecture.excalidraw.png)

## Author
Developed as part of DevOps learning
