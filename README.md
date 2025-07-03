# 🧪 Cybersecurity & Development Learning Labs (Docker Compose)

Welcome to the Cybersecurity & Development Learning Labs repository! This repository is a collection of isolated, Docker Compose-based environments designed to help you experiment and learn various aspects of cybersecurity, DevOps, and web development in a safe and reproducible manner.

Each lab is self-contained within its own directory, making it easy to spin up specific environments without interfering with others.

## 🌟 Why Use This Repo?

- **Isolated Environments:** Each lab runs on its own Docker network, minimizing interference and ensuring a safe space for experimentation.
- **Reproducible:** Docker Compose ensures that your lab environment is consistent every time you spin it up.
- **Easy Setup:** Get complex lab setups running with just a few commands.
- **Hands-on Learning:** Practice offensive and defensive security, explore CI/CD pipelines, and build web applications from the ground up.

## 🚀 Getting Started

### Prerequisites

Before you begin, ensure you have the following installed on your system:

- Docker Desktop (for Windows/macOS) or Docker Engine (for Linux)
- Docker Compose

### How to Use a Lab

1. Clone this repository:

    ```bash
    git clone https://github.com/YourGitHubUsername/your-repo-name.git
    cd your-repo-name
    ```

    *(Replace `YourGitHubUsername` and `your-repo-name` with your actual GitHub details.)*

2. Navigate to the desired lab directory:

    ```bash
    cd cybersecurity-lab
    ```

3. Spin up the lab environment:

    ```bash
    docker compose up -d
    ```

    The `-d` flag runs the containers in detached mode. The first time you run this, Docker will download the necessary images, which might take some time.

4. Access the lab services:

    Refer to the specific lab's documentation for service access details.

5. Stop the lab environment:

    ```bash
    docker compose down
    ```

    To also remove any associated volumes (which will delete persistent data):

    ```bash
    docker compose down --volumes
    ```

    > ⚠️ Use `--volumes` with caution, as it deletes your lab progress.

## 📚 Lab Categories

### 🔒 Cybersecurity Labs (`cybersecurity-lab/`)

- **Kali Linux:** Containerized instance with security tools.
- **OWASP Juice Shop:** Insecure web app for hacking practice.
- **DVWA:** PHP/MySQL app with common vulnerabilities.
- **Metasploitable2:** Vulnerable Linux VM.

*Future additions: ELK, Splunk, malware analysis sandboxes, vulnerable APIs, etc.*

### ⚙️ DevOps Labs (`devops-lab/`)

- Jenkins CI/CD pipeline with vulnerable apps
- GitLab Runner setups
- Prometheus & Grafana monitoring
- Ansible/Terraform practice environments

### 🌐 Web Development Labs (`web-dev-lab/`)

- LAMP/LEMP stacks
- Node.js apps with vulnerable dependencies
- Microservices architectures

## ⚠️ Important Security Considerations

- **Isolated Networks:** Prevent vulnerable services exposure.
- **Resource Consumption:** Monitor CPU/RAM usage.
- **`privileged: true`:** Grants high-level access. Use only in isolated labs.
- **Ephemeral Nature:** Use volumes for persistence.
- **Host Security:** Keep your host system secure and updated.

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository.
2. Create a branch: `git checkout -b feature/new-lab-name`
3. Add your lab with a `docker-compose.yml` and `README.md`
4. Commit: `git commit -m 'Add new lab: new-lab-name'`
5. Push: `git push origin feature/new-lab-name`
6. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
