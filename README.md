# 🫧 UCReview: AI-Powered Academic Validation

<p align="left">
  <img src="https://img.shields.io/badge/Research-FEUP-ebbcba?style=for-the-badge" height="25" />
  <img src="https://img.shields.io/badge/Stack-Django_|_React_|_LLM-e0def4?style=for-the-badge" height="25" />
  <img src="https://img.shields.io/badge/DevOps-Docker_|_Nginx-ebbcba?style=for-the-badge" height="25" />
</p>

> **A Full-Stack Research Project developed at FEUP** > Architecting an automated solution to untangle the complexity of university course descriptions (Fichas de UC) using a multi-provider AI factory.

---

## 📸 Product Showcase

<p align="center">
  <img src="./assets/main-dashboard.png" width="80%" alt="UCReview Dashboard" />
</p>

<details>
  <summary><b>🔍 View more screenshots</b></summary>
  <br />
  <p align="center">
    <img src="./assets/mobile-view.png" width="30%" />
    <img src="./assets/ai-report.png" width="65%" />
  </p>
</details>

---

## 📖 Project Overview

During my **Research Grant (BII)** at the University of Porto, I solved a major administrative bottleneck: the manual validation of thousands of Course Information Sheets. I built **UCReview** to automate the detection of inconsistencies in ECTS, language compliance, and learning outcomes using state-of-the-art AI.



## 🛠️ Tech Stack & Advanced Architecture

I architected a modular, containerized ecosystem designed for high-concurrency data processing:

* **🤖 Multi-Provider LLM Factory:** Implemented a **Factory Pattern** in Python to interface with **OpenAI, Anthropic, and DeepSeek**. This allows for dynamic model switching, preventing vendor lock-in.
* **⚡ Asynchronous Orchestration:** Powered by **Django** & **Celery** (Redis). Compute-intensive tasks—scraping and semantic AI analysis—are offloaded to background workers to keep the UI snappy.
* **📊 High-Performance Ingestion:** Engineered a native **PostgreSQL Scrapy pipeline**. Using **Atomic Upsert (ON CONFLICT)** logic, the system synchronizes thousands of records from SIGARRA with 100% relational integrity.
* **🌐 Web Server & Proxy:** Configured **Nginx** as a reverse proxy. Optimized with 300s timeouts for long-running AI operations and SPA routing for the **React/Tailwind** dashboard.
* **🐳 DevOps:** Fully containerized with **Docker** (Dev/Prod parity). Orchestrated via a centralized **Makefile** for streamlined deployments.

---

## 🧠 The "Brain-Knot" Challenges

* **The OIDC Implementation:** Mastered the **OpenID Connect (OIDC)** authorization code flow to ensure seamless SSO integration with the university's identity provider.
* **Normalization of "Dirty" Data:** Built robust Python parsers to clean SIGARRA’s inconsistent data (nested HTML/Markdown) before it hits the LLM layer.
* **LLM Response Determinism:** Solved the "unpredictable output" problem by implementing strict **JSON serialization** and validation schema on AI-generated audits.
* **Infrastructure Ownership:** Managed full deployment on a **Linux VM**, configuring the network stack and environment security within the university’s infrastructure.

---

## 🗝️ Institutional Notice

**Note on Code Availability:** This project was developed as part of a formal **Research Grant (BII)** at FEUP. To respect institutional intellectual property, the source code is kept in a **private repository**.

**I am happy to discuss the system design, architecture decisions, and AI prompting strategies during an interview!**

---

### 💌 Let's Connect!

<p align="left">
<a href="https://www.linkedin.com/in/mcaalmeida/" target="blank"><img src="https://img.shields.io/badge/LinkedIn-ebbcba?style=for-the-badge&logo=linkedin&logoColor=white" height="28" /></a>&nbsp;
<a href="https://github.com/mariana2103" target="blank"><img src="https://img.shields.io/badge/Portfolio-e0def4?style=for-the-badge&logo=github&logoColor=191724" height="28" /></a>
</p>
