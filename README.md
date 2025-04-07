# 🐳 Full-Stack Java App Deployment with Docker & Kubernetes on AWS

This project demonstrates end-to-end DevOps practices using **Docker**, **Docker Compose**, and **Kubernetes (Kops)** to deploy a full-stack Java web application on AWS. It includes an NGINX web layer, Tomcat application layer, MySQL database, Memcached for caching, and RabbitMQ for messaging.

---

## 🧱 Project Architecture

### 🔹 Components

| Service    | Description                                      | Tech Stack             |
|------------|--------------------------------------------------|------------------------|
| `web`      | Load balancer / frontend                         | NGINX                  |
| `app`      | Java app build & deploy                          | Maven + Tomcat         |
| `database` | Data layer                                       | MySQL 8                |
| `cache`    | Caching                                          | Memcached              |
| `queue`    | Messaging queue                                  | RabbitMQ with UI       |

---

## 🚀 Technologies Used

- **Build Tool:** Maven
- **Database:** MySQL
- **Web Server:** Tomcat
- **Cache:** Memcached
- **Queue:** RabbitMQ
- **Containerization:** Docker, Docker Compose
- **Orchestration:** Kubernetes with Kops
- **Cloud:** AWS EC2, S3, Route53
- **Domain:** GoDaddy (subdomain for ingress)

---

## 📦 Docker Setup

### ✅ Docker Images Built

- `web` - NGINX
- `app` - Spring Boot + Tomcat (from Maven build)
- `database` - MySQL with SQL dump preloaded

Each image is pushed to your Docker Hub account.

```bash
# Sample build & push
docker build -t sahil9079/vprofileapp ./app
docker push sahil9079/vprofileapp



