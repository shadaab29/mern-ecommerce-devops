# 🛍️ MERN E-commerce DevOps Project

A full-featured MERN stack (MongoDB, Express, React, Node.js) e-commerce app containerized with Docker and deployed using GitHub Actions CI/CD. Includes monitoring with Prometheus and Grafana.

---

## 📦 Tech Stack

| Layer      | Technology                  |
|------------|-----------------------------|
| Frontend   | React                       |
| Backend    | Node.js + Express           |
| Database   | MongoDB                     |
| Monitoring | Prometheus + Grafana        |
| CI/CD      | GitHub Actions + Docker     |
| Hosting    | AWS EC2 (via SSH Deployment) |

---

## 🧱 Project Structure

mern-ecommerce-devops/
├── backend/ # Node.js API with MongoDB
├── frontend/ # React UI
├── monitoring/ # Prometheus config
├── .github/workflows/ # GitHub Actions CI/CD
├── docker-compose.yml # Multi-container setup
├── README.md # You're here

---

## 🚀 Local Development Setup

### ✅ Prerequisites

- Docker & Docker Compose
- Node.js (optional)
- Git

### 🔧 Clone & Setup

```bash
git clone https://github.com/<your-username>/mern-ecommerce-devops.git
cd mern-ecommerce-devops

# Copy environment configs
cp env/backend.env backend/.env
cp env/frontend.env frontend/.env

# Build and run containers
docker-compose up --build


🌐 URLs
Service	URL
React App	http://localhost:3000
API	http://localhost:5000/api/products
MongoDB	localhost:27017
Prometheus	http://localhost:9090
Grafana	http://localhost:3001

📊 Monitoring
Prometheus scrapes metrics from the backend (port 5000)

Grafana can be accessed at http://localhost:3001

You can add custom dashboards for container metrics, API health, etc.

🔄 GitHub Actions CI/CD
🛠️ Workflow File
Located at: .github/workflows/deploy.yaml

🔐 Required GitHub Secrets
Name	Description
EC2_HOST	Public IP or DNS of your EC2
EC2_SSH_KEY	Your private SSH key for EC2