# Dockerized Multi-Service Application

A production-ready three-tier web application fully containerized using Docker and Docker Compose. This project demonstrates best practices in microservices isolation, persistent storage, internal health checks, and multistage image optimization.

---

## 🏗️ Architecture

The application consists of three decoupled services running on a shared bridge network:

1. **Frontend:** Nginx Alpine web server serving static assets (HTML/CSS/JS).
2. **Backend:** Node.js & Express REST API with health check endpoints.
3. **Database:** MongoDB 6 with named volumes for data persistence.

---

## 🛠️ Prerequisites

Ensure you have the following installed on your host machine:
* [Docker Desktop / Engine](https://docs.docker.com/get-docker/) (v20.10+)
* [Docker Compose](https://docs.docker.com/compose/install/) (v2.0+)
* [Git](https://git-scm.com/)

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone <https://github.com/eishamubashir1/tynoc-proj2>
cd tynoc-proj



Frontend Application: http://localhost:8085
Backend API: http://localhost:5001
MongoDB: localhost:27018
