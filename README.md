# 🇮🇳 Eureka AI For Bharat

<div align="center">

**An AI-Powered Short Drama & Content Production Platform — Built for India**

[![Go Version](https://img.shields.io/badge/Go-1.23+-00ADD8?style=flat&logo=go)](https://golang.org)
[![Vue Version](https://img.shields.io/badge/Vue-3.x-4FC08D?style=flat&logo=vue.js)](https://vuejs.org)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Made for India](https://img.shields.io/badge/Made%20for-Bharat%20🇮🇳-FF9933?style=flat)](https://github.com/Aryanite/Eureka_Ai_For_Bharat)

[Features](#-features) • [Architecture](#-architecture) • [Quick Start](#-quick-start) • [Roadmap](#-roadmap)

</div>

---

## 📖 About

**Eureka AI For Bharat** is a full-stack AI-powered content production platform designed with Indian creators in mind. It automates the complete short-drama production pipeline — from script writing and character generation to storyboarding, scene composition, and final video rendering — with native multi-language support for Indian regional languages.

Built on **Go + Vue 3** with a clean Domain-Driven Design (DDD) architecture, Eureka brings enterprise-grade AI tooling to indie creators, studios, and storytellers across Bharat.

---

## ✨ Features

### 🎭 Character & World Building
- AI-generated character portraits tailored to Indian aesthetics
- Batch character creation from script analysis
- Character library management with custom uploads
- Scene and prop generation grounded in Indian cultural contexts

### 📝 Script & Story Intelligence
- Parse and analyze scripts using large language models
- AI-assisted script generation and editing
- Multi-language support: Hindi, Tamil, Telugu, Bengali, Marathi, and more
- Automatic scene breakdown and shot design

### 🎨 Storyboard Production
- Auto-generate storyboards from parsed scripts
- Text-to-image generation for each scene
- Frame type selection: first frame / key frame / last frame / panel
- Grid-based image editor for fine-tuning

### 🎥 Video Generation & Editing
- Text-to-video and image-to-video generation
- Automatic video composition and merging
- Timeline editor for professional editing
- Audio extraction and synchronization

### 🌐 Platform & Infrastructure
- Multi-AI provider support (AWS Bedrock, OpenAI-compatible endpoints)
- Role-based settings and configuration management
- Real-time task queue with status tracking
- Cloud-native deployment (Docker, AWS Lambda, ECS)
- Prometheus-compatible stats and monitoring endpoint

---

## 🏗️ Architecture

Eureka follows **Domain-Driven Design (DDD)** with strict layer separation:

```
eureka-ai-for-bharat/
├── api/                    # HTTP handlers (Gin)
│   ├── handlers/           # Route handlers per domain
│   ├── middlewares/        # CORS, logging, rate limiting
│   └── routes/             # Route registration
├── application/
│   └── services/           # Business logic / use cases
├── domain/
│   ├── models/             # Core domain entities
│   └── repository.go       # Repository interfaces
├── infrastructure/
│   ├── database/           # SQLite / DynamoDB implementations
│   ├── external/           # Third-party API clients
│   ├── scheduler/          # Background task scheduler
│   └── storage/            # File storage abstraction
├── pkg/
│   ├── ai/                 # AI provider clients (Bedrock, etc.)
│   ├── image/              # Image processing utilities
│   ├── video/              # Video processing utilities
│   └── config/             # Configuration loader
├── web/                    # Vue 3 frontend (Vite + Tailwind)
├── migrations/             # SQL migration files
├── cmd/
│   ├── lambda/             # AWS Lambda entrypoint
│   └── migrate/            # DB migration runner
└── main.go                 # Local server entrypoint
```

**Tech Stack:**

| Layer | Technology |
|---|---|
| Backend | Go 1.23+, Gin, GORM |
| Frontend | Vue 3, Vite, Tailwind CSS, Pinia |
| Database | SQLite (local), DynamoDB (cloud) |
| AI Providers | AWS Bedrock (Nova, Titan), OpenAI-compatible |
| Deployment | Docker, AWS Lambda, AWS ECS/Fargate |
| Auth / Config | YAML config, environment variables |

---

## 🚀 Quick Start

### Prerequisites
- Go 1.23+
- Node.js 18+ / pnpm
- Docker (optional)

### 1. Clone the Repository

```bash
git clone https://github.com/Aryanite/Eureka_Ai_For_Bharat.git
cd Eureka_Ai_For_Bharat
```

### 2. Configure

```bash
cp configs/config.example.yaml configs/config.yaml
# Edit configs/config.yaml with your AI provider keys and settings
```

### 3. Run the Backend

```bash
go mod download
go run main.go
```

The API server starts at `http://localhost:8080`.

### 4. Run the Frontend

```bash
cd web
pnpm install
pnpm dev
```

The frontend starts at `http://localhost:5173`.

### 5. Docker (All-in-One)

```bash
docker-compose up --build
```

---

## 🗺️ Roadmap

- [x] Core drama/project management
- [x] AI script parsing and generation
- [x] Character and scene image generation
- [x] Storyboard auto-generation
- [x] Video generation pipeline
- [x] AWS Bedrock multi-model support
- [ ] Hindi / regional language UI localization
- [ ] Mobile-responsive frontend
- [ ] Creator marketplace & asset sharing
- [ ] Real-time collaboration for teams
- [ ] On-device AI inference support (edge)
- [ ] Bharat-specific content safety filters

---

## 🤝 Contributing

Contributions are welcome! Whether you're fixing a bug, adding a feature, translating the UI into a regional language, or improving documentation — every contribution helps.

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/my-feature`
3. Commit your changes: `git commit -m 'feat: add my feature'`
4. Push to the branch: `git push origin feature/my-feature`
5. Open a Pull Request

---

## 📄 License

This project is licensed under the **MIT License**. See [LICENSE](LICENSE) for details.

---

<div align="center">

Built with ❤️ for Indian Creators &nbsp;•&nbsp; **Eureka AI For Bharat**

</div>
