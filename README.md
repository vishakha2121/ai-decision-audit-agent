# 🔍 AI Enterprise Decision Audit Agent

> **Record every AI decision. Trace reasoning paths. Generate audit trails. Ensure governance & compliance.**

[![Python](https://img.shields.io/badge/Python-3.11+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.109+-009688?style=for-the-badge&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com)
[![React](https://img.shields.io/badge/React-18+-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://reactjs.org)
[![LangGraph](https://img.shields.io/badge/LangGraph-Latest-FF6F00?style=for-the-badge&logo=langchain&logoColor=white)](https://langchain.com)
[![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)

---

## 📖 Table of Contents

- [What is this?](#-what-is-this)
- [Key Features](#-key-features)
- [Architecture](#️-architecture)
- [Tech Stack](#️-tech-stack)
- [Quick Start](#-quick-start)
- [Project Structure](#-project-structure)
- [How It Works](#-how-it-works)
- [API Endpoints](#-api-endpoints)
- [Database Schema](#️-database-schema)
- [Screenshots](#-screenshots)
- [Key Concepts](#-key-concepts-demonstrated)
- [Roadmap](#️-roadmap)
- [Contributing](#-contributing)
- [License](#-license)
- [Author](#-author)

---

## 🎯 What is this?

**AI Enterprise Decision Audit Agent** is an AI-powered governance platform that captures every AI decision made in your system with complete transparency and auditability.

Modern AI systems are often **black boxes** — nobody knows *why* the AI made a particular decision. This creates problems for:

- 🏛️ **Regulatory Compliance** (GDPR, EU AI Act)
- 🔍 **Auditing** (internal & external)
- ⚖️ **Accountability** (who's responsible for AI decisions?)
- 🧠 **Explainability** (understanding AI reasoning)
- 📊 **Governance** (enterprise AI oversight)

This project solves that by recording:

| Component | What It Captures |
|---|---|
| 🧠 **Reasoning Paths** | Every thinking step of AI (via LangGraph) |
| 📜 **Audit Trails** | Immutable event log (Event Sourcing) |
| ✅ **Compliance Checks** | GDPR & EU AI Act validation |
| 📊 **Explainability Reports** | Human-readable decision breakdowns |
| 🔐 **Hash Chains** | Tamper-proof verification |

Perfect for **enterprises**, **developers**, and **researchers** building trustworthy AI systems.

---

## ✨ Key Features

| Feature | Description |
|---|---|
| 🧠 **Reasoning Path Capture** | Every AI thought step recorded via LangGraph state machine |
| 📜 **Event Sourcing** | Immutable, append-only audit log with SHA-256 hash chains |
| ✅ **Compliance Engine** | GDPR, EU AI Act, and custom rules auto-validation |
| 🔍 **Explainability UI** | Interactive reasoning flow + token usage + latency |
| 📊 **Audit Reports** | Generate PDF/CSV/JSON compliance reports |
| 🔐 **Tamper-Proof** | Cryptographic hash chain for every audit event |
| 🎨 **Modern UI** | React + Tailwind + shadcn-style components |
| ⚡ **Fast Backend** | Async FastAPI + SQLite (dev) |
| 🤖 **Gemini Integration** | Google Gemini API for LLM reasoning |
| 📈 **Dashboard Analytics** | Compliance scores, decision trends, activity charts |
| 🔎 **Advanced Filtering** | Search decisions by status, risk, date, compliance |
| 📤 **Export Options** | Download audit logs in CSV / JSON / PDF |
| 🎭 **Role-Based Views** | Admin, Auditor, User roles (RBAC-ready) |

---

## 🏗️ Architecture



---

## 🛠️ Tech Stack

### Backend
| Technology | Purpose |
|---|---|
| **Python 3.11+** | Core language |
| **FastAPI** | Async web framework |
| **SQLAlchemy 2.0** | ORM |
| **Alembic** | DB migrations |
| **Pydantic v2** | Data validation |
| **LangGraph** | AI agent state machine |
| **LangChain** | LLM orchestration |
| **Google Gemini API** | LLM reasoning |
| **SQLite** | Development database |
| **JWT** | Authentication |
| **Uvicorn** | ASGI server |

### Frontend
| Technology | Purpose |
|---|---|
| **React 18** | UI framework |
| **Vite** | Build tool |
| **Tailwind CSS** | Styling |
| **shadcn-style UI** | Components |
| **React Router v6** | Routing |
| **Axios** | HTTP client |
| **Zustand** | State management |
| **Recharts** | Data visualization |
| **Framer Motion** | Animations |
| **React Hook Form** | Form handling |

### DevOps & Tools
| Tool | Purpose |
|---|---|
| **Docker** | Containerization |
| **Docker Compose** | Multi-container orchestration |
| **Git** | Version control |
| **Postman** | API testing |
| **pytest** | Backend testing |
| **Vitest** | Frontend testing |

---

## 🚀 Quick Start

### Prerequisites

Before you begin, ensure you have:

- ✅ **Python 3.11+** — [Download](https://python.org/downloads)
- ✅ **Node.js 18+** — [Download](https://nodejs.org)
- ✅ **Git** — [Download](https://git-scm.com)
- ✅ **Gemini API Key** — [Get free](https://aistudio.google.com/app/apikey)

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/vishakha2121/ai-decision-audit-agent.git
cd ai-decision-audit-agent

cd backend

# Create virtual environment
python -m venv venv

# Activate it
# Windows:
venv\Scripts\activate
# macOS/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Setup environment variables
copy .env.example .env
# (Windows)
cp .env.example .env
# (macOS/Linux)

# Edit .env and add your GEMINI_API_KEY
notepad .env


# In a new terminal
cd frontend

# Install dependencies
npm install

# Setup environment
copy .env.example .env
# (Windows)
cp .env.example .env
# (macOS/Linux)

# Start dev server
npm run dev