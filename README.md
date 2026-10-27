<div align="center">

# 🎨 Artify Studio (CanvasCraft)

### Next-Generation Open-Source Graphic Design Suite & Canva Alternative

[![Next.js](https://img.shields.io/badge/Next.js-16.0-black?style=for-the-badge&logo=next.js)](https://nextjs.org/)
[![React](https://img.shields.io/badge/React-19.0-61DAFB?style=for-the-badge&logo=react)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-3178C6?style=for-the-badge&logo=typescript)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-CSS%20v4-38B2AC?style=for-the-badge&logo=tailwind-css)](https://tailwindcss.com/)
[![Konva](https://img.shields.io/badge/Canvas-Konva.js-00C4CC?style=for-the-badge)](https://konvajs.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-purple?style=for-the-badge)](./LICENSE)

<p align="center">
  <b>Artify Studio</b> is a powerhouse, community-driven graphic design platform built for creators, marketers, developers, and educators.
  Create beautiful social posts, presentations, posters, logos, and YouTube thumbnails with an ultra-responsive drag-and-drop HTML5 canvas editor, rich template libraries, AI-powered design layers, and multi-format vector exports.
</p>

[Explore Features](#-core-features) • [Quick Start](#-quick-start) • [Architecture](#-project-architecture) • [Database Setup](#-database-setup) • [Author & License](#-author--license)

</div>

---

## 🌟 Core Features

### 🖌️ Studio-Grade Drag & Drop Editor
- **Hardware-Accelerated Canvas:** Built with **Konva** and **React-Konva** for 60fps rendering, smooth panning, rotation, and precision zooming.
- **Rich Shape & Vector Library:** Rectangles, rounded corners, ellipses, stars, polygons, and custom SVG paths with gradient and pattern fills.
- **Curved Text & Typography:** Professional arc curve effects ($-180^\circ \dots +180^\circ$), 60+ curated Google Font families, letter-spacing, and line-height controls.
- **Canva-Style Interactive Tables:** Native inline table editing, dynamic row/column insertion, cell border styling, and SVG export.
- **Image Frames & Clipping:** Drop photos onto circular, hexagonal, star, or rounded frames with automatic aspect-ratio clipping.

### 📚 Pre-Built Template Ecosystem
- **All Formats Included:** Instagram Posts (1:1), Stories (9:16), YouTube Thumbnails (16:9), Business Presentation Decks, Letterheads, and Logo marks.
- **Zero Lock-In:** All template geometries and styling are stored right in the repository (`src/lib/templates.ts`) and instantly seedable to your database.

### 🤖 AI Design Copilot & Magic Layers
- **Magic Layers Decomposition:** Upload any flat image and let AI vision detect and reconstruct it into native editable Artify vector elements and text.
- **Artify AI Assistant:** Chat copilot for generating headlines, captions, color palettes, and contextual translations.
- **Background Removal:** Seamless browser-based background cutout powered by `@imgly/background-removal`.

### 👥 Real-Time Multiplayer Collaboration
- **Live Cursors & Presence:** Collaborate on the same canvas with colored multiplayer cursors, participant avatars, and live selection rings.
- **Canvas Pin Comments:** Drop anchored comment threads anywhere on the canvas or pin directly to elements.

### 💾 Versatile Export Engine
- **SVG:** True vector export without rasterization.
- **PNG & JPEG:** High-DPI transparent export for digital publishing.
- **PDF:** Print-ready documents with multi-page support.
- **MP4 / WebM Video:** Animate design slides and export full video files right in the browser.

---

## 🏗 Project Architecture

```
canvascraft/
├── prisma/                     # Database Schema & Seeding Engine
│   ├── schema.prisma           # PostgreSQL models (Design, Template, Version, Presence)
│   └── seed.ts                 # Template auto-loader script
├── public/                     # Static Brand Assets & Media
│   ├── logo.svg                # Artify Studio brand mark
│   └── photos/                 # Curated starter stock imagery
├── src/
│   ├── app/                    # Next.js 16 App Router
│   │   ├── (dashboard)/        # Template browser & project gallery
│   │   ├── editor/             # Studio canvas editor route
│   │   ├── api/                # AI, export, and collaboration endpoints
│   │   └── layout.tsx          # Root layout with Google Fonts
│   ├── components/             # UI Components (Editor, Canvas, Panels, Landing)
│   ├── hooks/                  # Custom React hooks (collaboration, history, state)
│   ├── lib/                    # Canvas algorithms, SVG export, and template definitions
│   └── store/                  # Zustand global editor stores
├── package.json                # Project dependencies
└── README.md                   # Artify Studio documentation
```

---

## 🚀 Quick Start

### 1. Clone & Enter Directory
```bash
git clone https://github.com/yashsingh-14/canvascraft.git
cd canvascraft
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Configure Database
Create a `.env` file in the project root (or copy from `.env.example`):
```env
# Default: Zero-config SQLite (works instantly on Windows/Mac/Linux without external servers)
DATABASE_URL="file:./dev.db"

# Or if deploying with PostgreSQL (Supabase, Neon.tech, Docker, etc.):
# DATABASE_URL="postgresql://user:password@localhost:5432/canvascraft?sslmode=require"
```

### 4. Push Schema & Seed Templates
```bash
npx prisma db push
npm run db:seed
```

### 5. Start Development Server
```bash
npm run dev
```
Open [http://localhost:3000](http://localhost:3000) to start designing!

---

## 👨‍💻 Author & License

- **Project Lead & Enhancements:** **Yash Singh** ([@yashsingh-14](https://github.com/yashsingh-14))
- **Based on Open-Source Core:** Canvix by Ashiq Hussain Mir
- **License:** [MIT License](./LICENSE) — Free for personal and commercial usage.

---
<div align="center">
  <b>Artify Studio</b> • Craft Beautiful Designs Without Limits.
</div>
