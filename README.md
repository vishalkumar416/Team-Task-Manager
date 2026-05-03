# Team Task Manager

TaskFlow is a state-of-the-art, full-stack team management platform designed for high-performance teams. It features a stunning **Glassmorphism UI**, real-time activity tracking, and a robust role-based access system.

## ✨ Core Functionalities

### 🛡️ Advanced Authentication & Security
- **Dual-Layer Auth:** Secure traditional login/signup alongside seamless **Google OAuth** integration via Firebase.
- **Role-Based Access Control (RBAC):** 
    - **Admins:** Full control over project creation, task assignment, and system-wide visibility.
    - **Members:** Personalized dashboards focusing on their specific assignments and progress.

### 📊 Project & Task Management
- **Project Workspaces:** Centralized hubs for specific goals with automatic completion progress calculation.
- **Kanban-Style Task Board:** Dynamic status tracking for tasks through `To Do`, `In Progress`, and `Done`.
- **Task Claiming:** Open tasks can be claimed by team members with a single click.
- **Smart Deadlines:** Automatic tracking of overdue tasks with visual alerts.

### 📈 Dashboard & Analytics
- **Visual Analytics:** Interactive doughnut charts (Chart.js) showing real-time task distribution.
- **Live Audit Trail:** A persistent activity log tracking every system action (who did what and when).
- **Executive Summary:** Quick-view stats for total projects, active assignments, and critical overdue items.

### 🌐 Technical Features
- **Production-Ready DB:** Automated database schema generation and admin seeding.
- **RESTful API:** JSON endpoints for task retrieval (`/api/tasks`).
- **Timezone-Aware:** All activities are logged using UTC timezone-aware timestamps for global team consistency.

## 🛠️ Technology Stack

| Layer | Technology |
| :--- | :--- |
| **Backend** | Python 3.11+, Flask |
| **Frontend** | HTML5, Vanilla CSS3 (Glassmorphism), Jinja2 |
| **Database** | PostgreSQL (Production), SQLAlchemy ORM |
| **Auth** | Firebase Admin SDK, Google OAuth, Flask-Login |
| **Server** | Gunicorn (Production), Railway Cloud |
| **Analytics** | Chart.js |

## 🚀 Getting Started

### 1. Local Setup
```bash
# Install dependencies
pip install -r requirements.txt

# Configure your .env file
SECRET_KEY=your_secret
DATABASE_URL=sqlite:///database.db
ADMIN_USERNAME=admin
ADMIN_PASSWORD=admin_pass

# Run the app
python app.py
```

### 2. Live Deployment (Railway)
This project is pre-configured for **Railway** deployment using the included `Procfile`. 

**Required Environment Variables on Railway:**
- `DATABASE_URL`: Linked from your Railway Postgres service.
- `FIREBASE_SERVICE_ACCOUNT_JSON`: The full JSON content of your Firebase service account file.
- `SECRET_KEY`: A secure random string.

---
