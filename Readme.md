# 🚀 Git Complete Learning Guide

## 📌 What is Git?

Git is a **Version Control System (VCS)** that keeps track of all updates you make in a project.  
It allows you to manage versions, collaborate with others, and revert to previous states safely.

---

## ⚙️ How Git Works

When you initialize Git:

```bash
git init -b main
```

Git creates:
- Your working directory
- A hidden `.git` folder (stores commit history & tracking info)

Git does not automatically track files.  
You must add files to the **staging area**:

```bash
git add filename.ext
```

Then commit changes:

```bash
git commit -m "your message"
```

View commit history:

```bash
git log
```

---

## 👤 Configure Git User

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

---

## 📦 Staging & Committing

Add single file:

```bash
git add file.ext
```

Add all files:

```bash
git add .
```

Commit directly (skip manual staging for tracked files):

```bash
git commit -a -m "message"
```

Check differences:

```bash
git diff
```

Remove file from tracking:

```bash
git rm --cached file.ext
```

---

## 🌍 Connect Local Repository to GitHub

```bash
git init
git add .
git commit -m "message"
git remote add origin https://github.com/username/repository.git
git branch -M main
git push -u origin main
```

---

## 🏷️ Git Tags

Tags are version names given to commits.

```bash
git tag
git tag -a v1.0 -m "Version 1.0"
git show v1.0
git push origin v1.0
```

---

## 🌿 Branching

Switch branch:

```bash
git checkout branchname
# or
git switch branchname
```

Create & switch to new branch:

```bash
git checkout -b branchname
# or
git switch -b branchname
```

View branches:

```bash
git branch
```

Delete local branch:

```bash
git branch -d branchname
```

Delete remote branch:

```bash
git push origin --delete branchname
```

---

## 🔀 Merging

```bash
git merge feature-branch
```

---

## 🔁 Rebase

```bash
git rebase branchname
```

Use:
- `merge` → keep feature history
- `rebase` → clean linear history

---

## ⚠️ Merge Conflict

Occurs when two branches modify the same line of code.  
You must manually choose which changes to keep, then:

```bash
git add .
git commit -m "resolved conflict"
```

---

## 🔄 Pull & Push

Push (local → remote):

```bash
git push origin main
```

Pull (remote → local):

```bash
git pull origin main
```

---

## 🧳 Git Stash

Temporarily save unfinished work:

```bash
git stash
git stash list
git stash apply
```

---

## 🍴 Git Fork

Fork creates a copy of someone else's repository into your GitHub account.  
You can modify it freely and later create a **Pull Request** to contribute changes.

---

## 🔁 Pull Request

After pushing changes to your fork:
1. Go to GitHub
2. Click **Pull Requests**
3. Select base repository
4. Click **Create Pull Request**

---

<br>

<p align="center">
  <img src="https://git-scm.com/images/logos/downloads/Git-Logo-2Color.png" width="200">
</p>

<p align="center">
  Made with ❤️ while learning Git
</p>
