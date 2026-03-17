# Example Voting App

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

## Screenshots
(Add your UI screenshots here)

## Author
Developed as part of DevOps learning

## Architecture

![Architecture diagram](architecture.excalidraw.png)

* A front-end web app in [Python](/vote) which lets you vote between two options
* A [Redis](https://hub.docker.com/_/redis/) which collects new votes
* A [.NET](/worker/) worker which consumes votes and stores them in…
* A [Postgres](https://hub.docker.com/_/postgres/) database backed by a Docker volume
* A [Node.js](/result) web app which shows the results of the voting in real time

## Notes

The voting application only accepts one vote per client browser. It does not register additional votes if a vote has already been submitted from a client.

This isn't an example of a properly architected perfectly designed distributed app... it's just a simple
example of the various types of pieces and languages you might see (queues, persistent data, etc), and how to
deal with them in Docker at a basic level.
