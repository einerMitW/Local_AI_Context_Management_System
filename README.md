# Local AI Context Management System

This project provides a standardized, portable, and file-based framework to manage how AI agents interact with your projects. 

Inspired by the **"File over AI"** philosophy, this system ensures that your project's identity, rules, and knowledge are not locked into a specific AI platform but reside locally within your workspace as Markdown files.

---

## 🛠️ Setup Guide

To implement this system in your project, follow these steps:

### 1. Scaffolding
Copy the `Local_AI_Context_Management` folder structure to the root of your project.

### 2. Alignment (The Identity Layer)
Fill out the templates in the `Identity/` folder:
- **`me.md`**: Tell the AI who you are, your communication preferences, reasoning standards, and non-negotiables.

### 3. Knowledge Curation (The Context Layer)
Define the project's situational knowledge:
- **`Context/standards.md`**: Document your code style, documentation rules, and technical requirements, Tasks, Storys, ...

### 4. Capability Definition (The Skills Layer)
Teach the AI how to perform specific tasks:
- **`Skills/skills-map.md`**: List the available SOPs.
- **`Skills/[task]-sop.md`**: Use the provided template to create modular instructions (under 200 lines) for repetitive tasks like auditing, drafting, or deployment.

---

## 📖 How to Use the System

### For the User
- **Gardening**: Regularly update `Memory/learnings.md` when the AI makes a mistake or when your preferences change.
- **Surgical Context**: Don't dump everything into one file. Use the folder structure to keep context lean and relevant.

### For the AI Agent
When an AI agent enters the project, its **Boot Process** is governed by the `INSTRUCTIONS.md` file at the root:

1. **Read `Vault_map.md`**: The agent learns the structure of your "Superbrain".
2. **Read `Identity/`**: The agent aligns its tone and behavior with your preferences.
3. **Read `Memory/learnings.md`**: The agent "remembers" past feedback to avoid repeating errors.
4. **Use `Context/Content-map.md`**: The agent navigates the repo efficiently without scanning every folder.

---

## 📂 System Architecture

- **`Identity/`**: Who you are and how the AI should behave.
- **`Context/`**: What the AI needs to know about the current project.
- **`Skills/`**: Modular, repeatable workflows (SOPs).
- **`Memory/`**: Persistent history of decisions and self-improvement feedback.
- **`Vault_map.md`**: The master navigational index for the AI.
- **`INSTRUCTIONS.md`**: The mandatory onboarding hook for every session.

---

## 💡 Best Practices
- **Progressive Disclosure**: Only load deep-level information when strictly necessary.
- **The 200-Line Rule**: Keep SOPs and instruction files short to maximize AI focus and minimize token usage.
- **Chainloading**: This system acts as a local extension of your global Agentic OS rules.

---
