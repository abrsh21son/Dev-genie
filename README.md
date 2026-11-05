# DevGenie

**Skip the setup. Start building.**

A web-based project scaffolding tool that generates production-ready code structures in seconds. Describe your stack, configure your architecture, and download a complete project as a ZIP file — no account required.

---

## What it does

DevGenie eliminates the repetitive boilerplate work at the start of every project. Two modes:

**[01] Basic** — Describe your project in plain English. Get a working Node.js scaffold instantly.

**[02] Advanced** — Select language, framework, architecture pattern, and feature modules. Generate enterprise-grade structures tailored to your exact specification.

**[03] Templates** — Browse a curated library of production-ready templates. Download directly or customize in Advanced mode.

---

## Features

→ Chat-style interface for natural language project description  
→ Visual configurator with language / framework / architecture selectors  
→ Architecture patterns: MVC, Clean, Microservices, Monolith, Serverless, Hexagonal  
→ Feature modules: JWT Authentication, Database integration, Docker, Testing  
→ One-click ZIP download — extract and run immediately  
→ Offline fallback via local JSZip generation engine  
→ Template library with search and filter  
→ Smooth scroll animations and custom cursor UI  

---

## Tech Stack

| Layer | Technology |
|---|---|
| UI Framework | React 19 |
| Routing | React Router 7 |
| Icons | React Icons (Font Awesome, Simple Icons) |
| ZIP Generation | JSZip 3.10 |
| File Download | file-saver |
| Backend API | REST — hosted on Render |
| Deployment | Vercel |
| Build Tool | Create React App |

---

## Getting Started

**Prerequisites:** Node.js v16+, npm v8+

```bash
git clone https://github.com/abrsh21son/Dev-genie.git
cd Dev-genie/client
npm install
npm start
```

Opens at `http://localhost:3000`

```bash
# Production build
npm run build
```

---

## Project Structure

```
Dev-genie/
└── client/
    ├── src/
    │   ├── pages/
    │   │   ├── Home.jsx            # Landing page
    │   │   ├── GetStarted.jsx      # Mode selection
    │   │   ├── ChatBasic.jsx       # Basic generator
    │   │   ├── AdvancedChat.jsx    # Advanced configurator
    │   │   └── Templates.jsx       # Template browser
    │   ├── services/
    │   │   ├── api.js              # Backend API client
    │   │   ├── backendGenerator.js # API calls + offline fallback
    │   │   └── projectGenerator.js # Local JSZip engine
    │   └── App.js                  # Route definitions
    ├── vercel.json                 # SPA routing config
    └── package.json


## License

Abraham Shiferaw , Efrem ktachew , ruth gezahegn , afomiya ketsela 
