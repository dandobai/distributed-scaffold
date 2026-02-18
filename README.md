# Distributed Scaffold

A production-ready, highly scalable architectural foundation for JVM-based microservices. This repository serves as a **Template** for building distributed systems with a focus on observability, event-driven communication, and containerization.

## Architecture Overview

This scaffold provides a pre-configured infrastructure designed to support both **Java** and **Kotlin** Spring Boot applications, paired with a modern **Vue.js 3** frontend.

### Tech Stack
- **Backend Infrastructure:** Spring Boot (WebFlux ready)
- **Frontend:** Vue.js 3 (Vite, Pinia)
- **Messaging:** - **RabbitMQ:** For traditional point-to-point and pub/sub queuing.
  - **Apache Kafka:** For high-throughput event streaming.
- **Observability:** Prometheus & Grafana (pre-configured dashboards).
- **Load Balancing:** NGINX (configured for horizontal scaling).
- **Database:** PostgreSQL.
- **DevOps:** Docker Compose & GitHub Actions.

## Getting Started

### Prerequisites
- Docker & Docker Desktop
- Java 21+ / Kotlin 1.9+
- Node.js (for frontend development)

### Usage as a Template
1. Click the **"Use this template"** button on GitHub to create your new project.
2. Choose your project name (e.g., `ticket-system` or `stock-monitor`).
3. Generate your Spring Boot project via [Spring Initializr](https://start.spring.io/) and place it in the `/backend` folder.
4. Run the infrastructure:
   ```bash
   docker-compose up -d
   ```

## Observability
The scaffold includes a built-in monitoring stack. Once the containers are running, you can access:

* **Grafana:** `http://localhost:3000` (Default dashboards included)
* **Prometheus:** `http://localhost:9090`
* **RabbitMQ Management:** `http://localhost:15672` (Default login: `guest`/`guest`)

The backend is configured to be scraped by Prometheus via the `/actuator/prometheus` endpoint, ensuring real-time visibility into application performance.

## 🛡 License
This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---
*Developed as part of a high-scalability microservices portfolio.*