# Architecture

KidKraft Flashcards follows a lightweight full-stack TypeScript architecture.

```text
React + Vite
    │
    ├── Pages & reusable UI components
    │
    └── TanStack Query
             │
             ▼
       Express API
             │
             ▼
       Storage layer
```

## Frontend

- React 18
- TypeScript
- Vite
- Tailwind CSS
- Radix UI primitives
- Framer Motion
- TanStack React Query

The frontend lives under `client/` and is organized into pages, reusable components, hooks, and shared utilities.

## Backend

The Express server lives under `server/`.

Key API routes include:

- `GET /api/products`
- `GET /api/products/category/:category`
- `GET /api/products/:id`
- `GET /api/blogs`
- `POST /api/contact`

## Shared types

`shared/schema.ts` contains the shared data definitions used by the client and server.

## Data model

The current implementation uses an in-memory storage layer for the portfolio/demo application. Product content and product imagery are defined in the server-side data layer and served through the API.
