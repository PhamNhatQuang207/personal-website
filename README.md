# Pham Nhat Quang — Personal Website

A cyberpunk-themed personal portfolio website with a **terminal/dashboard aesthetic** and interactive **3D animations**. Built as a static site with vanilla HTML, CSS, and JavaScript — no frameworks, no build step.

🔗 **Live:** *(deployed on Vercel)*

---

## ✨ Features

### Visual Design
- **CRT scanline overlay** with subtle flicker — the whole page feels like a retro monitor
- **Animated grid background** that slowly scrolls across the viewport
- **Glitch text effect** on the hero heading using CSS `clip-path` and RGB-split
- **Typing animation** that cycles through roles: Software Engineer, Web Developer, Data Enthusiast, Problem Solver
- **Terminal window frames** — content sections styled as bash shells with `$ whoami` commands
- **Hexagonal profile photo** with animated gradient border

### 3D Hero Animation (Three.js)
- Dual wireframe icosahedrons rotating at different speeds
- 300 floating particles creating a starfield effect
- Mouse-reactive camera parallax — the scene responds to cursor position

### Dashboard Skill Panels
- Four color-coded panels: Frontend (green), Backend (cyan), Database (amber), DevOps (purple)
- Animated progress bars that fill to target percentage when scrolled into view
- Live "ACTIVE" status indicators with pulsing dots

### Portfolio Project Cards
- **3D tilt effect** — cards rotate based on mouse position using CSS `perspective` and JS `mousemove`
- Gradient border glow on hover
- Image desaturation that lifts on hover
- Projects link to live deployments (when available)

### Other
- Smooth scroll navigation styled as terminal commands (`./about`, `./skills`, etc.)
- Contact form wired to **Formspree** for message delivery
- Session timer in the footer showing live uptime
- Fully responsive across mobile, tablet, and desktop

---

## 🛠 Tech Stack

| Layer | Technology |
|-------|------------|
| Structure | HTML5 (semantic) |
| Styling | Vanilla CSS (handwritten design system) |
| Typography | [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) + [Orbitron](https://fonts.google.com/specimen/Orbitron) |
| 3D Animation | [Three.js](https://threejs.org/) r128 (via CDN) |
| Scroll Effects | Intersection Observer API |
| Contact Form | [Formspree](https://formspree.io/) |
| Deployment | [Vercel](https://vercel.com/) |

---

## 📁 Project Structure

```
personal-website/
├── build/                  # Production-ready static site
│   ├── index.html          # Main page (HTML + inline JS)
│   ├── css/
│   │   ├── terminal.css    # Complete design system (~890 lines)
│   │   └── style.css       # Legacy Tailwind output (unused)
│   └── img/
│       ├── profile.jpg     # Profile photo
│       ├── slideshow/      # BIC Insurance project screenshots
│       └── fittrack/       # FitTrack project screenshots
├── src/
│   └── input.css           # Legacy Tailwind input (unused)
├── vercel.json             # Vercel deployment config
├── package.json            # Node dependencies (Tailwind — legacy)
├── tailwind.config.js      # Legacy Tailwind config (unused)
└── README.md
```

---

## 🚀 Deployment

### Vercel (recommended)

1. Push the repository to GitHub
2. Import the project in [Vercel](https://vercel.com/)
3. No build command needed — Vercel serves the `build/` directory directly (configured in `vercel.json`)

### Local Preview

Open `build/index.html` directly in your browser — no server required.

Alternatively, use any static file server:

```bash
npx serve build
```

---

## 🎨 Design System

The design system is defined entirely through CSS custom properties in `terminal.css`:

### Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| `--bg-primary` | `#0a0a0f` | Page background |
| `--green` | `#00ff41` | Primary accent, prompts, active states |
| `--cyan` | `#00d4ff` | Secondary accent, links, typing text |
| `--amber` | `#ffb000` | Highlights, warnings, section tags |
| `--purple` | `#b44dff` | Decorative elements |
| `--red` | `#ff3355` | Glitch effect, error states |

### Typography

- **Display:** Orbitron (headings, section titles) — sci-fi geometric
- **Mono:** JetBrains Mono (body text, terminal content) — developer terminal

---

## 📂 Projects Showcased

### BIC Insurance *(deployment discontinued)*
Sales website built during internship at BIC Insurance Company.
- **Frontend:** Angular, TypeScript, AWS Amplify
- **Backend:** ASP.NET, MSSQL, Docker, AWS Elastic Beanstalk, JWT auth

### FitTrack *(live)*
Full-stack MERN fitness tracker for workout planning and body progress monitoring.
- **Frontend:** React 19, Tailwind CSS, Recharts
- **Backend:** Node.js, Express, MongoDB, JWT
- **Deployment:** Vercel (frontend) + Render (backend)
- 🔗 https://fit-track-frontend-gray.vercel.app

---

## 📄 License

© 2025 Pham Nhat Quang. All rights reserved.
