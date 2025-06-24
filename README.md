# n8n Local Docker Setup with PostgreSQL, Redis, and WAHA

This repository contains a ready-to-use Docker setup for running [n8n](https://n8n.io/) locally with **PostgreSQL**, **Redis**, and **WAHA** (WhatsApp HTTP API), fully containerized and secured with basic authentication.

## 🚀 Quick Start

### 1. Clone the repo

```bash
git clone https://github.com/yourusername/n8n-local.git
cd n8n-local
```

### 2. Create your `.env` file

Copy and edit environment variables as needed:

```bash
cp .env.example .env
```

Or manually create `.env`:

```env
GENERIC_TIMEZONE=America/Sao_Paulo
N8N_BASIC_AUTH_ACTIVE=true
N8N_BASIC_AUTH_USER=admin
N8N_BASIC_AUTH_PASSWORD=your_strong_password
N8N_HOST=localhost
N8N_PORT=5678
WAHA_API_TOKEN=your_waha_token
```

### 3. Run everything with Docker

```bash
docker-compose up -d
```

Then open:

- n8n: `http://localhost:5678`
- WAHA API: `http://localhost:3000`
- WAHA Webhook: `http://localhost:3001`

Login to n8n with the credentials from your `.env`.

---

## 🧠 Services Overview

- **n8n** – Workflow automation tool
- **PostgreSQL** – Persistent DB storage for n8n
- **Redis** – Queue manager for high-performance workflow execution
- **WAHA** – WhatsApp HTTP API integration

---

## 📂 Project Structure

```bash
.
├── .env              # Your environment variables (not committed)
├── .gitignore
├── docker-compose.yml
└── README.md
```

---

## 🛑 Do not commit `.env`

Make sure `.env` is included in your `.gitignore` to avoid leaking secrets.

---

## 📜 License

MIT — use at your own risk and customize as needed.
