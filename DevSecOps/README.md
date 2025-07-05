# 🛠️ DevSecOps Practice Lab

Welcome to the **DevSecOps Lab** — a practical, containerized lab environment built using Docker Compose to help you master key DevOps and security tools in a safe, modular, and reproducible way.

## 🚀 Lab Overview

This lab includes the following services:

| Tool        | Purpose                                 | URL (default)         |
|-------------|-----------------------------------------|------------------------|
| GitLab      | Source control & DevSecOps integration  | http://localhost:8080 |
| Jenkins     | CI/CD pipeline automation               | http://localhost:8081 |
| SonarQube   | Static code analysis & code quality     | http://localhost:9000 |
| OWASP ZAP   | Dynamic security testing (DAST)         | http://localhost:8090 |
| Trivy       | Docker image vulnerability scanning     | CLI only               |
| Portainer   | Docker container management UI          | https://localhost:9443 |

---

## 🧱 Prerequisites

- Docker Engine & Docker Compose
- 8 GB+ RAM recommended for all services to run smoothly

---

## 🧪 Getting Started

### 1. Clone the Lab Repository

```bash
git clone https://github.com/YourUsername/devsecops-lab.git
cd devsecops-lab
```

### 2. Start the Lab

```bash
docker compose up -d
```

The first time may take a few minutes to pull all images.

## 🔐 Service Access

- Service	Default Login
- GitLab	Set up on first access
- Jenkins	Unlock with /var/jenkins_home/secrets/initialAdminPassword
- SonarQube	admin / admin
- Portainer	Set up on first access
- ZAP / Trivy	CLI only (run via exec)

## 🛠️ Example Use Cases

### ✅ GitLab

- Practice Git workflows, branches, and merge requests

- Simulate CI/CD trigger via .gitlab-ci.yml

### ✅ Jenkins

- Build pipelines for test, build, and deploy

- Integrate SonarQube and Trivy scanners

### ✅ SonarQube

- Run static code analysis from Jenkins

- Monitor bugs, code smells, vulnerabilities

### ✅ Trivy

- Scan Docker images for CVEs:

```bash
docker exec -it trivy trivy image jenkins/jenkins:lts
```

### ✅ OWASP ZAP

- Launch a manual or automated security scan on your local web app

```bash
docker exec -it zap zap-baseline.py -t http://yourapp:port
```

### 🧯 Stopping & Cleaning Up

```bash
docker compose down
```

# Optional: remove volumes

```bash
docker compose down --volumes
```

### 🧭 Learning Tips

- Document all pipeline configs in a personal wiki or GitHub repo

- Gradually add security gates into CI/CD pipelines

- Explore advanced integrations like Docker-in-Docker, GitLab Runners, or K8s in CI

### 🤝 Contributing

- Feel free to fork this repo, add your own lab modules, and submit a Pull Request!

### 📄 License

- MIT License — use freely, modify responsibly.
