# Frontend Developer Intern - Starter Project

## Features
- Next.js + TailwindCSS frontend
- Node.js + Express backend with MongoDB
- JWT-based auth (signup/login)
- User profile fetch/update
- Tasks CRUD (create/read/update/delete)
- Search + filter tasks
- Password hashing (bcrypt)
- Protected routes (token required)

## Setup

### Backend
1. cd backend
2. npm install
3. create .env (see .env.example)
4. start MongoDB
5. npm run dev

### Frontend
1. cd frontend
2. npm install
3. create .env.local with NEXT_PUBLIC_API_URL=http://localhost:5000/api
4. npm run dev

## Postman
Import `postman_collection.json` and use to test APIs.

## How to run tests / quick manual test
1. Register user via frontend
2. Login -> redirected to dashboard
3. Create task, edit, delete, search

## How to scale (short note)
- **Frontend:** split pages into feature modules, use API client with retries, lazy-load heavy components, use SSR/SSG for public pages, host on Vercel or Netlify, CDN for assets, auth cookies (httpOnly) for security.
- **Backend:** separate services (auth, api), containerize with Docker, use managed DB (Atlas/Postgres RDS), use Redis for sessions/cache, use K8s for scaling, add rate-limiting & helmet for security, use structured logging & observability (Prometheus/Grafana).
