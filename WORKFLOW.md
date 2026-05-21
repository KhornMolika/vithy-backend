# Vithy Development Workflow

## Purpose

This document defines the Git branching strategy and development workflow to ensure smooth collaboration and prevent merge conflicts.

---

# Repository Structure

Repositories:

- vithy_backend
- vithy_frontend

Branch structure:

main
dev
feature/*

---

# Branch Description

## main

Purpose:
- Stable branch
- Production/demo-ready code

Rules:
- No direct commits
- Only merge from dev

---

## dev

Purpose:
- Integration branch
- Combine completed features

Rules:
- Developers merge completed work here

---

## feature/*

Purpose:
- Individual feature development

Examples:

feature/login
feature/profile
feature/database
feature/devops-ci

Rules:
- Create from dev
- Merge back to dev

---

# Development Process

Step 1 — Get latest changes

git checkout dev
git pull origin dev

---

Step 2 — Create feature branch

git checkout -b feature/<feature-name>

Example:

git checkout -b feature/login

---

Step 3 — Develop feature

Commit regularly:

git add .
git commit -m "Implement login feature"

---

Step 4 — Push branch

git push origin feature/login

---

Step 5 — Create Pull Request

feature/* → dev

Review before merging.

---

Step 6 — Merge to main

After testing:

dev → main

---

# Merge Rules

Allowed:

feature/* → dev
dev → main

Not Allowed:

feature/* → main

---

# Conflict Resolution

If conflicts occur:

git pull origin dev

Resolve conflicts

git add .
git commit

Push again.

---

# Release Process

main → Stable Release

Tag releases:

v1.0
v1.1
v1.2

---

# Team Responsibility

Developer
- Develop feature branches

DevOps
- Maintain workflow
- Manage branches
- Support integration

Team Leader
- Review merges
