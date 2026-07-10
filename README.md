<div align="center">

# FluentasAI

### Enterprise-Grade AI Platform for Complete Digital Transformation

**Self-Hosted • Zero Vendor Lock-In • Production-Ready**

[Quick Start](#-quick-start) • [Features](#-features) • [Documentation](#-documentation) • [Deployment](#-deployment-options) • [Contributing](#-contributing)

---

[![License](https://img.shields.io/badge/license-Proprietary-red.svg)](LICENSE)
[![Docker](https://img.shields.io/badge/docker-ready-blue.svg)](https://hub.docker.com)
[![Kubernetes](https://img.shields.io/badge/kubernetes-compatible-326CE5.svg)](https://kubernetes.io)
[![PostgreSQL](https://img.shields.io/badge/postgresql-17-336791.svg)](https://www.postgresql.org)
[![React](https://img.shields.io/badge/react-19-61DAFB.svg)](https://react.dev)

</div>

---

## 🎯 Overview

**FluentasAI** is a comprehensive, self-hostable AI-powered enterprise platform that combines intelligent agents, document management, collaboration tools, and 20+ specialized business applications — all deployable on your own infrastructure with complete data sovereignty.

Built for organizations that need enterprise-grade AI capabilities without sacrificing control, FluentasAI delivers a complete digital workspace that runs anywhere: on-premises, cloud, or hybrid.

### Why FluentasAI?

- **🔒 Complete Data Sovereignty** - Your data never leaves your infrastructure
- **🚀 Production-Ready** - Battle-tested in enterprise environments
- **🎨 20+ Enterprise Apps** - Complete business suite out of the box
- **🤖 Advanced AI** - RAG, multi-agent workflows, MCP integration
- **📊 Multi-Tenant** - Serve multiple organizations from one deployment
- **🔐 Enterprise Security** - NIST 800-53 compliant, full audit trails
- **⚡ Deploy Anywhere** - Docker, Kubernetes, EKS, AKS, GKE, or bare metal

---

## ✨ Features

### 🤖 AI & Automation

- **Visual Agent Builder** - No-code workflow designer with 40+ node types
- **RAG (Retrieval-Augmented Generation)** - Ground AI responses in your documents
- **MCP (Model Context Protocol)** - Integrate external tools and APIs
- **Multi-Provider Support** - AWS Bedrock, Azure OpenAI, Google Vertex AI, Anthropic, OpenAI, Ollama
- **Predictive RAG** - Learn from user behavior to improve retrieval
- **Deep Search** - Multi-hop reasoning over document collections
- **Workflow Automation** - Trigger actions based on events and schedules

### 📊 Enterprise Applications (20+ Built-In)

| Category | Applications |
|----------|-------------|
| **Productivity** | Chat, OfficeAI (Docs/Sheets/Slides), Wiki, Links, Minutes |
| **Communication** | TMail (Email Management), Send (Secure File Transfer) |
| **Project Management** | PMO (Portfolio), SprintR (Agile), TestR (QA), Five15 (Status Reports) |
| **Business Operations** | Contracts, Expenses, Proposals, SignFlow (E-Signature) |
| **HR & Talent** | HRM (HRIS), Recruitment, Performance, Training |
| **Supply Chain** | TrackR Supply (Inventory), MedSupply/SimOps, TrackR IT Assets |
| **Finance** | Accounting (GL/AP/AR), Tax Engine, Consolidations |
| **Healthcare** | RCM CodeFlow (Revenue Cycle), OSHA Inspect, SAR (Access Requests) |
| **Development** | AppDev (AI Code Assistant), Learn (LMS), Quizzy (Assessments) |
| **Support** | Helpdesk (Ticketing), Calendr (Scheduling) |
| **Analytics** | InstaViz (BI), Reports, Dashboards across all apps |
| **Entertainment** | Arcade (20+ games with gamification) |

### 🔐 Security & Compliance

- **Row-Level Security (RLS)** on every database table
- **Multi-Factor Authentication** - TOTP, SMS, Passkey, Smartcard
- **Single Sign-On** - SAML, Azure Entra ID, Google Workspace
- **NIST 800-53 Compliance** - Built-in compliance dashboard
- **Complete Audit Trail** - Every action logged with user, timestamp, IP
- **Virus Scanning** - ClamAV integration for all file uploads
- **Bot Detection** - Automated threat prevention
- **Encryption at Rest** - AES-256 for sensitive data
- **Role-Based Access Control** - Granular permissions per app and resource

### 📁 Document Management

- **OfficeAI Suite** - Full-featured editors for documents, spreadsheets, presentations, PDFs
- **Collaboration** - Real-time co-editing, comments, version history
- **Cloud Integration** - SharePoint, OneDrive, Google Drive, S3
- **AI-Powered** - Document generation, summarization, Q&A over documents
- **Advanced Editors** - Diagrams, mind maps, mockups, SVG, code, video, audio
- **User Storage** - Personal and shared workspaces with granular permissions

### 🎨 Modern User Experience

- **Responsive Design** - Works seamlessly on desktop, tablet, and mobile
- **Dark Mode** - System-aware with 7 color themes
- **Accessibility** - WCAG AA compliant, keyboard navigation, screen reader support
- **Offline Support** - Progressive Web App with offline capabilities
- **Real-Time Collaboration** - Live cursors, presence indicators, conflict resolution
- **Customizable** - Per-user preferences, layouts, and workflows

---

## 🚀 Quick Start

### Prerequisites

- **Docker** 24.0+ with Compose v2
- **4 vCPU, 8 GB RAM, 50 GB disk** (minimum)
- **Linux, macOS, or Windows** with PowerShell

### Installation (5 Minutes)

```bash
# 1. Clone the repository
git clone https://github.com/microhealthllc/fluenta.git
cd fluenta

# 2. Run the interactive setup wizard
# macOS/Linux:
make fluenta

# Windows:
fluenta.cmd

# 3. Follow the wizard prompts to:
#    - Choose deployment type (All-in-One recommended)
#    - Generate secure credentials
#    - Configure your domain/IP
#    - Create admin account

# 4. Start the platform
docker compose --profile selfhosted up -d

# 5. Access FluentasAI
# Open http://localhost:8080 in your browser
# Complete first-time setup at /setup
```

**That's it!** You now have a fully functional enterprise AI platform running locally.

### What You Get

After installation, you have immediate access to:

- ✅ AI Chat with multiple LLM providers
- ✅ 20+ enterprise applications
- ✅ Document management and collaboration
- ✅ Admin panel for configuration
- ✅ User management and RBAC
- ✅ Audit logging and compliance tools

---

## 🏗️ Architecture

### Technology Stack

| Layer | Technology |
|-------|-----------|
| **Frontend** | React 19, TypeScript, Vite, Tailwind CSS, shadcn/ui |
| **Backend** | Deno Edge Functions (Supabase-compatible) |
| **Database** | PostgreSQL 17 + PostgREST + pgvector + pg_cron + pg_net |
| **Authentication** | Custom JWT with MFA, SSO, Passkey, Smartcard |
| **Vector Search** | pgvector for RAG and semantic search |
| **Job Queue** | BullMQ with Redis for background processing |
| **Virus Scanning** | ClamAV with REST API |
| **Browser Automation** | Playwright MCP Server |
| **Container Runtime** | Docker / Docker Compose |
| **Orchestration** | Kubernetes (EKS, AKS, GKE, MicroK8s, k3s) |
| **Infrastructure as Code** | Helm, Terraform, Kustomize |
| **Monitoring** | OpenTelemetry, Prometheus-compatible metrics |

### System Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                        Load Balancer                        │
│                    (Ingress / ALB / NLB)                    │
└────────────────────────┬────────────────────────────────────┘
                         │
         ┌───────────────┴───────────────┐
         │                               │
┌────────▼────────┐            ┌────────▼────────┐
│    Frontend     │            │  Edge Functions │
│  (React + Vite) │            │  (Deno Runtime) │
│                 │            │                 │
│  • UI/UX        │            │  • Business     │
│  • Routing      │            │    Logic        │
│  • State Mgmt   │            │  • AI Agents    │
└────────┬────────┘            │  • Workflows    │
         │                     └────────┬────────┘
         │                              │
         └──────────────┬───────────────┘
                        │
         ┌──────────────▼──────────────┐
         │        PostgREST API        │
         │    (Auto-generated REST)    │
         └──────────────┬──────────────┘
                        │
         ┌──────────────▼──────────────┐
         │      PostgreSQL 17          │
         │                             │
         │  • pgvector (embeddings)    │
         │  • pg_cron (scheduling)     │
         │  • pg_net (webhooks)        │
         │  • RLS (row security)       │
         └─────────────────────────────┘

         ┌─────────────────────────────┐
         │    Supporting Services      │
         ├─────────────────────────────┤
         │  • Redis (BullMQ queue)     │
         │  • ClamAV (virus scan)      │
         │  • Playwright (automation)  │
         │  • Worker (background jobs) │
         └─────────────────────────────┘
```

### Multi-Tenancy

FluentasAI supports both **single-tenant** and **multi-tenant** deployments:

- **Single Tenant** - One organization per deployment (default)
- **Multi Tenant** - Multiple isolated organizations sharing infrastructure
- **Hybrid** - Mix of dedicated and shared resources

Multi-tenancy features:
- Organization-level data isolation
- Per-org RBAC and permissions
- Shared or dedicated storage
- Platform admin console
- Usage tracking and billing hooks
