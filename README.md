# 🐛 Smart Bug Tracker

A full-stack **AI-Powered Bug Management System** built using **Spring Boot, Spring Security, JWT, MySQL, Docker, Jenkins, and Google Gemini AI**. The application streamlines bug reporting, assignment, and resolution with secure role-based access, AI-powered issue analysis, and automated CI/CD.

---

## 🌟 Features

- 🔐 JWT Authentication with Spring Security
- 👥 Role-Based Access Control (Admin, Developer, Tester)
- 🤖 AI-Powered Issue Analysis using Google Gemini
- 📊 Dashboard Analytics
- 📝 Issue & Comment Management
- 🎯 AI-based Priority & Developer Expertise Recommendation
- 🔍 Similar Issue Detection
- 🐳 Docker Containerization
- ⚙️ Jenkins CI/CD Pipeline

---

# 🛠️ Tech Stack

### Backend
- Spring Boot
- Spring Security
- JWT
- Spring Data JPA
- Hibernate
- Maven

### Frontend
- HTML
- CSS
- JavaScript

### Database
- MySQL

### AI
- Google Gemini API

### DevOps
- Docker
- Jenkins

---

# 🏗️ System Architecture

```text
Frontend (HTML, CSS, JavaScript)
              │
              ▼
 REST APIs (JWT Authentication)
              │
              ▼
Spring Boot Backend
 ├── Spring Security
 ├── Controllers
 ├── Services
 ├── AI Analysis (Gemini)
 ├── Repositories
              │
              ▼
          MySQL Database

CI/CD Pipeline

GitHub
   │
   ▼
Jenkins
   │
   ▼
Maven Build
   │
   ▼
Docker Image
   │
   ▼
Deployment
```

---

# 🔐 Authentication Workflow

```text
User Login
      ↓
Backend Verifies Credentials
      ↓
JWT Generated
      ↓
JWT Stored on Client
      ↓
Authorization: Bearer <token>
      ↓
Spring Security Validates JWT
      ↓
Role-Based Access Granted
```

---

# 👥 User Roles

## 👨‍💼 Admin

- View all issues
- Review AI recommendations
- Assign developers
- Manage issues
- View dashboard analytics

## 👨‍💻 Developer

- View assigned issues
- Update issue status
- Add comments

## 🧪 Tester

- Create issues
- View own issues
- Verify resolved issues
- Reopen issues
- Add comments

---

# 🤖 AI-Powered Issue Analysis

When a tester creates an issue:

```text
Tester Creates Issue
        ↓
Backend Fetches Previous Issues
        ↓
Gemini AI Analyzes Issue
        ↓
AI Generates:
• Optimized Summary
• Suggested Priority
• Suggested Developer Expertise
• Similar Existing Issue
        ↓
Admin Reviews Suggestions
        ↓
Developer Assigned
```

AI assists the admin by recommending priority, developer expertise, and similar existing issues, while the final decision always remains with the admin.

---

# 📋 Issue Lifecycle

```text
NEW
 ↓
OPEN
 ↓
IN_PROGRESS
 ↓
RESOLVED
 ↓
CLOSED

        ↑
        │
   REOPENED
```

---

# ⚙️ CI/CD Pipeline (Jenkins)

The project uses **Jenkins** to automate the build process.

### Pipeline Workflow

```text
Developer Pushes Code
        ↓
GitHub Repository
        ↓
Jenkins Pipeline Triggered
        ↓
Checkout Source Code
        ↓
Maven Build
        ↓
Run Unit Tests
        ↓
Generate JAR
        ↓
Docker Image Build
        ↓
Deploy Application
```

### Jenkins Responsibilities

- Pulls latest code from GitHub
- Builds the project using Maven
- Executes unit tests
- Generates executable JAR
- Builds Docker image
- Automates deployment

---

# 🐳 Docker

Docker is used to containerize the application and ensure a consistent deployment environment.

```text
Spring Boot Application
        ↓
Docker Build
        ↓
Docker Image
        ↓
Docker Container
        ↓
Application Running
```

Run using:

```bash
docker-compose up --build
```

---

# 📡 REST API Highlights

```
POST   /api/auth/login
GET    /api/issues
POST   /api/issues
PUT    /api/issues/{id}
POST   /api/issues/{id}/assign
GET    /api/dashboard
```

---

# ⚙️ Installation

```bash
git clone <repository-url>

cd smart-bug-tracker

./mvnw spring-boot:run
```

Open:

```
http://localhost:8080
```

---

# 🔑 Environment Variables

```properties
spring.datasource.url=
spring.datasource.username=
spring.datasource.password=

jwt.secret=

gemini.api.key=
```

---

# 📸 Screenshots

Include screenshots of:

- Login Page
- Dashboard
- Create Issue
- AI Analysis Panel
- Admin Dashboard
- Developer Dashboard
- Tester Dashboard

---


# 👨‍💻 Author

**Gorityala Manasa**

⭐ If you found this project useful, consider starring the repository.
