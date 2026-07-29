# Production-Ready CI/CD Pipeline Automation

![CI/CD Pipeline](https://github.com/eishamubashir1/tynoc-projects/actions/workflows/ci-cd.yml/badge.svg)

## 📌 Project Overview
This repository contains a production-ready CI/CD pipeline built with **GitHub Actions** for a Node.js multi-tier application. It demonstrates modern DevOps practices, automated workflows, version control strategies, and automated quality assurance before simulating deployment to a staging environment.

---

## 🚀 Pipeline Architecture & Stages

The GitHub Actions workflow (`.github/workflows/ci-cd.yml`) is divided into two sequential jobs:
[ Push / PR to main ]
│
▼
┌──────────────────┐
│  Lint & Test     │ ──> Installs dependencies, runs code formatting checks, executes unit tests.
└─────────┬────────┘
│ (on success)
▼
┌──────────────────┐
│  Build & Deploy  │ ──> Injects Secrets/Env Vars, builds production artifacts, simulates Staging Deployment.
└──────────────────┘
1. **Automated Build Pipeline**: Set up via GitHub Actions on Node.js v20 environment.
2. **Lint & Test Execution**: Installs backend packages, verifies syntax code quality with ESLint, and executes test cases using Jest.
3. **Environment Variables & Secrets Handling**: Securely injects environment credentials (`APP_ENV`, `API_KEY`) into build and deployment stages.
4. **Deployment Workflow**: Simulates deployment to a staging environment upon passing code quality gates.

---

## 🔐 Environment Variables & Secrets Setup

To configure custom secrets for the deployment pipeline in GitHub:

1. Go to your GitHub Repository: `Settings` > `Secrets and variables` > `Actions`.
2. Click **New repository secret**.
3. Add the following secrets:
   - `APP_ENV`: `staging` or `production`
   - `API_KEY`: Your secret API authentication key

*Note: The pipeline automatically defaults to safe fallback values if repository secrets are not set.*

---

## 💻 How to Run Locally

### Prerequisites
- Node.js (v18 or higher)
- Git

### Local Setup Instructions
```bash
# 1. Clone the repository
git clone [https://github.com/eishamubashir1/tynoc-projects.git](https://github.com/eishamubashir1/tynoc-projects.git)

# 2. Navigate to backend
cd tynoc-projects/backend

# 3. Install dependencies
npm install

# 4. Run tests & linters
npm test
npm run lint

# 5. Start application
npm start


