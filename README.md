# Metro Nexus Festival OS

AI-Based Dynamic Event Scheduling and Conflict Resolution System for Large-Scale Festivals — built with the MERN stack.

## Features

- **Admin Portal**: Full festival management with professional dashboard sidebar
- **User Portal**: Event browsing, registration, personalized schedule, AI recommendations
- **AI Scheduling**: OpenAI-powered schedule generation and conflict resolution
- **Conflict Detection**: Timing, venue, resource, staff, and capacity conflicts
- **Reports**: Participation, venue/resource utilization, exports to Excel

## Tech Stack

- **Frontend**: React 18, Vite, Tailwind CSS, React Router
- **Backend**: Node.js, Express, MongoDB, Mongoose
- **AI**: OpenAI API (with rule-based fallback)

## Prerequisites

- Node.js 18+
- MongoDB running locally

## Setup

```bash
# Install all dependencies
npm install
npm run install:all

# Copy environment file
copy server\.env.example server\.env

# Seed database with sample data (8 categories, 8 events, etc.)
npm run seed

# Start development servers
npm run dev
```

- **Frontend**: http://localhost:5173
- **Backend API**: http://localhost:5000

## Demo Credentials

| Role  | Email                  | Password  |
|-------|------------------------|-----------|
| Admin | admin@metronexus.com   | admin123  |
| User  | sarah@example.com      | user123   |

## Seed Data

The seed script creates:
- 1 admin + 7 users
- 8 event categories (Music, Dance, Drama, Technical, Sports, Food, Cultural, Art)
- 8 brands/sponsors
- 8 venues
- 8 resources
- 8 staff members
- 8 festival events
- Sample registrations, conflicts, notifications, feedback

## OpenAI Configuration

Add your OpenAI API key in **Admin → Settings** or set `OPENAI_API_KEY` in `server/.env`. Without a key, the system uses intelligent rule-based fallbacks.

## Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start API + client concurrently |
| `npm run seed` | Populate database with demo data |
| `npm run build` | Build client for production |
