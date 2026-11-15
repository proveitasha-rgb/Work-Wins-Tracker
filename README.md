# Proof — Work Wins Tracker

A polished, privacy-first career tool for documenting achievements and turning them into performance review evidence.

![Status](https://img.shields.io/badge/status-MVP-6c4bdb) ![React](https://img.shields.io/badge/React-18-61dafb) ![TypeScript](https://img.shields.io/badge/TypeScript-5-3178c6) ![License](https://img.shields.io/badge/license-MIT-green)

## Why this exists

People do meaningful work all year, then struggle to remember specific examples when review season arrives. Proof makes it easy to capture accomplishments as they happen, with impact and collaborators attached.

## Features

- Log wins with title, contribution, impact, category, date, and collaborators
- Dashboard with total wins, active months, and wins with impact
- Search and category filtering
- Performance review builder that compiles your wins into a structured draft
- Export all wins as CSV or your review draft as plain text
- Optional fictional sample-data preview (clearly labeled)
- Responsive desktop and mobile interface
- Browser-only local storage; no backend, analytics, login, or API keys

## Run locally

Requirements: Node.js 20.19+ or 22.12+ and npm.

```bash
npm install
npm run dev
```

Open the local URL shown in the terminal (usually `http://localhost:5173`).

To verify a production build:

```bash
npm run build
npm run preview
```

## Publish to GitHub

Create a new **empty** GitHub repository named `work-wins-tracker` (do not initialize with a README), then run:

```bash
git init
git add .
git commit -m "Build Proof work wins tracker MVP"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/work-wins-tracker.git
git push -u origin main
```

Replace `YOUR_USERNAME` with your GitHub username. GitHub may prompt you to authenticate.

## Deploy for free

On [Vercel](https://vercel.com) or [Netlify](https://www.netlify.com), import the GitHub repository. Framework: Vite. Build command: `npm run build`. Output directory: `dist`.

## Project structure

```text
work-wins-tracker/
├── src/
│   ├── App.tsx         # Dashboard, forms, review builder, exports
│   ├── main.tsx        # React entry point
│   └── styles.css      # Responsive UI styling
├── index.html
├── package.json
├── tsconfig.json
├── vite.config.ts
├── .gitignore
├── LICENSE
└── README.md
```

## Data and privacy

Wins are stored in `localStorage` under `proof-work-wins-v1`. They stay on the device/browser where they were created. Clearing browser storage, using private browsing, or switching devices can lose your data. **Export CSV regularly as a backup.** No data is sent to a server. This is not suitable for confidential employer information unless your company's policies permit local storage in this browser.

## Limitations / roadmap

This MVP has no accounts, cloud sync, editing existing wins, authentication, or AI generation. Suggested next steps: edit existing entries, year/quarter filters, JSON import/backup, PDF export, user-approved AI-assisted rewriting, and optional encrypted sync.

## License

MIT. See [LICENSE](LICENSE).
