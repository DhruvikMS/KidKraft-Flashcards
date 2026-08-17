# KidKraft Flashcards

<p align="center">
  <strong>Interactive educational flashcards platform for early learning</strong>
</p>

<p align="center">
  <a href="https://kidkraft.onrender.com">Live Demo</a> ·
  <a href="https://github.com/DhruvikMS/Project-KidKraft">Original Deployment Repository</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/React-18-61DAFB?logo=react&logoColor=white" alt="React" />
  <img src="https://img.shields.io/badge/TypeScript-5.6-3178C6?logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Node.js-18+-339933?logo=node.js&logoColor=white" alt="Node.js" />
  <img src="https://img.shields.io/badge/Tailwind_CSS-3-06B6D4?logo=tailwindcss&logoColor=white" alt="Tailwind CSS" />
  <img src="https://img.shields.io/badge/Vite-6-646CFF?logo=vite&logoColor=white" alt="Vite" />
</p>

## Overview

KidKraft Flashcards is a responsive educational product website designed to showcase children's flashcard collections across topics such as alphabets, animals, birds, fruits, vegetables, numbers, and colors/shapes.

The project combines a modern React frontend with a Node.js/Express API layer. It was built as a practical full-stack web application rather than a static landing page, with reusable UI components, typed data models, product detail views, category filtering, blog content, and a contact workflow.

## Key Features

- Responsive product showcase for educational flashcard collections
- Category-based product discovery
- Dedicated product detail pages
- Reusable React component architecture
- REST API for products, categories, blogs, and contact submissions
- Type-safe shared schemas with Zod
- Interactive UI components using Radix UI
- Client-side data fetching with TanStack React Query
- Responsive navigation and mobile-friendly layouts
- Motion and interaction effects with Framer Motion
- Cloud-hosted product imagery
- Production build configuration for frontend and backend

## Tech Stack

| Layer | Technologies |
|---|---|
| Frontend | React, TypeScript, Vite |
| Styling | Tailwind CSS, CSS |
| UI | Radix UI, Lucide React |
| State / Data Fetching | TanStack React Query |
| Backend | Node.js, Express |
| Validation | Zod, drizzle-zod |
| Animation | Framer Motion |
| Build | Vite, esbuild |
| Deployment | Render |

## Architecture

```text
┌───────────────────────────────┐
│        React + Vite           │
│  Pages • Components • Hooks   │
└───────────────┬───────────────┘
                │ REST API
                ▼
┌───────────────────────────────┐
│       Node.js + Express       │
│ Products • Blogs • Contact    │
└───────────────┬───────────────┘
                ▼
┌───────────────────────────────┐
│        Storage Layer          │
│  Typed application data       │
└───────────────────────────────┘
```

See [`docs/architecture.md`](docs/architecture.md) for more detail.

## Project Structure

```text
├── client/
│   ├── src/
│   │   ├── components/
│   │   │   ├── home/
│   │   │   ├── layout/
│   │   │   └── ui/
│   │   ├── hooks/
│   │   ├── lib/
│   │   └── pages/
│   └── index.html
├── server/
│   ├── index.ts
│   ├── routes.ts
│   ├── storage.ts
│   └── vite.ts
├── shared/
│   └── schema.ts
├── docs/
│   └── architecture.md
├── .env.example
├── .gitignore
├── LICENSE
├── package.json
├── tsconfig.json
├── tailwind.config.ts
└── vite.config.ts
```

## Getting Started

### Prerequisites

- Node.js 18+
- npm

### Installation

```bash
git clone https://github.com/DhruvikMS/KidKraft-Flashcards.git
cd KidKraft-Flashcards
npm install
```

### Environment

Create a local `.env` file from the example:

```bash
cp .env.example .env
```

At minimum, set a strong local `SESSION_SECRET`.

### Run locally

```bash
npm run dev
```

The development server runs on port `5000` by default.

### Type-check

```bash
npm run check
```

### Production build

```bash
npm run build
npm start
```

## API Endpoints

| Method | Endpoint | Purpose |
|---|---|---|
| GET | `/api/products` | Return all products |
| GET | `/api/products/category/:category` | Filter products by category |
| GET | `/api/products/:id` | Return a product and its images |
| GET | `/api/blogs` | Return blog posts |
| POST | `/api/contact` | Validate and submit contact information |

## Portfolio Note

This repository is the **clean showcase version** of the KidKraft project. The original deployment/source repository is intentionally kept separate so the live project remains untouched.

- **Showcase repository:** `DhruvikMS/KidKraft-Flashcards`
- **Original repository:** `DhruvikMS/Project-KidKraft`
- **Live application:** https://kidkraft.onrender.com

## Resume Description

> **KidKraft Flashcards — React, TypeScript, Node.js, Tailwind CSS:** Developed and deployed a responsive educational e-commerce platform with reusable React components, category-based product discovery, product detail views, REST APIs, type-safe validation, and a Node.js/Express backend.

## Future Improvements

- Persistent production database for contact submissions
- Authentication and admin product management
- Automated testing and API integration tests
- SEO metadata and structured product data
- Accessibility audit and automated Lighthouse checks
- Analytics for product/category engagement

## License

This project is licensed under the MIT License. See [`LICENSE`](LICENSE).
