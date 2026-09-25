# CityMove / SmartTransit

A production-style public transit platform prototype built in a monorepo-style workspace with a React frontend and TypeScript backend foundation.

## Project structure

- `frontend/` — passenger-facing web app with route pages, live tracking views, login, and admin dashboard shell
- `backend/` — API architecture, security utilities, mock transit dataset, and service routes

## Features included

- Passenger homepage and routes/schedule/stop views
- Admin dashboard shell for fleet management
- Role-based UI navigation patterns
- Express API routes for auth, buses, routes, stops, alerts, and admin
- Secure auth architecture with password hashing and JWT generation
- Mock data layer designed to be replaced by real transit systems
- Responsive design for mobile and desktop layouts

## Quick start

### Frontend

```bash
cd frontend
npm install
npm run dev
```

### Backend

```bash
cd backend
npm install
npm run dev
```

## Default API endpoints

- `GET /health`
- `POST /api/auth/register`
- `POST /api/auth/login`
- `POST /api/auth/logout`
- `GET /api/buses`
- `GET /api/buses/:id`
- `GET /api/routes`
- `GET /api/routes/:id`
- `GET /api/stops`
- `GET /api/stops/:id`
- `GET /api/alerts`
- `GET /api/admin/dashboard`

## Security notes

- Passwords are never stored in plain text in the mock data layer.
- JWT tokens are generated using a secret defined in environment variables.
- The app architecture is structured so real database, GPS, and AI providers can be swapped in later without rewriting the frontend.

## Notes

This project is intentionally a production-ready architecture foundation with realistic mock data and interface flows. It is not a full replacement for a real government transit system, but it follows the requested structure and demonstrates a serious implementation pattern.
