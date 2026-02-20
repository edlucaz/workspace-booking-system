<div align="center">

[![en](https://img.shields.io/badge/lang-en-red.svg?style=for-the-badge)](README.md)
[![pt-br](https://img.shields.io/badge/lang-pt--br-green.svg?style=for-the-badge)](README.pt-br.md)

# 🎆 Workspace Booking System

### Sistema Moderno de Agendamento de Espaços de Trabalho

<img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Travel%20and%20places/Cityscape%20at%20Dusk.png" alt="cityscape" width="100" />

![Status](https://img.shields.io/badge/Status-Em%20Desenvolvimento-00ffff?style=for-the-badge&logo=linear&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.12-00ff00?style=for-the-badge&logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-5.1-ff00ff?style=for-the-badge&logo=django&logoColor=white)
![Vue](https://img.shields.io/badge/Vue.js-3-ffff00?style=for-the-badge&logo=vue.js&logoColor=black)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

```ascii
    ╭──────────────────────────────────────────╮
    │   ⚡ REFATORANDO EM PROGRESSO ⚡       │
    │                                          │
    │   2021 🠆 Projeto Original             │
    │   2026 🚀 Versão Profissional          │
    ╰──────────────────────────────────────────╯
```

</div>

---

## 🎯 Sobre o Projeto

Refatoração profissional do [Landing-Page---Fcamara (2021)](https://github.com/edlucaz/Landing-Page---Fcamara), transformando uma landing page estática em um **sistema full-stack moderno** de agendamento de espaços de trabalho.

### 🎯 Objetivos do Projeto

- ✅ **Portfólio Profissional:** Demonstrar habilidades backend (Django REST Framework) e frontend (Vue 3)
- ✅ **Código Limpo:** Seguir boas práticas (SOLID, DRY, Clean Code)
- ✅ **Deploy-Ready:** Container Docker configurado desde o início
- ✅ **Visual Impactante:** Design neon fluorescente moderno
- ✅ **Documentação Completa:** Código auto-explicativo com docstrings

---

## ✨ Funcionalidades (MVP)

### 🔑 Autenticação
- Login/Registro com JWT
- Refresh tokens
- Perfil de usuário

### 🏛️ Gestão de Espaços
- Listagem com filtros (tipo, capacidade, disponibilidade)
- Detalhes de cada espaço
- Sistema de busca

### 📅 Sistema de Reservas
- Calendário interativo
- Validação de conflitos de horário
- Confirmação/Cancelamento de reservas

### 📊 Painel do Usuário
- Minhas reservas (ativas e histórico)
- Cancelamento de reservas
- Notificações

---

## 🛠️ Stack Tecnológica

### Backend
```yaml
Linguagem: Python 3.12
Framework: Django 5.1
API: Django REST Framework 3.15
Banco: PostgreSQL 16 (via Docker)
Testes: pytest + pytest-django
Docs: drf-spectacular (Swagger/OpenAPI)
```

**Bibliotecas Principais:**
- `django-cors-headers` → Gerenciamento de CORS
- `python-decouple` → Variáveis de ambiente
- `psycopg2-binary` → Driver PostgreSQL
- `dj-database-url` → Config de banco via URL

### Frontend
```yaml
Framework: Vue 3 (Composition API)
Build Tool: Vite
Estilização: Tailwind CSS
State: Pinia
Requests: Axios
Roteamento: Vue Router
```

**Design System:**
- 🌈 Paleta neon (cyan, magenta, yellow, green)
- 🌃 Background escuro (#0a0e27)
- ✨ Sombras e glow effects
- 📱 Layout 100% responsivo

### DevOps
```yaml
Containers: Docker + Docker Compose
CI/CD: GitHub Actions (futuro)
Deploy: Railway / Render (planejado)
Versão: Git (commits semânticos)
```

---

## 🚀 Quick Start

### Pré-requisitos
```bash
# Instalar no Pop!_OS (ou Debian/Ubuntu)
sudo apt update
sudo apt install python3.12 python3.12-venv docker.io docker-compose git

# Adicionar seu usuário ao grupo docker (evita sudo)
sudo usermod -aG docker $USER
newgrp docker  # Ou reinicie a sessão
```

### Instalação (Modo Híbrido - Recomendado)

#### 1️⃣ Clonar Repositório
```bash
git clone https://github.com/edlucaz/workspace-booking-system.git
cd workspace-booking-system
```

#### 2️⃣ Backend (Python local + PostgreSQL Docker)
```bash
# Subir apenas PostgreSQL
docker compose up db -d

# Configurar backend
cd backend
python3.12 -m venv venv
source venv/bin/activate
pip install --upgrade pip
pip install -r requirements/base.txt

# Rodar migrações
python manage.py migrate

# Criar superusuário
python manage.py createsuperuser

# Iniciar servidor
python manage.py runserver
# ✅ Backend: http://localhost:8000
# ✅ Admin: http://localhost:8000/admin
# ✅ Swagger: http://localhost:8000/api/docs
```

#### 3️⃣ Frontend (Node local)
```bash
cd frontend
npm install
npm run dev
# ✅ Frontend: http://localhost:5173
```

### Ou: Tudo com Docker (Produção)
```bash
docker compose up --build
# Aguarde ~2 minutos para build inicial
```

---

## 📚 Documentação

### Arquitetura
```
workspace-booking-system/
├── backend/              # Django REST API
│   ├── core/            # Configurações do projeto
│   ├── bookings/        # App principal (Workspace + Booking)
│   ├── users/           # Autenticação JWT
│   └── requirements/    # Dependências (base, dev, prod)
├── frontend/             # Vue 3 SPA
│   ├── src/
│   │   ├── components/  # Componentes reutilizáveis
│   │   ├── pages/       # Páginas (rotas)
│   │   ├── api/         # Axios config
│   │   └── stores/      # Pinia (state)
│   └── public/
├── docker/               # Dockerfiles
├── docker-compose.yml    # Orquestração de containers
└── README.md
```

### Endpoints da API

| Método | Endpoint | Descrição |
|--------|----------|----------|
| `GET` | `/api/workspaces/` | Listar espaços disponíveis |
| `GET` | `/api/workspaces/{id}/` | Detalhes de um espaço |
| `POST` | `/api/bookings/` | Criar nova reserva |
| `GET` | `/api/bookings/` | Minhas reservas |
| `PATCH` | `/api/bookings/{id}/` | Cancelar reserva |
| `POST` | `/api/auth/login/` | Autenticação JWT |
| `POST` | `/api/auth/register/` | Criar conta |

📖 **Documentação Interativa:** http://localhost:8000/api/docs

---

## 🪧 Progresso do Desenvolvimento

Acompanhe o roadmap completo no [Linear](https://linear.app/next-change/project/workspace-booking-system-refatoracao-a33b0c5d556d):

### Fase 1: Estrutura 🟢 (Planejado)
- [ ] [NEX-42](https://linear.app/next-change/issue/NEX-42) - Estrutura inicial
- [ ] [NEX-43](https://linear.app/next-change/issue/NEX-43) - Setup Django
- [ ] [NEX-44](https://linear.app/next-change/issue/NEX-44) - Docker + PostgreSQL

### Fase 2: Backend 🟡 (Planejado)
- [ ] [NEX-45](https://linear.app/next-change/issue/NEX-45) - Models Django
- [ ] [NEX-46](https://linear.app/next-change/issue/NEX-46) - Serializers DRF
- [ ] [NEX-47](https://linear.app/next-change/issue/NEX-47) - ViewSets + URLs

### Fase 3: Frontend 🟡 (Planejado)
- [ ] [NEX-48](https://linear.app/next-change/issue/NEX-48) - Setup Vue 3 + Vite

---

## 🎨 Design System Neon

### Paleta de Cores
```css
:root {
  /* Cores Neon */
  --neon-cyan: #00ffff;      /* Links, botões primários */
  --neon-magenta: #ff00ff;   /* Destaques, alertas */
  --neon-yellow: #ffff00;    /* Avisos, notificações */
  --neon-green: #00ff00;     /* Sucesso, confirmações */
  
  /* Backgrounds */
  --dark-bg: #0a0e27;        /* Background principal */
  --dark-card: #1a1f3a;      /* Cards, modais */
  
  /* Sombras Neon */
  --shadow-cyan: 0 0 20px rgba(0, 255, 255, 0.5);
  --shadow-magenta: 0 0 20px rgba(255, 0, 255, 0.5);
}
```

### Tipografia
- **Fonte:** Inter (sans-serif)
- **Tamanhos:** 14px (corpo), 16px (botões), 24px+ (títulos)

---

## 🧑‍💻 Autor

**Lucas Eduardo Rocha**
- 👨‍💻 Desenvolvedor Backend | Python | Django
- 🎓 Bacharelando em TI (Univesp)
- 📧 Email: [24217901@aluno.univesp.br](mailto:24217901@aluno.univesp.br)
- 💙 GitHub: [@edlucaz](https://github.com/edlucaz)
- 🏛️ Araras-SP, Brasil

### Next Change Soluções Digitais
Projeto desenvolvido pela **Next Change**, focada em soluções web modernas com Django e tecnologias open-source.

---

## 📜 Licença

MIT License - Veja [LICENSE](LICENSE) para detalhes.

---

## 🔗 Links Úteis

- 📝 [Projeto no Linear](https://linear.app/next-change/project/workspace-booking-system-refatoracao-a33b0c5d556d)
- 🐛 [Reportar Bug](https://github.com/edlucaz/workspace-booking-system/issues)
- 💡 [Sugerir Feature](https://github.com/edlucaz/workspace-booking-system/issues)
- 📖 [Documentação Django](https://docs.djangoproject.com/en/5.1/)
- 📖 [Documentação Vue 3](https://vuejs.org/guide/introduction.html)

---

<div align="center">

### ✨ Estrele o projeto se ele te ajudou! ⭐

![Workspace Booking](https://img.shields.io/github/stars/edlucaz/workspace-booking-system?style=social)

---

<img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Laptop.png" alt="laptop" width="50" />

*De uma landing page estática a um sistema profissional full-stack.*

**2021 → 2026 | Evolução Contínua** 🚀

</div>
