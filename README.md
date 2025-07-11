# GitHub Actions Practice & CI/CD

This repository contains my practice workflows while learning **GitHub Actions** and basic **CI/CD pipelines** — following [this YouTube tutorial](https://www.youtube.com/watch?v=7gJFHjXscr8).

## 🚀 What This Repo Includes

- ✅ **Manual Trigger Workflows** using `workflow_dispatch`
- 🕒 **Scheduled Workflows** using cron syntax
- 🔁 **Repository Dispatch Workflows** triggered via API or another workflow
- 🧪 **Simple Test Automation** using Node.js and Shell scripts
- 📦 **CI/CD Pipeline Simulation** with build + test steps
- 📂 Inputs and payload data handling

---

## 📌 CI/CD Concepts Practiced

### 🔹 Continuous Integration (CI)
- Automatically runs tests on push
- Validates code through scripts (e.g. `test.sh`)
- Prevents broken code from being merged

### 🔹 Continuous Deployment (CD)
- Simulates deployments to environments (e.g., `dev`, `staging`, `prod`)
- Uses manual triggers or API calls to control deploy flow

---

## 🛠 How to Use

### 🔧 Manual Trigger
Go to the **Actions tab**, select a workflow, and click **“Run workflow”**.

### ⏰ Scheduled Trigger
Runs automatically at scheduled times (e.g., daily at 06:00 UTC).

### 📡 Repository Dispatch
Trigger via `curl` or another workflow:
```bash
curl -X POST \
  -H "Authorization: token YOUR_TOKEN" \
  -H "Accept: application/vnd.github.v3+json" \
  https://api.github.com/repos/AbdallahElshenawy/Actions/dispatches \
  -d '{"event_type":"incident-report","client_payload":{"environment":"prod"}}'
