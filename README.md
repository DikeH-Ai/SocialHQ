# SocialPilot HQ

AI-powered SaaS tool for distributed teams to **collaboratively schedule, refine, and automate social media posting**.  
Posts can be created **directly in the web app** or **synced from Google Sheets / Airtable**, then automatically published to connected social accounts with team-based content variations.

---

## 🚀 Overview

Distributed teams often struggle to maintain a consistent and coordinated social media presence.  
**SocialPilot HQ** solves this by providing:

- A **centralized team workspace** for managing posts.  
- **Direct scheduling via frontend** or syncing from **Google Sheets / Airtable**.  
- **AI-enhanced content refinement and variations** for better engagement.  
- **Role-based team management** (admins and members).  
- **Automated posting** across multiple social platforms.  

---

## ✨ Features

- ✅ User authentication & team management  
- ✅ Connect LinkedIn, Twitter/X, and Facebook accounts (per user)  
- ✅ OAuth2-based secure credential storage  
- ✅ Create scheduled posts directly from the web app  
- ✅ Sync posts from Google Sheets / Airtable  
- ✅ AI-powered content refinement & variation generation  
- ✅ Default images with ability to assign **different images per user**  
- ✅ Background job scheduling for automated posting  
- ✅ Dashboard with status tracking (pending, posted, failed)  

---

## 🛠️ Tech Stack

**Backend**
- FastAPI (Python 3.11+)
- PostgreSQL + SQLAlchemy
- Alembic (DB migrations)

**Scheduling & Jobs**
- Celery + Redis

**Frontend**
- Next.js (React) — for SaaS dashboard  
  *(or HTMX/Jinja2 for lightweight MVP)*

**Integrations**
- Google Sheets API  
- Airtable API  
- LinkedIn, Twitter/X, Facebook APIs  
- OpenAI GPT-4 (content refinement & variations)

**DevOps**
- Docker & Docker Compose  
- GitHub Actions (CI/CD)  
- Deployment: Fly.io / Railway / Render  

---

## 📂 Project Structure

socialpilot-hq/
├── backend/
│ ├── app/
│ │ ├── main.py # FastAPI entrypoint
│ │ ├── models/ # SQLAlchemy models
│ │ ├── api/ # REST endpoints
│ │ ├── services/ # Google, Airtable, Social posting
│ │ ├── tasks/ # Celery background workers
│ │ └── core/ # Config, auth, token mgmt
│ ├── Dockerfile
│ └── requirements.txt
├── frontend/
│ └── nextjs-app/ # Dashboard (Next.js)
├── scheduler/ # Job runners, cron config
├── docs/ # ERD, system diagrams
└── docker-compose.yml

## Usage

### 1. Sign up & create a team
- Invite team members  
- Assign roles (**admin/member**)  

### 2. Connect social media accounts
- Supported: **LinkedIn, Twitter/X, Facebook**  
- Each user manages their own credentials  

### 3. Add content
- Create scheduled posts **directly in the frontend**  
- Or sync from **Google Sheets / Airtable**  

### 4. Refine with AI
- Generate improved text  
- Create variations before posting  

### 5. Schedule & Automate
- Assign images (default or per-user)  
- Posts are auto-published at the scheduled time  

## 🤝 Contributing

Contributions are welcome! Please **fork the repo** and submit a **pull request**.  
For major changes, please **open an issue first** to discuss what you’d like to improve.

## 📜 License
This project is licensed under the **MIT License**.  
