# 🧪 Lab 02 — Dockerizing a Flask Microservice and Local Development Environment Setup

This document explains the steps taken to complete **Lab 02**, based on the existing files in this repository.

---

## 🎯 Lab Goals
- Containerize a Flask microservice using **Docker**.
- Create a **local development stack** using **Docker Compose** (NGINX + MySQL).
- Verify connectivity and persistence.
- Document build and run results with screenshots.

---

## 🧩 Task 1 — Dockerizing the Flask Microservice

### ⚙️ Steps

1. **Navigate to the Flask app directory**
   ```bash
   cd Lab2/task1-flask
docker build -t lab2-flask:latest . # to build the image
docker run --rm -d -p 8080:5000 --name lab2-flask lab2-flask:latest # to run it
curl http://localhost:8080 # to test and see the output

Task 2 — Docker Compose: NGINX + MySQL Stack

docker compose up -d  # to start all services
docker ps # to see runnig containers
curl http://localhost:8080 # to test and check the results
