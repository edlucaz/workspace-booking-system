<div align="center">

[![en](https://img.shields.io/badge/lang-en-red.svg?style=for-the-badge)](README.md)
[![pt-br](https://img.shields.io/badge/lang-pt--br-green.svg?style=for-the-badge)](README.pt-br.md)

# 🎆 Workspace Booking System

### Modern Workspace Scheduling System

<img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Travel%20and%20places/Cityscape%20at%20Dusk.png" alt="cityscape" width="100" />

![Status](https://img.shields.io/badge/Status-In%20Development-00ffff?style=for-the-badge&logo=linear&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.12-00ff00?style=for-the-badge&logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-5.1-ff00ff?style=for-the-badge&logo=django&logoColor=white)
![Vue](https://img.shields.io/badge/Vue.js-3-ffff00?style=for-the-badge&logo=vue.js&logoColor=black)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

```ascii
    ╭──────────────────────────────────────────╮
    │   ⚡ REFACTORING IN PROGRESS ⚡        │
    │                                          │
    │   2021 🠆 Original Project            │
    │   2026 🚀 Professional Version         │
    ╰──────────────────────────────────────────╯
```

</div>

---

## 🎯 About the Project

Professional refactoring of [Landing-Page---Fcamara (2021)](https://github.com/edlucaz/Landing-Page---Fcamara), transforming a static landing page into a **modern full-stack system** for workspace scheduling.

### 🎯 Project Goals

- ✅ **Professional Portfolio:** Demonstrate backend (Django REST Framework) and frontend (Vue 3) skills
- ✅ **Clean Code:** Follow best practices (SOLID, DRY, Clean Code)
- ✅ **Deploy-Ready:** Docker container configured from the start
- ✅ **Impactful Visual:** Modern fluorescent neon design
- ✅ **Complete Documentation:** Self-explanatory code with docstrings

---

## ✨ Features (MVP)

### 🔑 Authentication
- Login/Register with JWT
- Refresh tokens
- User profile

### 🏛️ Workspace Management
- Listing with filters (type, capacity, availability)
- Details of each workspace
- Search system

### 📅 Booking System
- Interactive calendar
- Time conflict validation
- Booking confirmation/cancellation

### 📊 User Dashboard
- My bookings (active and history)
- Booking cancellation
- Notifications

---

## 🛠️ Tech Stack

### Backend
```yaml
Language: Python 3.12
Framework: Django 5.1
API: Django REST Framework 3.15
Database: PostgreSQL 16 (via Docker)
Testing: pytest + pytest-django
Docs: drf-spectacular (Swagger/OpenAPI)
```

**Main Libraries:**
- `django-cors-headers` → CORS management
- `python-decouple` → Environment variables
- `psycopg2-binary` → PostgreSQL driver
- `dj-database-url` → Database config via URL

### Frontend
```yaml
Framework: Vue 3 (Composition API)
Build Tool: Vite
Styling: Tailwind CSS
State: Pinia
Requests: Axios
Routing: Vue Router
```

**Design System:**
- 🌈 Neon palette (cyan, magenta, yellow, green)
- 🌃 Dark background (#0a0e27)
- ✨ Shadows and glow effects
- 📱 100% responsive layout

### DevOps
```yaml
Containers: Docker + Docker Compose
CI/CD: GitHub Actions (future)
Deploy: Railway / Render (planned)
Version: Git (semantic commits)
```

---

## 🚀 Quick Start

### Prerequisites
```bash
# Install on Pop!_OS (or Debian/Ubuntu)
sudo apt update
sudo apt install python3.12 python3.12-venv docker.io docker-compose git

# Add your user to docker group (avoid sudo)
sudo usermod -aG docker $USER
newgrp docker  # Or restart session
```

### Installation (Hybrid Mode - Recommended)

#### 1️⃣ Clone Repository
```bash
git clone https://github.com/edlucaz/workspace-booking-system.git
cd workspace-booking-system
```

#### 2️⃣ Backend (Local Python + Docker PostgreSQL)
```bash
# Start PostgreSQL only
docker compose up db -d

# Configure backend
cd backend
python3.12 -m venv venv
source venv/bin/activate
pip install --upgrade pip
pip install -r requirements/base.txt

# Run migrations
python manage.py migrate

# Create superuser
python manage.py createsuperuser

# Start server
python manage.py runserver
# ✅ Backend: http://localhost:8000
# ✅ Admin: http://localhost:8000/admin
# ✅ Swagger: http://localhost:8000/api/docs
```

#### 3️⃣ Frontend (Local Node)
```bash
cd frontend
npm install
npm run dev
# ✅ Frontend: http://localhost:5173
```

### Or: All with Docker (Production)
```bash
docker compose up --build
# Wait ~2 minutes for initial build
```

---

## 📚 Documentation

### Architecture
```
workspace-booking-system/
├── backend/              # Django REST API
│   ├── core/            # Project settings
│   ├── bookings/        # Main app (Workspace + Booking)
│   ├── users/           # JWT authentication
│   └── requirements/    # Dependencies (base, dev, prod)
├── frontend/             # Vue 3 SPA
│   ├── src/
│   │   ├── components/  # Reusable components
│   │   ├── pages/       # Pages (routes)
│   │   ├── api/         # Axios config
│   │   └── stores/      # Pinia (state)
│   └── public/
├── docker/               # Dockerfiles
├── docker-compose.yml    # Container orchestration
└── README.md
```

### API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/api/workspaces/` | List available workspaces |
| `GET` | `/api/workspaces/{id}/` | Workspace details |
| `POST` | `/api/bookings/` | Create new booking |
| `GET` | `/api/bookings/` | My bookings |
| `PATCH` | `/api/bookings/{id}/` | Cancel booking |
| `POST` | `/api/auth/login/` | JWT authentication |
| `POST` | `/api/auth/register/` | Create account |

📖 **Interactive Documentation:** http://localhost:8000/api/docs

---

## 🪧 Development Progress

Follow the complete roadmap on [Linear](https://linear.app/next-change/project/workspace-booking-system-refatoracao-a33b0c5d556d):

### Phase 1: Structure 🟢 (Planned)
- [ ] [NEX-42](https://linear.app/next-change/issue/NEX-42) - Initial structure
- [ ] [NEX-43](https://linear.app/next-change/issue/NEX-43) - Django setup
- [ ] [NEX-44](https://linear.app/next-change/issue/NEX-44) - Docker + PostgreSQL

### Phase 2: Backend 🟡 (Planned)
- [ ] [NEX-45](https://linear.app/next-change/issue/NEX-45) - Django models
- [ ] [NEX-46](https://linear.app/next-change/issue/NEX-46) - DRF serializers
- [ ] [NEX-47](https://linear.app/next-change/issue/NEX-47) - ViewSets + URLs

### Phase 3: Frontend 🟡 (Planned)
- [ ] [NEX-48](https://linear.app/next-change/issue/NEX-48) - Vue 3 + Vite setup

---

## 🎨 Neon Design System

### Color Palette
```css
:root {
  /* Neon Colors */
  --neon-cyan: #00ffff;      /* Links, primary buttons */
  --neon-magenta: #ff00ff;   /* Highlights, alerts */
  --neon-yellow: #ffff00;    /* Warnings, notifications */
  --neon-green: #00ff00;     /* Success, confirmations */
  
  /* Backgrounds */
  --dark-bg: #0a0e27;        /* Main background */
  --dark-card: #1a1f3a;      /* Cards, modals */
  
  /* Neon Shadows */
  --shadow-cyan: 0 0 20px rgba(0, 255, 255, 0.5);
  --shadow-magenta: 0 0 20px rgba(255, 0, 255, 0.5);
}
```

### Typography
- **Font:** Inter (sans-serif)
- **Sizes:** 14px (body), 16px (buttons), 24px+ (headings)

---

## 🧑‍💻 Author

**Lucas Eduardo Rocha**
- 👨‍💻 Backend Developer | Python | Django
- 🎓 Bachelor's in IT (Univesp)
- 📧 Email: [24217901@aluno.univesp.br](mailto:24217901@aluno.univesp.br)
- 💙 GitHub: [@edlucaz](https://github.com/edlucaz)
- 🏛️ Araras-SP, Brazil

### Next Change Digital Solutions
Project developed by **Next Change**, focused on modern web solutions with Django and open-source technologies.

---

## 📜 License

MIT License - See [LICENSE](LICENSE) for details.

---

## 🔗 Useful Links

- 📝 [Project on Linear](https://linear.app/next-change/project/workspace-booking-system-refatoracao-a33b0c5d556d)
- 🐛 [Report Bug](https://github.com/edlucaz/workspace-booking-system/issues)
- 💡 [Suggest Feature](https://github.com/edlucaz/workspace-booking-system/issues)
- 📖 [Django Documentation](https://docs.djangoproject.com/en/5.1/)
- 📖 [Vue 3 Documentation](https://vuejs.org/guide/introduction.html)

---

<div align="center">

### ✨ Star the project if it helped you! ⭐

![Workspace Booking](https://img.shields.io/github/stars/edlucaz/workspace-booking-system?style=social)

---

<img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Laptop.png" alt="laptop" width="50" />

*From a static landing page to a professional full-stack system.*

**2021 → 2026 | Continuous Evolution** 🚀

</div>
