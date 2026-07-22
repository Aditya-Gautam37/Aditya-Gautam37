<!-- ============================================================ -->
<!--  Aditya Gautam — GitHub Profile README                      -->
<!--  Push this to a repo named EXACTLY "Aditya-Gautam37"         -->
<!--  (i.e. github.com/Aditya-Gautam37/Aditya-Gautam37) so        -->
<!--  GitHub renders it on the profile page.                      -->
<!-- ============================================================ -->

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,50:161B33,100:1B1035&height=200&section=header" width="100%"/>

<img src="https://raw.githubusercontent.com/Aditya-Gautam37/Aditya-Gautam37/main/assets/avatar.svg" width="150" height="150" alt="Aditya Gautam"/>

### Aditya Gautam

<img src="https://readme-typing-svg.demolab.com/?font=Fira+Code&weight=600&size=22&duration=2800&pause=900&color=3FA7D6&center=true&vCenter=true&width=560&lines=AI+Engineer;Building+Production-Grade+AI+Systems;Munshi+%E2%80%A2+Material+Checker+%E2%80%A2+Resume+Screener;Learning+by+Shipping%2C+Not+by+Certificate" alt="typing animation" />

<br/>

[![Email](https://img.shields.io/badge/Email-Contact_Me-0D1117?style=for-the-badge&logo=gmail&logoColor=3FA7D6&labelColor=0D1117)](mailto:gautam371202@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0D1117?style=for-the-badge&logo=linkedin&logoColor=3FA7D6&labelColor=0D1117)](https://www.linkedin.com/in/aditya-gautam-4700ab309)
[![Resume](https://img.shields.io/badge/Resume-Download-0D1117?style=for-the-badge&logo=readdotcv&logoColor=3FA7D6&labelColor=0D1117)](https://raw.githubusercontent.com/Aditya-Gautam37/Aditya-Gautam37/main/assets/Aditya_Gautam_Resume.pdf)

<sub>alt. email: singhaditya28255@gmail.com</sub>

<br/><br/>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Aditya-Gautam37/Aditya-Gautam37/output/github-contribution-grid-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Aditya-Gautam37/Aditya-Gautam37/output/github-contribution-grid-snake.svg" />
  <img alt="GitHub contribution snake animation" src="https://raw.githubusercontent.com/Aditya-Gautam37/Aditya-Gautam37/output/github-contribution-grid-snake.svg" width="100%" />
</picture>

</div>

<br/>

## About

I'm an M.Tech Data Science student and AI Engineer who builds AI systems all the way to deployment — not just to a notebook. My flagship project, **Munshi**, is a fully offline GST billing app used by real small businesses; my resume screener processes 1,000+ resumes with 88% match precision; my construction-material assistant is live in production on Vercel.

I'd rather show you a system that handles a bad input gracefully than tell you about a certificate.

| | |
|---|---|
| 🎓 **Education** | M.Tech, Data Science — Gautam Buddha University *(2025–2027, ongoing)* · B.Tech, Computer Science — CGPA 7.25/10 *(2021–2025)* |
| 🎯 **Goal** | AI/ML Engineer building production AI systems that solve real problems |
| 💼 **Experience** | Freelance tutor (Java, C++, full-stack web) — mentored 20+ students, Dec 2024–Jun 2025 |
| 📍 **Currently** | Extending **Munshi**'s Gemini vision pipeline and studying RAG/agentic architectures |

<br/>

## Engineering Philosophy

Every project I build is answerable to the same seven questions. If I can't answer one, the project isn't done.

```
Problem            → What breaks without this, and for whom?
Architecture       → How are the pieces separated and why?
Engineering        → What tradeoffs did I make, and what did they cost?
Optimization       → Where was it slow/wrong, and what fixed it?
Deployment         → Does it run somewhere other than my laptop?
Scalability        → What breaks first under 10x load?
Maintainability    → Could someone else safely change this in six months?
```

The 5-model fallback chain in Material Checker and the multiprocessing rewrite in my resume screener both came from hitting a real limit and fixing the actual bottleneck — not from following a tutorial.

<br/>

## Current Focus

- 🔭 Extending **Munshi**'s offline billing engine and its Gemini-based bill-extraction pipeline
- 🧠 Studying **LangChain, RAG, and agentic architectures** to move from single-call LLM features to multi-step reasoning systems
- 🐳 Deepening **Docker** usage to containerize all three flagship projects
- 📚 Studying **system design** so scaling decisions are made ahead of the bottleneck, not after it

<br/>

## Tech Stack

<div align="center">

<img src="https://skillicons.dev/icons?i=python,js,cpp,java,mysql,tensorflow,pytorch,sklearn,flask,nextjs,git,docker,vercel&theme=dark" />

<sub>+ LangChain · OpenAI API · Gemini API · spaCy · ChromaDB · Pandas · NumPy</sub>

</div>

<br/>

## Featured Projects

| Project | What it does | Engineering focus | Stack |
|---|---|---|---|
| 🧾 **[Munshi](https://github.com/Aditya-Gautam37/Application_Munshi)** | Fully offline GST billing & invoicing desktop app | Gemini vision extraction, bilingual UI, auth, Pytest-covered money logic | Python, Flask, Gemini API, SQLite |
| 🏗️ **[Material Checker](https://github.com/Aditya-Gautam37/material-checker)** | Live AI buying guide for construction materials | 5-model LLM fallback chain, prompt-injection guardrails | Next.js 16, React 19, OpenRouter, Vercel |
| 📄 **[AI Resume Screener](https://github.com/Aditya-Gautam37/-AI-Resume-Screener)** | Semantic resume-to-job matching engine | 88% match precision, vector search, multiprocessing | Python, spaCy, Sentence-Transformers, ChromaDB |

<br/>

## 🧾 Munshi — Offline GST Billing & Invoicing App

**The problem.** Small transport businesses need GST-compliant invoices (*bilty*), payment records, and ledgers — but can't depend on internet access at the point of sale, and can't afford to get GST math wrong.

**What it does**

- Fully offline desktop billing app — generates GST-compliant invoices, records payments, maintains ledgers with zero internet dependency
- **Gemini vision pipeline**: photograph a paper bill, auto-extract the details, and convert it straight into a structured digital *bilty* — cutting manual data entry significantly
- Bilingual (English/Hindi) UI with a guided first-run setup wizard and authentication
- Core money and GST-calculation logic protected by an automated **Pytest** suite — the part of the app that can't be allowed to silently drift

**Engineering decisions worth mentioning**

- Chose a fully offline-first architecture (SQLite, no server dependency) because the target users are small businesses without reliable connectivity — this ruled out a cloud-first design from day one
- Isolated GST/money calculations behind tests specifically because a UI bug is annoying, but a billing bug is a liability
- Used a vision LLM (Gemini) only at the ingestion boundary — once data is structured, the rest of the app never depends on the model being available

**Status:** actively developed — this is the flagship project and the one under continuous iteration.

<br/>

## 🏗️ Material Checker — Live AI Buying Guide

A deployed, publicly usable web app: first-time homeowners describe what they're buying, and get instant, practical construction-material guidance.

- Engineered a **cascading 5-model fallback chain** over the OpenRouter API with automatic retries and rate-limit handling — achieving near-100% uptime while running entirely on free-tier models
- Implemented **3-layer input guardrails** (client-side validation, server-side keyword allowlist, system-prompt scoping) to block off-topic queries and prompt-injection attempts
- Shipped and deployed on Vercel — this one is live, not just demoable locally

This project is the proof that I can take an LLM feature from "works in a demo" to "survives a free-tier rate limit and a hostile input."

<br/>

## 📄 AI Resume Screener & Job Match Engine

- Built an NLP resume-screening tool using **spaCy** for entity extraction and **Sentence-Transformers** for semantic matching against job descriptions — **88% matching precision**
- Stored candidate embeddings in **ChromaDB**, enabling fast cosine-similarity search across **1,000+ resumes**
- Batch-processed 1,000+ resumes with Python **multiprocessing**, cutting total pipeline execution time by **55%**

<br/>

## GitHub Statistics

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=Aditya-Gautam37&show_icons=true&theme=github_dark&hide_border=true&bg_color=0D1117&title_color=3FA7D6&icon_color=D98C5A&text_color=C9D1D9" />
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Aditya-Gautam37&layout=compact&theme=github_dark&hide_border=true&bg_color=0D1117&title_color=3FA7D6&text_color=C9D1D9" />

<img src="https://github-readme-streak-stats.herokuapp.com/?user=Aditya-Gautam37&theme=github-dark-blue&hide_border=true&background=0D1117&ring=3FA7D6&fire=D98C5A&currStreakLabel=3FA7D6" />

<img src="https://github-readme-activity-graph.vercel.app/graph?username=Aditya-Gautam37&theme=github-compact&hide_border=true&bg_color=0D1117&color=3FA7D6&line=D98C5A&point=C9D1D9" width="100%"/>

</div>

<br/>

## Learning Journey

- [ ] LangChain, RAG systems, and agentic architectures
- [ ] Docker → containerize Munshi, Material Checker, and the Resume Screener
- [ ] Cloud deployment beyond single-service PaaS hosting
- [ ] System design fundamentals (scaling, caching, queues)
- [ ] Deeper Transformer fine-tuning workflows

<br/>

## Milestones

- Shipped **Munshi**, a fully offline, production-ready GST billing app with an integrated Gemini vision pipeline
- Deployed **Material Checker** live on Vercel with a 5-model fallback chain and prompt-injection defenses
- Built a resume-matching engine hitting **88% precision** across 1,000+ resumes, with a 55% faster batch pipeline
- Mentored 20+ students in programming and full-stack web development as a freelance tutor
- Currently pursuing an **M.Tech in Data Science** while shipping outside the classroom

<br/>

## Open Source Goals

- Publish Munshi's GST-calculation and invoice-generation modules as a standalone, reusable library once the core app stabilizes
- Contribute to open-source LLM-tooling projects (fallback/retry orchestration, prompt-injection guardrails) — direct extensions of the Material Checker work
- Start reviewing and responding to issues on projects I depend on, not just filing my own

<br/>

## Future Vision

The next 12 months are about turning three solid solo projects into a portfolio that reads as production engineering: containerized deployments, monitoring, and at least one project rebuilt around RAG or agentic reasoning rather than single-shot LLM calls. Long-term, I want to be the engineer a team hands an ambiguous "make AI understand our documents/process/data" problem to — and trusts to come back with something that ships and holds up.

<br/>

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1B1035,50:161B33,100:0D1117&height=100&section=footer" width="100%"/>

*Building in public. Open to internships and full-time AI/ML engineering roles.*

</div>
