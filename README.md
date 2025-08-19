EN version:
# BreakIn Direct 🚀

> **Proof-of-Work Hiring System (PoWHS) - Revolutionizing Tech Recruitment**

[![Tech Stack](https://img.shields.io/badge/Stack-Next.js%20%7C%20FastAPI%20%7C%20MongoDB%20%7C%20GPT--5-blue)](https://github.com/david15tonon/BreakIn)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-MVP%20Hackathon-orange)](https://github.com/david15tonon/BreakIn)
[![Demo](https://img.shields.io/badge/Demo-Live-green)](https://breakin-direct.vercel.app)

> 🇺🇸 **English Version** | 🇫🇷 **[Version Française](README.md)**

---

## 📋 Table of Contents

- [The Problem](#the-problem)
- [Our Solution](#our-solution)
- [How It Works](#how-it-works)
- [Hackathon Roadmap (5 Days)](#hackathon-roadmap-5-days)
- [Architecture](#architecture)
- [Installation & Setup](#installation--setup)
- [Tech Stack](#tech-stack)
- [Live Demo](#live-demo)
- [Contributing](#contributing)

---

## 💣 The Problem

### A Broken Hiring System

In today's hiring landscape, **junior developers and transitioning talent are left behind** - not for lack of skill, but because résumés fail to show what truly matters: **the ability to build, collaborate, and grow in real-world conditions**.

| Area | What's Broken |
|------|---------------|
| **Recruitment** | ATS filters out talent based on pedigree, not performance |
| **Juniors & Transitions** | Entry-level roles are shrinking; "2+ years experience" is now entry-level |
| **Bias & Inequity** | Candidates from non-traditional backgrounds are unfairly overlooked |
| **Companies** | Struggle to validate skill, team fit, and work ethic pre-hire |
| **Mentorship Access** | Junior developers lack feedback loops and role models in early stages |

> 🚨 **A junior dev today doesn't just compete with peers — they compete with noisy job markets, silent rejection emails, and invisible gatekeeping.**

---

## 💡 Our Solution

### Proof-of-Work Hiring System (PoWHS)

**A zero-resumé, no-job-posting, mentorship-first simulation platform** where skill earns opportunity.

BreakIn Direct replaces guesswork hiring with **verifiable performance**. Through simulation sprints, AI review, mentor feedback, and collaborative team builds, we generate living portfolios that hiring managers can trust more than any cover letter.

### 🔁 How It Works

1. **Developers join team-based simulation sprints**
2. **AI + mentor feedback powers reputation & growth**
3. **Hiring engine recommends talent based on work—not words**
4. **Companies hire directly—without posting a job or screening résumés**

---

## 🎯 Who BreakIn Serves

| Stakeholder | Value |
|-------------|-------|
| **Junior & Mid Developers** | Build real experience, get feedback, earn trust without prior jobs |
| **Mentors (Senior Devs)** | Guide talent, scout future hires, grow community leadership |
| **Companies** | Hire based on actual builds, teamwork behavior, and skill growth—not static credentials |
| **Schools/NGOs** | Offer real-world internships, track student impact, plug into global talent demand |

---

## 🚀 Hackathon Roadmap (5 Days)

### 🎯 Final Objective
Deliver a functional MVP of BreakIn:
- **Frontend** (SquadRoom UI + pseudonyms)
- **Backend API** (FastAPI + MongoDB + GPT-5)
- **Complete Flow**: signup → pseudonym assignment → mission → anonymous feedback → scoring
- **Live demo + GitHub repo (public) + pitch video**

### 📆 Sprint Plan (5 Days)

#### **Day 1 — Kickoff & Setup** ✅
- [x] Define MVP scope (keep it simple but impactful)
- [x] Setup GitHub repo (frontend + backend monorepo)
- [x] Configure MongoDB Atlas + connect to FastAPI
- [x] Setup GPT-5 API (hackathon key)
- [x] Quick SquadRoom UI mockups (Figma/Miro)
- **👉 Deliverable**: Repo structured + UX validated

#### **Day 2 — Backend Core** ✅
- [x] Build FastAPI with routes:
  - `/signup` → user creation + pseudonym
  - `/start-sprint` → GPT-5 mission generation
  - `/submit-task` → save deliverable (MongoDB)
  - `/feedback` → mentors/AI feedback
- [x] Design MongoDB schema (users, sprints, feedback, scores)
- **👉 Deliverable**: Postman-testable API

#### **Day 3 — Frontend Core + API Integration** ✅
- [x] Setup Next.js + Tailwind (fast dev)
- [x] Pages:
  - Login (pseudo)
  - SquadRoom dashboard (list sprints + chat pseudonyms)
  - Mission page (submit task)
  - Feedback display
- [x] Connect frontend ↔ backend (REST API)
- **👉 Deliverable**: Clickable frontend fully connected to backend

#### **Day 4 — AI + Anonymization + Scoring** 🔄
- [ ] Integrate GPT-5 for mission generation + feedback
- [ ] Implement pseudonym rotation (per sprint)
- [ ] Add scoring system (≥85% = revealable)
- [ ] End-to-end test flow: signup → mission → submission → feedback → scoring
- **👉 Deliverable**: Full functional sprint flow with anonymization

#### **Day 5 — Finalization & Pitch** 📅
- [ ] Polish UX (animations, icons)
- [ ] Add admin logs (integrity)
- [ ] Deploy: Vercel (frontend) + Render/Heroku (backend)
- [ ] Record pitch video (2–3 min: problem → solution → impact)
- [ ] Prepare slides (vision, tech stack, business angle)
- [ ] Submit repo + demo link + slides + video
- **👉 Deliverable**: Hosted MVP + final hackathon submission

---

## 🏗️ Architecture

### Frontend (Next.js 14 + Tailwind)

```bash
Frontend/
├── app/                     # App Router (Next.js 14)
│   ├── page.tsx            # Landing page
│   ├── login/              # Pseudonym authentication
│   ├── squadroom/          # Main dashboard
│   ├── sprint/[id]/        # Individual mission page
│   └── feedback/           # Feedback system
├── components/             # Reusable components
│   ├── ui/                # UI components (shadcn/ui)
│   ├── SquadRoom.tsx      # Main interface
│   └── PseudonymChat.tsx  # Anonymous chat
└── lib/                   # Utilities & API calls
```

### Backend (FastAPI + MongoDB + GPT-5)

```bash
Backend/
├── app/
│   ├── main.py            # FastAPI entry point
│   ├── config.py          # Configuration (MongoDB, GPT-5)
│   ├── models.py          # Pydantic models
│   ├── routes/
│   │   ├── auth.py        # Pseudonym management
│   │   ├── sprint.py      # Sprint logic
│   │   ├── feedback.py    # Feedback system
│   │   └── scoring.py     # Scoring algorithm
│   └── services/
│       ├── db.py          # MongoDB interface
│       ├── gpt.py         # GPT-5 integration
│       └── anonymizer.py  # Pseudonym management
└── requirements.txt       # Python dependencies
```

---

## ⚙️ Tech Stack

| Layer | Technologies |
|-------|-------------|
| **Frontend** | Next.js 14, TypeScript, Tailwind CSS, shadcn/ui |
| **Backend** | FastAPI, Python 3.12, Pydantic |
| **Database** | MongoDB Atlas |
| **AI** | GPT-5 API (OpenAI) |
| **Authentication** | Custom pseudonym system |
| **Deployment** | Vercel (frontend) + Render/Heroku (backend) |
| **Collaboration** | GitHub, Discord, Trello |

---

## 🚀 Installation & Setup

### Prerequisites
- Node.js 18+ and npm/pnpm
- Python 3.12+
- MongoDB Atlas account
- GPT-5 API key (OpenAI)

### 1. Clone & Setup

```bash
git clone https://github.com/david15tonon/BreakIn.git
cd BreakIn
```

### 2. Backend Setup

```bash
cd Backend

# Virtual environment
python -m venv venv
source venv/bin/activate  # Linux/Mac

# Dependencies
pip install -r requirements.txt

# Environment variables
cp .env.example .env
# Edit .env:
# MONGO_URI=mongodb+srv://your-cluster
# DB_NAME=breakin_hackathon
# GPT_API_KEY=your_gpt5_key

# Start server
uvicorn app.main:app --reload --port 8000
```

### 3. Frontend Setup

```bash
cd Frontend

# Dependencies
pnpm install

# Environment variables
cp .env.example .env.local
# NEXT_PUBLIC_API_URL=http://localhost:8000

# Start dev server
pnpm dev
```

### 🌐 Development URLs

- **Frontend**: <http://localhost:3000>
- **API Backend**: <http://localhost:8000>
- **API Docs**: <http://localhost:8000/docs>
- **SquadRoom**: <http://localhost:3000/squadroom>

---

## 🎮 Live Demo

### Complete User Flow

1. **Signup** → Automatic pseudonym generation
2. **SquadRoom** → Join available sprint
3. **Mission** → Receive GPT-5 generated challenge
4. **Development** → Collaborate with team (pseudonyms)
5. **Submission** → Upload solution + documentation
6. **Feedback** → AI + anonymous mentor evaluation
7. **Scoring** → Score ≥85% reveals identity to recruiters

### Example GPT-5 Mission

```markdown
🎯 Mission: "E-commerce Cart Microservice"
⏱️ Duration: 3 days
👥 Team: 4 developers (pseudonyms: Alpha, Bravo, Charlie, Delta)

📋 Objective:
Build a shopping cart microservice with:
- REST API (Node.js/Python)
- Database (your choice)
- Unit tests
- API documentation
- Docker containerization

💡 Evaluation Criteria:
- Code quality & architecture (30%)
- Collaboration & communication (25%)
- Tests & documentation (25%)
- Innovation & creativity (20%)
```

---

## 🏆 Hackathon Winning Strategy

1. **Impact** → bias-free recruitment = global meritocracy
2. **Smooth demo** → show full loop in ≤2 min
3. **Business angle** → SaaS B2B product for unbiased hiring
4. **Storytelling** → start with a discrimination anecdote

---

## 🔑 Core Differentiator: Performance > Paper

| Traditional Hiring (ATS) | Proof-of-Work Hiring (BreakIn) |
|--------------------------|--------------------------------|
| Filters by keyword/resumé | Filters by actual performance |
| Opaque ranking algorithms | Transparent sprint scoreboards |
| Ghosting and black boxes | Feedback-rich development loop |
| Slow, biased, and static | Real-time, merit-based, living ecosystem |

---

## 🌐 The New Learning-Working Loop

BreakIn Direct introduces the **Orbit Model**:

**Learn → Build → Lead → Mentor → Get Hired → Give Back**

Each developer graduates from mentee to contributor to mentor, growing the ecosystem while pulling others up—a self-sustaining talent loop that traditional HR pipelines can't replicate.

---

## 🤝 Contributing

### For the Hackathon

1. **Fork** the project
2. Pick a task from [Trello Board](https://trello.com/b/breakin-hackathon)
3. Create a branch (`feature/task-name`)
4. Develop & test
5. Pull Request with detailed description

### Guidelines

- **Code style**: Prettier (Frontend) + Black (Backend)
- **Commits**: Conventional format (`feat:`, `fix:`, `docs:`)
- **Tests**: Required for new features
- **Documentation**: Update README if API changes

---

## 💸 Revenue Strategy (Lean, Ethical, Scalable)

| Stream | Model |
|--------|-------|
| 💼 **Company subscriptions** | AI-matched talent dashboard |
| 🪙 **Sprint sponsorships** | Run branded simulation challenges |
| 🎓 **Education partnerships** | Institutions pay for guided student sprints |
| 🎖️ **Dev portfolio boosts** | Developers pay to enhance visibility post-sprint |
| 💻 **Hiring-as-a-service** | Managed hiring for startups & recruiters |

---

## 📞 Contact & Links

- **GitHub Repo**: [BreakIn Direct](https://github.com/david15tonon/BreakIn)
- **Live Demo**: [breakin-direct.vercel.app](https://breakin-direct.vercel.app)
- **Team Discord**: [Join](https://discord.gg/breakin-hackathon)
- **Pitch Video**: [YouTube](https://youtube.com/watch?v=breakin-pitch)

---

## 🎯 Vision

> **BreakIn Direct is not just a platform — it's a movement.**
> 
> A movement to restore trust in early-career hiring, to replace bias with evidence, and to prove that great talent doesn't need a perfect resumé — just a real chance to build.
> 
> **Let's stop hiring potential on paper and start hiring performance in action.**

---

<div align="center">

**BreakIn Direct** - Raising the talent floor for everyone — with proof, not promises 🚀

**#ProofOfWork #TalentRevolution #BiasFreehiring**

</div>

FR version


# BreakIn Direct 🚀

> **Système de Recrutement par Preuve de Travail (PoWHS) - Révolutionner l'embauche tech**

[![Tech Stack](https://img.shields.io/badge/Stack-Next.js%20%7C%20FastAPI%20%7C%20MongoDB%20%7C%20GPT--5-blue)](https://github.com/david15tonon/BreakIn)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-MVP%20Hackathon-orange)](https://github.com/david15tonon/BreakIn)
[![Demo](https://img.shields.io/badge/Demo-Live-green)](https://breakin-direct.vercel.app)

> 🇺🇸 **[English Version](README_EN.md)** | 🇫🇷 **Version Française**

---

## 📋 Table des matières

- [Le Problème](#le-problème)
- [Notre Solution](#notre-solution)
- [Comment ça marche](#comment-ça-marche)
- [Roadmap Hackathon (5 jours)](#roadmap-hackathon-5-jours)
- [Architecture](#architecture)
- [Installation & Setup](#installation--setup)
- [Tech Stack](#tech-stack)
- [Démo en direct](#démo-en-direct)
- [Contribution](#contribution)

---

## 💣 Le Problème

### Un système d'embauche cassé

Dans le paysage actuel de l'embauche, **les développeurs juniors et les talents en transition sont laissés pour compte** - non pas par manque de compétences, mais parce que les CV échouent à montrer ce qui compte vraiment : **la capacité à construire, collaborer et grandir dans des conditions réelles**.

| Domaine | Ce qui est cassé |
|---------|------------------|
| **Recrutement** | Les ATS filtrent les talents sur le pedigree, pas la performance |
| **Juniors & Transitions** | Les postes entry-level disparaissent ; "2+ ans d'expérience" devient le nouveau entry-level |
| **Biais & Inégalités** | Les candidats issus de milieux non-traditionnels sont injustement ignorés |
| **Entreprises** | Difficultés à valider les compétences, l'adéquation à l'équipe et l'éthique de travail avant l'embauche |
| **Accès au mentorat** | Les développeurs juniors manquent de boucles de feedback et de modèles dans les premières étapes |

> 🚨 **Un développeur junior aujourd'hui ne fait pas que concurrencer ses pairs — il concurrence des marchés d'emploi bruyants, des emails de refus silencieux et un gatekeeping invisible.**

---

## 💡 Notre Solution

### Système de Recrutement par Preuve de Travail (PoWHS)

**Une plateforme de simulation sans CV, sans offre d'emploi, centrée sur le mentorat**, où les compétences gagnent des opportunités.

BreakIn Direct remplace l'embauche par intuition par **des performances vérifiables**. À travers des sprints de simulation, des revues IA, des feedbacks de mentors et des constructions d'équipes collaboratives, nous générons des portfolios vivants en lesquels les responsables de recrutement peuvent avoir plus confiance qu'en n'importe quelle lettre de motivation.

### 🔁 Comment ça fonctionne

1. **Les développeurs rejoignent des sprints de simulation en équipe**
2. **IA + feedback de mentors alimentent la réputation & croissance**
3. **Le moteur d'embauche recommande les talents basé sur le travail—pas les mots**
4. **Les entreprises embauchent directement—sans poster d'annonce ou filtrer des CV**

---

## 🎯 Pour qui BreakIn existe

| Partie prenante | Valeur apportée |
|----------------|-----------------|
| **Développeurs Junior & Mid** | Construire une vraie expérience, recevoir des feedbacks, gagner la confiance sans emplois précédents |
| **Mentors (Développeurs Senior)** | Guider les talents, scout de futurs employés, développer le leadership communautaire |
| **Entreprises** | Embaucher basé sur de vraies constructions, comportement d'équipe et croissance de compétences—pas des credentials statiques |
| **Écoles/ONG** | Offrir des stages réels, tracker l'impact étudiant, se connecter à la demande globale de talents |

---

## 🚀 Roadmap Hackathon (5 jours)

### 🎯 Objectif Final
Livrer un MVP fonctionnel de BreakIn :
- **Frontend** (SquadRoom UI + pseudonymes)
- **Backend API** (FastAPI + MongoDB + GPT-5)
- **Flow complet** : inscription → assignation pseudonyme → mission → feedback anonyme → scoring
- **Démo live + repo GitHub (public) + vidéo pitch**

### 📆 Plan de Sprint (5 Jours)

#### **Jour 1 — Kickoff & Setup** ✅
- [x] Définir le scope MVP (simple mais impactant)
- [x] Setup repo GitHub (frontend + backend monorepo)
- [x] Configurer MongoDB Atlas + connexion FastAPI
- [x] Setup GPT-5 API (clé hackathon)
- [x] Maquettes SquadRoom UI rapides (Figma/Miro)
- **👉 Livrable** : Repo structuré + UX validée

#### **Jour 2 — Backend Core** ✅
- [x] Construire API FastAPI avec routes :
  - `/signup` → création utilisateur + pseudonyme
  - `/start-sprint` → génération mission GPT-5
  - `/submit-task` → sauvegarder livrable (MongoDB)
  - `/feedback` → feedback mentors/IA
- [x] Concevoir schéma MongoDB (users, sprints, feedback, scores)
- **👉 Livrable** : API testable avec Postman

#### **Jour 3 — Frontend Core + Intégration API** ✅
- [x] Setup Next.js + Tailwind (dev rapide)
- [x] Pages :
  - Login (pseudo)
  - Dashboard SquadRoom (liste sprints + chat pseudonymes)
  - Page Mission (soumettre tâche)
  - Affichage Feedback
- [x] Connecter frontend ↔ backend (REST API)
- **👉 Livrable** : Frontend cliquable entièrement connecté au backend

#### **Jour 4 — IA + Anonymisation + Scoring** 🔄
- [ ] Intégrer GPT-5 pour génération mission + feedback
- [ ] Implémenter rotation pseudonymes (par sprint)
- [ ] Ajouter système de scoring (≥85% = révélable)
- [ ] Test end-to-end : inscription → mission → soumission → feedback → scoring
- **👉 Livrable** : Flow sprint fonctionnel complet avec anonymisation

#### **Jour 5 — Finalisation & Pitch** 📅
- [ ] Polir UX (animations, icônes)
- [ ] Ajouter logs admin (intégrité)
- [ ] Déployer : Vercel (frontend) + Render/Heroku (backend)
- [ ] Enregistrer vidéo pitch (2–3 min: problème → solution → impact)
- [ ] Préparer slides (vision, tech stack, angle business)
- [ ] Soumettre repo + lien démo + slides + vidéo
- **👉 Livrable** : MVP hébergé + soumission hackathon finale

---

## 🏗️ Architecture

### Frontend (Next.js 14 + Tailwind)

```bash
Frontend/
├── app/                     # App Router (Next.js 14)
│   ├── page.tsx            # Page d'accueil
│   ├── login/              # Authentification pseudonyme
│   ├── squadroom/          # Dashboard principal
│   ├── sprint/[id]/        # Page mission individuelle
│   └── feedback/           # Système de feedback
├── components/             # Composants réutilisables
│   ├── ui/                # Composants UI (shadcn/ui)
│   ├── SquadRoom.tsx      # Interface principale
│   └── PseudonymChat.tsx  # Chat anonyme
└── lib/                   # Utilitaires & API calls
```

### Backend (FastAPI + MongoDB + GPT-5)

```bash
Backend/
├── app/
│   ├── main.py            # Point d'entrée FastAPI
│   ├── config.py          # Configuration (MongoDB, GPT-5)
│   ├── models.py          # Modèles Pydantic
│   ├── routes/
│   │   ├── auth.py        # Gestion pseudonymes
│   │   ├── sprint.py      # Logique sprints
│   │   ├── feedback.py    # Système feedback
│   │   └── scoring.py     # Algorithme scoring
│   └── services/
│       ├── db.py          # Interface MongoDB
│       ├── gpt.py         # Intégration GPT-5
│       └── anonymizer.py  # Gestion pseudonymes
└── requirements.txt       # Dépendances Python
```

---

## ⚙️ Tech Stack

| Couche | Technologies |
|--------|-------------|
| **Frontend** | Next.js 14, TypeScript, Tailwind CSS, shadcn/ui |
| **Backend** | FastAPI, Python 3.12, Pydantic |
| **Base de données** | MongoDB Atlas |
| **IA** | GPT-5 API (OpenAI) |
| **Authentification** | Système pseudonyme custom |
| **Déploiement** | Vercel (frontend) + Render/Heroku (backend) |
| **Collaboration** | GitHub, Discord, Trello |

---

## 🚀 Installation & Setup

### Prérequis
- Node.js 18+ et npm/pnpm
- Python 3.12+
- Compte MongoDB Atlas
- Clé API GPT-5 (OpenAI)

### 1. Clone & Setup

```bash
git clone https://github.com/david15tonon/BreakIn.git
cd BreakIn
```

### 2. Backend Setup

```bash
cd Backend

# Environnement virtuel
python -m venv venv
source venv/bin/activate  # Linux/Mac

# Dépendances
pip install -r requirements.txt

# Variables d'environnement
cp .env.example .env
# Éditer .env :
# MONGO_URI=mongodb+srv://your-cluster
# DB_NAME=breakin_hackathon
# GPT_API_KEY=your_gpt5_key

# Démarrer le serveur
uvicorn app.main:app --reload --port 8000
```

### 3. Frontend Setup

```bash
cd Frontend

# Dépendances
pnpm install

# Variables d'environnement
cp .env.example .env.local
# NEXT_PUBLIC_API_URL=http://localhost:8000

# Démarrer le dev server
pnpm dev
```

### 🌐 URLs de développement

- **Frontend** : <http://localhost:3000>
- **API Backend** : <http://localhost:8000>
- **Docs API** : <http://localhost:8000/docs>
- **SquadRoom** : <http://localhost:3000/squadroom>

---

## 🎮 Démo en direct

### Flow utilisateur complet

1. **Inscription** → Génération pseudonyme automatique
2. **SquadRoom** → Rejoindre sprint disponible
3. **Mission** → Recevoir défi généré par GPT-5
4. **Développement** → Collaborer avec équipe (pseudonymes)
5. **Soumission** → Upload solution + documentation
6. **Feedback** → Évaluation IA + mentors anonymes
7. **Scoring** → Score ≥85% révèle identité pour recruteurs

### Exemple de Mission GPT-5

```markdown
🎯 Mission: "E-commerce Cart Microservice"
⏱️ Durée: 3 jours
👥 Équipe: 4 développeurs (pseudonymes: Alpha, Bravo, Charlie, Delta)

📋 Objectif:
Construire un microservice de panier d'achat avec:
- API REST (Node.js/Python)
- Base de données (au choix)
- Tests unitaires
- Documentation API
- Conteneurisation Docker

💡 Critères d'évaluation:
- Code quality & architecture (30%)
- Collaboration & communication (25%)
- Tests & documentation (25%)
- Innovation & créativité (20%)
```

---

## 🏆 Stratégie de Victoire Hackathon

1. **Impact** → Recrutement sans biais = méritocratie globale
2. **Démo fluide** → Montrer la boucle complète en ≤2 min
3. **Angle business** → Produit SaaS B2B pour embauche sans biais
4. **Storytelling** → Commencer par une anecdote de discrimination

---

## 🤝 Contribution

### Pour le Hackathon

1. **Fork** le projet
2. Prendre une tâche sur [Trello Board](https://trello.com/b/breakin-hackathon)
3. Créer une branche (`feature/task-name`)
4. Développer & tester
5. Pull Request avec description détaillée

### Guidelines

- **Code style** : Prettier (Frontend) + Black (Backend)
- **Commits** : Format conventionnel (`feat:`, `fix:`, `docs:`)
- **Tests** : Obligatoires pour nouvelles features
- **Documentation** : MAJ README si changements d'API

---

## 📞 Contact & Liens

- **Repo GitHub** : [BreakIn Direct](https://github.com/david15tonon/BreakIn)
- **Démo Live** : [breakin-direct.vercel.app](https://breakin-direct.vercel.app)
- **Discord Team** : [Rejoindre](https://discord.gg/breakin-hackathon)
- **Pitch Video** : [YouTube](https://youtube.com/watch?v=breakin-pitch)

---

## 🎯 Vision

> **BreakIn Direct n'est pas juste une plateforme — c'est un mouvement.**
> 
> Un mouvement pour restaurer la confiance dans l'embauche en début de carrière, pour remplacer les biais par des preuves, et pour prouver que les grands talents n'ont pas besoin d'un CV parfait — juste d'une vraie chance de construire.
> 
> **Arrêtons d'embaucher le potentiel sur papier et commençons à embaucher la performance en action.**

---

<div align="center">

**BreakIn Direct** - Élever le niveau de talent pour tous — avec des preuves, pas des promesses 🚀

**#ProofOfWork #TalentRevolution #BiasFreHiring**

</div>
