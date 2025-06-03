# Getting Started with GitHub on Windows

This guide will walk you through creating, managing, and uploading a GitHub project using Git on Windows — including how to authenticate with GitHub securely.

---

## 🧰 Prerequisites

- [Git for Windows](https://git-scm.com/download/win)
- A [GitHub account](https://github.com/)
- Git Bash (comes with Git)

---

## 📁 Step 1: Create a Local Project Folder

```bash
mkdir MyFirstProject
cd MyFirstProject
```

---

## 📄 Step 2: Create Some Files

```bash
echo "# My First Project" > README.md
echo "print('Hello GitHub!')" > main.py
```

---

## 🌀 Step 3: Initialize Git

```bash
git init
```

---

## 👤 Step 4: Configure Git (First Time Only)

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

---

## 📦 Step 5: Stage and Commit

```bash
git add .
git commit -m "Initial commit"
```

---

## 🌐 Step 6: Create a GitHub Repository

1. Go to [https://github.com](https://github.com)
2. Click the **+** → **New repository**
3. Name it `MyFirstProject`
4. Click **Create repository**

---

## 🔗 Step 7: Connect Local Folder to GitHub

```bash
git remote add origin https://github.com/your-username/MyFirstProject.git
```

(Optional: verify)

```bash
git remote -v
```

---

## 🔐 Step 8: Set Up Authentication (HTTPS + Token)

### 🔸 Generate a GitHub Token:

1. Go to: [https://github.com/settings/tokens](https://github.com/settings/tokens)
2. Click **Fine-grained tokens → Generate new token**
3. Select:
   - Expiration: 30 days (or "No expiration")
   - Repository access: All repositories
   - Permissions: **Contents: Read and write**
4. Click **Generate token**
5. Copy the token — you won’t see it again!

### 🔸 Push Code:

```bash
git branch -M main
git push -u origin main
```

Git will ask:

```
Username: your-username
Password: <paste your token>
```

---

## 🔄 Step 9: Making Future Changes

```bash
# After editing files:
git add .
git commit -m "Update"
git push
```

---

## 🧽 Step 10: Use .gitignore

```bash
echo "__pycache__/" > .gitignore
git add .gitignore
git commit -m "Add .gitignore"
git push
```

---

## 🧪 Useful Git Commands

| Command              | Description                          |
|----------------------|--------------------------------------|
| `git status`         | Show file changes                    |
| `git log`            | Show commit history                  |
| `git pull`           | Get updates from GitHub              |
| `git clone <url>`    | Copy a repo to your computer         |

---

## ✅ Done!

You’ve created a GitHub repo from scratch on Windows, added authentication, and pushed your first project. 🚀
