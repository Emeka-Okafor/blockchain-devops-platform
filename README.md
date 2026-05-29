# Blockchain DevOps Platform

Production-ready DevOps reference architecture for managing **blockchain nodes**, **RPC infrastructure**, CI/CD, monitoring, and multi-cloud deployments.

This project demonstrates real-world skills for DevOps / Platform Engineer roles (especially those involving blockchain infrastructure).

## Key Features

- CI/CD Pipelines using GitHub Actions
- Docker containerization for blockchain nodes
- RPC Proxy with rate limiting
- Monitoring & Logging (Prometheus + Grafana)
- High Availability & Scalability patterns

## Project Structure

├── docker-compose.yml              # Main stack (Node + RPC + Monitoring)
├── docker/
│   ├── docker-compose.yml
│   └── nginx.conf
├── monitoring/
│   ├── docker-compose.monitoring.yml
│   └── prometheus.yml
├── .github/workflows/
│   └── ci-cd.yml
└── README.md


## Quick Start

```bash
# 1. Clone the repo
git clone https://github.com/YOUR-USERNAME/blockchain-devops-platform.git
cd blockchain-devops-platform

# 2. Start the full stack
docker compose up -d

# 3. Check services
curl http://localhost:8080/health          # Should return OK
curl http://localhost:9090                 # Prometheus
curl http://localhost:3000                 # Grafana (default login: admin/admin)

Access Points

RPC Endpoint: http://localhost:8080
Prometheus: http://localhost:9090
Grafana: http://localhost:3000

Tech Stack

Containerization: Docker, Docker Compose
Blockchain: Reth (Ethereum-compatible node)
CI/CD: GitHub Actions
Monitoring: Prometheus + Grafana
Proxy: Nginx (with rate limiting)
