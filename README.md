# Recruiter REST API

**Recipe Project — Recruiter-Friendly REST API**

### Explore a working backend API with zero setup — just Docker Desktop required

This is a backend REST API built with **Django & Django REST Framework**, designed to be **easy for recruiters and hiring managers to explore**, while also showcasing modern backend practices for technical reviewers.

- **Non-technical viewers:** See endpoints in action, explore the admin panel, and get a sense of how I structure backend systems.
- **Technical reviewers:** Demonstrates containerization with Docker, secure JWT authentication, modular architecture, PostgreSQL integration, Test-Driven Development (TDD), and CI/CD with GitHub Actions.

---

### Why You Should Hire Me

# This project demonstrates exactly how I think, structure systems, and ship maintainable backend code with:
- Clear modular architecture for scalable backend systems Secure authentication & permissions management
- Dockerized development for reproducibility & team onboarding
- TDD with high test coverage to ensure reliability
- CI/CD integration to automate quality and deployment
- PostgreSQL integration showing real-world database handling

# By exploring this repository, recruiters and technical reviewers can see hands-on evidence of my backend engineering skills, not just a resume.

### 📬 Contact & Hiring Info

I am currently seeking:
- Remote full-time backend or software engineering roles
- Contract or contract-to-hire opportunities
- Email: mattpritchard405 [at] gmail [dot] com

---

## 🚀 Key Features

- Full CRUD API for recipes, ingredients, tags, and users
- JWT authentication with secure object-level permissions
- Image uploads, nested serializers, filtering, sorting, and searching
- Dockerized development & production environments
- PostgreSQL database configuration
- GitHub Actions CI/CD: automatic tests and linting
- TDD approach with high test coverage

---

## 🛠 Quick Start (5 Minutes)

**Goal:** Let anyone explore the project without needing Python setup. Just use Docker.

**Prerequisites:** [Docker Desktop](https://www.docker.com/products/docker-desktop) installed.

```bash
# 1. Clone the project
git clone https://github.com/mpritc991/recipe-project.git
cd recipe-project

# 2. Start the stack (Database + API)
docker compose up --build

# 3. Create Admin user
docker compose run app python manage.py createsuperuser

# 4. Access the project
# API: http://localhost:8000
# Docs: http://localhost:8000/api/docs/ (Authorize with JWT: prefix token with "Token ")
# Admin: http://localhost:8000/admin
