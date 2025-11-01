<div align="center">

# ⚡ DevGenie

### *Skip the setup. Start building.*

**DevGenie** is a smart, web-based project scaffolding tool that generates production-ready code structures in seconds — so developers can skip the boilerplate and focus on building features.

[![React](https://img.shields.io/badge/React-19-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://react.dev)
[![React Router](https://img.shields.io/badge/React_Router-7-CA4245?style=for-the-badge&logo=react-router&logoColor=white)](https://reactrouter.com)
[![JSZip](https://img.shields.io/badge/JSZip-3.10-orange?style=for-the-badge)](https://stuk.github.io/jszip/)
[![Vercel](https://img.shields.io/badge/Deploy-Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://vercel.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

</div>

---

## 📋 Table of Contents

- [About the Project](#-about-the-project)
- [Key Features](#-key-features)
- [Why DevGenie?](#-why-devgenie)
- [Technology Stack](#-technology-stack)
- [Screenshots](#-screenshots--preview)
- [Getting Started](#-getting-started)
- [How to Use](#-how-to-use)
- [Project Structure](#-project-structure)
- [Contributing & License](#-contributing--license)

---

## 🧠 About the Project

DevGenie is a **developer productivity platform** that eliminates the repetitive, time-consuming setup work at the start of every new project. Instead of copying old boilerplates or configuring project structures from scratch, you describe what you need — and DevGenie builds it for you instantly as a downloadable ZIP file.

It serves two modes of use:

- **Basic Mode** — Chat-style interface where you describe your stack in plain English and get a complete Node.js project scaffold.
- **Advanced Mode** — Visual configurator where you select language, framework, architecture (MVC, Microservices, Clean, etc.), and opt-in features (Authentication, Database, Docker, Testing) to generate enterprise-grade project structures.

The app connects to a hosted backend API for generation, with a fully functional **local JSZip fallback** if the backend is unavailable — so it works offline too.

---

## ✨ Key Features

| Feature | Description |
|---|---|
| 🤖 **AI-Style Chat Interface** | Describe your project in natural language and get an instant scaffold |
| ⚙️ **Advanced Configurator** | Choose language, framework, architecture, and feature toggles visually |
| 📦 **Template Library** | Browse and download 6+ production-ready project templates |
| 🏗️ **Architecture Selection** | MVC, Microservices, Monolith, Clean Architecture support |
| 🔐 **Auth + DB Scaffolding** | JWT authentication, MongoDB/PostgreSQL models generated on demand |
| 🐳 **Docker Support** | Generates `Dockerfile` and `docker-compose.yml` automatically |
| 🧪 **Testing Scaffolding** | Jest + Supertest test files included when selected |
| ⬇️ **One-Click ZIP Download** | Complete project delivered as a ready-to-extract ZIP file |
| 🎨 **Custom Cursor UI** | Smooth, interactive cursor animations across all pages |
| 📱 **Responsive Design** | Works on desktop and mobile |

---

## 💡 Why DevGenie?

Every developer has wasted hours recreating the same folder structures, copying config files, or googling "express mongoose boilerplate" for the tenth time. DevGenie solves that.

**Target users:**
- Developers starting new side projects or freelance work
- Teams who want a consistent, opinionated project structure from day one
- Students learning backend architecture patterns
- Engineers prototyping quickly before committing to a full stack

**Advantages over manual setup or generic boilerplates:**
- ✅ Tailored to your exact stack — not a one-size-fits-all template
- ✅ Includes real working code: routes, controllers, models, middleware
- ✅ Multiple architecture patterns, not just MVC
- ✅ Works offline via local generation fallback
- ✅ No account required — generate and download instantly

---

## 🛠 Technology Stack

**Frontend**
| Technology | Purpose |
|---|---|
| React 19 | UI framework |
| React Router 7 | Client-side routing |
| React Icons | Icon library (Font Awesome, Simple Icons) |
| JSZip 3.10 | Client-side ZIP file generation (offline fallback) |
| file-saver | Browser file download trigger |
| CSS Modules | Per-page scoped styling |

**Backend API**
| Technology | Purpose |
|---|---|
| REST API | Hosted at `dev-genie-backend.onrender.com` |
| `/api/generate/basic` | Basic project generation endpoint |
| `/api/generate/advanced` | Advanced project generation endpoint |
| `/api/templates` | Template list endpoint |

**Tooling**
| Tool | Purpose |
|---|---|
| Create React App | Build toolchain |
| ESLint | Code quality enforcement |
| Vercel | Frontend deployment |

---

## 📸 Screenshots / Preview

> Screenshots will be added after deployment. Below are placeholders for each page.

| Page | Preview |
|---|---|
| 🏠 **Home** | _Landing page with animated hero, services, and scroll animations_ |
| 🚀 **Get Started** | _Mode selection: Basic vs Advanced_ |
| 💬 **Basic Chat** | _Chat-style interface for quick project generation_ |
| ⚙️ **Advanced Generator** | _Full configurator with language/framework/architecture/features_ |
| 📚 **Templates** | _Browsable template library with search and filter_ |

---

## 🚀 Getting Started

### Prerequisites

- Node.js **v16+**
- npm **v8+**

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/abrsh21son/Dev-genie.git
cd Dev-genie

# 2. Install dependencies
cd client
npm install

# 3. Start the development server
npm start
```

The app opens at **http://localhost:3000**

### Build for Production

```bash
cd client
npm run build
```

### Deploy to Vercel

```bash
npm install -g vercel
cd client
vercel
```

> The `vercel.json` file in `client/` handles SPA routing redirects automatically.

---

## 📖 How to Use

1. **Open the app** at `http://localhost:3000` (or your deployed URL)
2. **Click "Get Started"** on the home page
3. **Choose your mode:**
   - **Basic** → Type a description like *"I want a Node.js setup with Express and MongoDB"* → Hit send → Download ZIP
   - **Advanced** → Select language, framework, architecture, and features → Describe your project → Download ZIP
4. **Browse Templates** for ready-made configurations you can customize or download directly
5. **Extract the ZIP**, run `npm install`, and start coding immediately

---

## 📁 Project Structure

```
Dev-genie/
└── client/                     # React frontend application
    ├── public/                 # Static assets & index.html
    ├── src/
    │   ├── pages/              # One component per route
    │   │   ├── Home.jsx        # Landing page
    │   │   ├── GetStarted.jsx  # Mode selection page
    │   │   ├── ChatBasic.jsx   # Basic chat generator
    │   │   ├── AdvancedChat.jsx# Advanced configurator
    │   │   └── Templates.jsx   # Template browser
    │   ├── services/
    │   │   ├── api.js          # Backend API client
    │   │   ├── backendGenerator.js  # API calls with local fallback
    │   │   └── projectGenerator.js # Local JSZip generation engine
    │   ├── App.js              # Router and route definitions
    │   └── index.js            # React entry point
    ├── vercel.json             # Vercel SPA routing config
    └── package.json            # Dependencies and scripts
```

---

## 🤝 Contributing & License

Contributions are welcome. To contribute:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m "feat: add your feature"`
4. Push and open a Pull Request

This project is licensed under the **MIT License** — free to use, modify, and distribute.

---

<div align="center">

Built with ❤️ by developers, for developers.

**[⬆ Back to top](#-devgenie)**

</div>
