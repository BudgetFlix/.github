<!-- PROJECT LOGO -->
<br />
<div align="center">

<h3 align="center">BudgetFlix</h3>

  <p align="center">
    Modern media automation and content processing ecosystem.
    <br />
    <br />
    <a href="https://github.com/BudgetFlix">View Organization</a>
    ·
    <a href="https://github.com/BudgetFlix/issues">Report Bug</a>
    ·
    <a href="https://github.com/BudgetFlix/issues">Request Feature</a>
  </p>
</div>

---

<!-- TABLE OF CONTENTS -->
<details>
  <summary>📚 Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#architecture">Architecture</a></li>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#development-philosophy">Development Philosophy</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
  </ol>
</details>

---

# About The Project

BudgetFlix is a modular media automation ecosystem focused on scalable video uploading, processing, scheduling, and platform automation.

The organization is designed around lightweight services and workers that can operate independently while communicating through messaging systems such as RabbitMQ.

The long-term goal is to build a complete self-hosted media pipeline platform with:

- Media uploading
- Distributed workers
- Video processing
- Dashboard management
- Monitoring & analytics
- Scheduling systems
- Platform integrations
- Automation tooling

The ecosystem is currently in active early-stage development.

---

## Architecture

The platform follows a service-oriented architecture.

```mermaid
flowchart TD

    UI[Desktop / UI App]
    API[API / Gateway]
    MQ[RabbitMQ]

    W1[Worker A]
    W2[Worker B]

    EXT[External Platforms]

    UI --> API
    API --> MQ

    MQ --> W1
    MQ --> W2

    W1 --> EXT
    W2 --> EXT
````

The ecosystem is intentionally designed to support:

* Horizontal scaling
* Service isolation
* Queue-based processing
* Future cloud deployments
* Local self-hosted development

---

## Built With

<div align="left">

### Backend

![Go](https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white)
![Java](https://img.shields.io/badge/Java-E76F00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?style=for-the-badge&logo=rabbitmq&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

### Frontend

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-38BDF8?style=for-the-badge&logo=tailwindcss&logoColor=white)
![DaisyUI](https://img.shields.io/badge/DaisyUI-5A0EF8?style=for-the-badge&logo=daisyui&logoColor=white)
![Tauri](https://img.shields.io/badge/Tauri-FFC131?style=for-the-badge&logo=tauri&logoColor=black)

### Infrastructure

![Docker Compose](https://img.shields.io/badge/Docker_Compose-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)

</div>

---

# Getting Started

## Prerequisites

Before starting, make sure you have installed:

* Docker
* Docker Compose
* Git
* Go (for worker development)
* Node.js (for frontend applications)
* Java 21+ (for legacy services)

---

## Installation

Clone the organization repositories:

```bash
git clone https://github.com/BudgetFlix/<repository-name>.git
```

Enter the project directory:

```bash
cd <repository-name>
```

Start services with Docker:

```bash
docker compose up -d
```

---

# Projects

Current and planned repositories inside the ecosystem:

| Repository       | Description                         |
| ---------------- | ----------------------------------- |
| `worker`         | Distributed media processing worker |
| `media-uploader` | Desktop uploader application        |
| `dashboard`      | Web management dashboard            |
| `gateway`        | API gateway and routing             |
| `monitoring`     | Metrics and monitoring services     |
| `shared`         | Shared contracts and utilities      |

---

# Roadmap

* [x] Initial organization setup
* [x] RabbitMQ-based communication
* [x] Dockerized development environment
* [ ] Go worker migration
* [ ] Media processing pipeline
* [ ] Dashboard UI
* [ ] Upload management
* [ ] Video metadata management
* [ ] Distributed task orchestration
* [ ] Monitoring stack
* [ ] Multi-platform integrations
* [ ] Authentication system
* [ ] CI/CD pipelines

---

# Development Philosophy

BudgetFlix is being built with a focus on:

* Simplicity over unnecessary abstraction
* Service isolation
* Queue-driven architecture
* Fast local development
* Self-hosting support
* Scalable infrastructure
* Incremental migration from legacy systems

The project heavily emphasizes practical engineering and iterative development.

---

# Contributing

Contributions, ideas, and feedback are welcome.

If you'd like to contribute:

1. Fork the repository
2. Create your feature branch

```bash
git checkout -b feature/amazing-feature
```

3. Commit your changes

```bash
git commit -m "Add amazing feature"
```

4. Push to the branch

```bash
git push origin feature/amazing-feature
```

5. Open a Pull Request

---

# License

Distributed under the MIT License.

---

<div align="center">
Built with ❤️ by BudgetFlix
</div>
