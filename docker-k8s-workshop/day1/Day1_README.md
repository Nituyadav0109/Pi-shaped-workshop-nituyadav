# Day 1 – Introduction to Docker & Kubernetes: Containerization Basics

## 📅 Workshop Track
Pi-shaped Workshop – Docker & Kubernetes


## ✅ Objectives

- Create a simple Node.js REST API (`Hello, World!`)
- Write a Dockerfile to containerize the app
- Build and tag a Docker image
- Run the container locally on port `8080`
- Push the image to Docker Hub


## 🚀 Running Locally

### 1. Install dependencies

```bash
npm install
```

### 2. Start app locally

```bash
node app.js
```

### 3. Build Docker image

```bash
docker build -t nituyadav0109/hello-docker-node:day1 .
```

### 4. Run Docker container

```bash
docker run -p 8080:8080 nituyadav0109/hello-docker-node:day1
```

Visit: [http://localhost:8080](http://localhost:8080)

### 5. Push image to Docker Hub

```bash
docker login
docker push nituyadav0109/hello-docker-node:day1
```

> Note: You must have a Docker Hub account and be logged in to push images.

---

## 🔗 Docker Hub Image Link

[https://hub.docker.com/r/nituyadav0109/hello-docker-node]

---

## 📘 Core Concept Questions

### ✅ Why is Docker useful in building and deploying microservices?

Docker enables each microservice to run in its own container with all of its dependencies. This ensures consistent behavior across development, testing, and production environments. It simplifies scaling, isolates services for easier debugging and maintenance, and allows independent updates or rollbacks of individual services.

---

### ✅ What is the difference between a Docker image and a container?

- A **Docker image** is a read-only blueprint that contains the application and its environment.
- A **container** is a running instance of that image.

In scaling a web application, multiple containers are launched from the same image to distribute traffic and load.

---

### ✅ How does Kubernetes complement Docker at scale?

Kubernetes orchestrates and manages Docker containers across multiple hosts. It handles:

- Container deployment and scaling
- Load balancing and service discovery
- Auto-restart of failed containers (self-healing)
- Rolling updates and zero-downtime deployment

It ensures applications remain highly available and scalable in production.

---

### ✅ Note on Docker Hub

To push Docker images to Docker Hub:

1. Create a [Docker Hub account](https://hub.docker.com)
2. Log in via CLI with:

```bash
docker login
```

3. Then push your tagged image with:

```bash
docker push dockerhubusername/image-name:tag
```

You must be authenticated to push to your own repository.

---
