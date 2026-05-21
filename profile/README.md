<!-- HERO -->
<div align="center">

<p align="center">
  <img
    src="https://raw.githubusercontent.com/budgetflix/.github/main/assets/logo_and_name_big.png"
    width="620"
    alt="BudgetFlix"
  />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Status-Early%20Development-E50914?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Architecture-Service%20Oriented-111827?style=for-the-badge" />
</p>

<h3>
  Modular streaming, media processing, and automation ecosystem.
</h3>

<p align="center">
  BudgetFlix is an early-stage platform focused on scalable media workflows,
  queue-driven processing, streaming infrastructure, and self-hosted tooling.
</p>

<br>

</div>



# Tech Stack

## Backend & Processing

<p>

<img src="https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white" />
<img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" />
<img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" />
<img src="https://img.shields.io/badge/RabbitMQ-FF6600?style=for-the-badge&logo=rabbitmq&logoColor=white" />
<img src="https://img.shields.io/badge/FFmpeg-007808?style=for-the-badge&logo=ffmpeg&logoColor=white" />

</p>

## Frontend

<p>

<img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" />
<img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" />
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" />
<img src="https://img.shields.io/badge/Tamagui-24A1C1?style=for-the-badge" />
<img src="https://img.shields.io/badge/Tauri-FFC131?style=for-the-badge&logo=tauri&logoColor=black" />

</p>

## Infrastructure

<p>

<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/Docker_Compose-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" />
<img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" />

</p>

---

# Overview

BudgetFlix is a modular media ecosystem built around lightweight services, isolated workers, and queue-based communication.

The platform currently focuses on:

- media uploads
- distributed processing
- HLS video generation
- streaming workflows
- infrastructure orchestration
- automation tooling

The architecture is intentionally designed so every service can evolve independently while still fitting into a larger scalable system.

---

# Ecosystem Architecture

```mermaid
flowchart LR

    USER[User]
    UI[Frontend / Desktop Apps]
    API[API Layer]
    MQ[RabbitMQ]

    WORKER[Media Workers]
    STORAGE[(Media Storage)]
    STREAM[HLS Streaming]

    USER --> UI
    UI --> API
    API --> MQ

    MQ --> WORKER
    WORKER --> STORAGE

    STORAGE --> STREAM
    STREAM --> USER
```

---

# Repositories

| Repository | Description |
| --- | --- |
| [`frontend`](https://github.com/BudgetFlix/frontend) | Next.js streaming frontend monorepo |
| [`api`](https://github.com/BudgetFlix/api) | Spring Boot backend and upload orchestration |
| [`worker`](https://github.com/BudgetFlix/worker) | Go-based FFmpeg media processing worker |
| [`media-uploader`](https://github.com/BudgetFlix/media-uploader) | Tauri desktop uploader |
| [`infra`](https://github.com/BudgetFlix/infra) | Docker infrastructure and orchestration |

---

# Repository Roles

## [`frontend`](https://github.com/BudgetFlix/frontend)

<p>

<img src="https://img.shields.io/badge/Next.js-14-000000?style=flat-square&logo=nextdotjs&logoColor=white" />
<img src="https://img.shields.io/badge/React-18-20232A?style=flat-square&logo=react&logoColor=61DAFB" />
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" />
<img src="https://img.shields.io/badge/HLS.js-Video-FF5A5F?style=flat-square" />
<img src="https://img.shields.io/badge/Tamagui-UI-24A1C1?style=flat-square" />

</p>

Streaming frontend foundation focused on:

- movie browsing
- HLS playback
- reusable UI architecture
- scalable frontend packages

---

## [`api`](https://github.com/BudgetFlix/api)

<p>

<img src="https://img.shields.io/badge/Java-17-ED8B00?style=flat-square&logo=openjdk&logoColor=white" />
<img src="https://img.shields.io/badge/Spring_Boot-3.1-6DB33F?style=flat-square&logo=springboot&logoColor=white" />
<img src="https://img.shields.io/badge/RabbitMQ-AMQP-FF6600?style=flat-square&logo=rabbitmq&logoColor=white" />
<img src="https://img.shields.io/badge/Maven-Build-C71A36?style=flat-square&logo=apachemaven&logoColor=white" />

</p>

Backend orchestration layer responsible for:

- upload job creation
- RabbitMQ publishing
- movie metadata
- stream path lookup
- processing state management

---

## [`worker`](https://github.com/BudgetFlix/worker)

<p>

<img src="https://img.shields.io/badge/Go-1.24-00ADD8?style=flat-square&logo=go&logoColor=white" />
<img src="https://img.shields.io/badge/FFmpeg-HLS-007808?style=flat-square&logo=ffmpeg&logoColor=white" />
<img src="https://img.shields.io/badge/RabbitMQ-Consumer-FF6600?style=flat-square&logo=rabbitmq&logoColor=white" />
<img src="https://img.shields.io/badge/Docker-Containerized-2496ED?style=flat-square&logo=docker&logoColor=white" />

</p>

Distributed media processing worker with:

- FFmpeg HLS pipelines
- filesystem job lifecycle
- queue acknowledgement handling
- graceful shutdown support

---

## [`media-uploader`](https://github.com/BudgetFlix/media-uploader)

<p>

<img src="https://img.shields.io/badge/Tauri-Desktop-FFC131?style=flat-square&logo=tauri&logoColor=black" />
<img src="https://img.shields.io/badge/React-UI-20232A?style=flat-square&logo=react&logoColor=61DAFB" />
<img src="https://img.shields.io/badge/Rust-Native-000000?style=flat-square&logo=rust&logoColor=white" />
<img src="https://img.shields.io/badge/SFTP-Upload-2563EB?style=flat-square" />

</p>

Desktop-first upload tool featuring:

- local media uploads
- SFTP transfer flow
- API integration
- native desktop runtime

---

## [`infra`](https://github.com/BudgetFlix/infra)

<p>

<img src="https://img.shields.io/badge/Docker-Compose-2496ED?style=flat-square&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/RabbitMQ-Infrastructure-FF6600?style=flat-square&logo=rabbitmq&logoColor=white" />
<img src="https://img.shields.io/badge/Linux-Environment-FCC624?style=flat-square&logo=linux&logoColor=black" />
<img src="https://img.shields.io/badge/GitHub_Actions-CI/CD-2088FF?style=flat-square&logo=githubactions&logoColor=white" />

</p>

Infrastructure repository containing:

- Docker Compose environments
- shared networking
- queue infrastructure
- deployment workflow foundations

---

# Processing Flow

```mermaid
flowchart LR

    A[Uploader / Frontend]
    B[API]
    C[RabbitMQ]
    D[Worker]
    E[FFmpeg HLS Output]
    F[Streaming Client]

    A --> B
    B --> C
    C --> D
    D --> E
    E --> F
```

---

# Design Principles

BudgetFlix is being built around a few core ideas:

- small isolated services
- queue-driven workflows
- reproducible local infrastructure
- practical engineering over overengineering
- scalable architecture without early complexity
- self-hosted friendly deployments
- incremental development

The goal is to build systems that remain understandable as the platform grows.

---

# Roadmap

- [x] RabbitMQ messaging
- [x] Dockerized local infrastructure
- [x] Initial upload pipeline
- [x] HLS media processing
- [x] Frontend monorepo foundation
- [ ] Streaming authentication
- [ ] Monitoring and metrics
- [ ] Distributed worker scaling
- [ ] Upload dashboards
- [ ] Search and metadata systems
- [ ] Multi-environment deployments
- [ ] Kubernetes support
- [ ] Automated media workflows

---

# Development Status

BudgetFlix is currently in an early but functional foundation stage.

Core architecture pieces already exist:

- frontend
- backend API
- upload tooling
- queue infrastructure
- media processing pipeline

The current focus is improving integration between services while expanding the streaming and automation workflow.

---

# Contributing

Contributions, ideas, and feedback are welcome.

```bash
git checkout -b feature/my-feature
git commit -m "Add my feature"
git push origin feature/my-feature
```

Then open a Pull Request.

---

# Philosophy

> Build the pipeline first.  
> Make it reliable.  
> Scale it later.

---

<div align="center">

Built by <b>PeterKokenyessy</b>

</div>
