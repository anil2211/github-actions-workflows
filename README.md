# 🚀 GitHub Actions Multi-Event Workflow Demo

This repository demonstrates a **multi-event CI pipeline using GitHub Actions**.

The workflow is triggered by multiple events such as:

- ✅ Push  
- 🔁 Pull Request  
- ▶️ Manual Trigger (workflow_dispatch)  

It also showcases **conditional job execution** based on the type of event, making it a flexible and event-driven CI/CD example.

---

## 📌 Project Overview

This project is a demo repository created to:

- Understand GitHub Actions workflows
- Trigger pipelines using multiple events
- Implement conditional job execution
- Explore manual workflow dispatch options
- Learn event-based CI/CD automation

---

## 📂 Repository Structure

```
.
├── .github/
│   └── workflows/
│       └── workflow.yml   # Multi-event GitHub Actions workflow
└── README.md
```

---

## 🔄 Workflow Triggers

The pipeline runs on:

### 1️⃣ Push Event
Triggered when code is pushed to a specific branch.

### 2️⃣ Pull Request Event
Triggered when a pull request is opened or updated.

### 3️⃣ Manual Trigger (workflow_dispatch)
Allows manual execution from the GitHub Actions tab.

---

## ⚙️ Key Features

- Multi-event workflow configuration
- Conditional job execution using `if:` statements
- Manual pipeline execution support
- Event-based CI/CD logic
- Demonstration of flexible automation design

---

## 🏗 Example Workflow Structure

```yaml
name: Multi-Event Workflow

on:
  push:
    branches:
      - main
  pull_request:
    branches:
      - main
  workflow_dispatch:

jobs:
  example-job:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout Repository
        uses: actions/checkout@v3

      - name: Print Event Name
        run: echo "Triggered by ${{ github.event_name }}"

      - name: Conditional Step
        if: github.event_name == 'push'
        run: echo "This runs only on push event"
```

---

## 🖥 How to Test the Workflow

### 🔹 Push Trigger
Push code to the configured branch.

### 🔹 Pull Request Trigger
Create a pull request targeting the configured branch.

### 🔹 Manual Trigger
1. Go to **Actions** tab in the repository  
2. Select the workflow  
3. Click **Run workflow**

---

## 🎯 Learning Outcomes

After exploring this repository, you will understand:

- How GitHub Actions events work
- How to trigger workflows using multiple events
- How to add conditional logic inside jobs
- How to manually dispatch workflows
- How event-driven CI/CD pipelines function

---

## 📌 Future Improvements

- Add matrix builds
- Add environment-based conditions
- Add reusable workflows
- Add status badges to README
- Integrate testing and deployment stages

---

## 👨‍💻 Author

**Anil Rai**  
DevOps & Automation Enthusiast

---

⭐ This repository is intended for learning and demonstration purposes.
