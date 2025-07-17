# Discreet Women’s Safety App (Kenya-focused)

A modern, production-ready MERN stack app for discreet personal safety, featuring a decoy journal UI, hidden SOS, check-in timer, emergency contacts, and customizable preferences. Built for privacy, speed, and reliability.

---

## Features
- **Decoy Journal UI:** Realistic notes app with titles, entries, and deletion.
- **Hidden Navigation:** Swipe gestures reveal SOS and Settings (PIN-gated).
- **SOS Alert:** Sends custom message (with location) to emergency contacts.
- **Check-In Timer:** Set a timer; auto-SOS if not checked in.
- **Emergency Contacts:** Add, edit, delete trusted contacts.
- **Preferences:** Custom SOS message, check-in default, GBV support, vibration.
- **Onboarding Overlay:** Explains gestures on first launch.
- **Dark/Light Mode:** Toggle from journal screen.
- **Mobile-first, accessible, and responsive.**

---

## Tech Stack

## Deployment Status
- Last deployment attempt: 2025-07-17
- Status: Pending
- Triggered by: Version bump
- **Frontend:** React (Vite), CSS, react-swipeable, lottie-react
- **Backend:** Express.js, MongoDB (Mongoose), dotenv
- **DevOps:** GitHub Actions (CI/CD), Render/Netlify (deployment), UptimeRobot (monitoring)

---

## Local Setup

### Prerequisites
- Node.js (v18+ recommended)
- MongoDB Atlas account (or local MongoDB)
- pnpm or npm

### 1. Clone the repository
```bash
git clone <your-repo-url>
cd week-7-devops-deployment-assignment-Vinci-Plath
```

### 2. Backend Setup
```bash
cd backend
pnpm install # or npm install
cp .env.example .env # edit with your MongoDB URI
pnpm start # or npm start
```
- The backend runs on `http://localhost:5001` by default.

### 3. Frontend Setup
```bash
cd ../frontend
pnpm install # or npm install
pnpm dev # or npm run dev
```
- The frontend runs on `http://localhost:5173` by default.

---

## Environment Variables
Create a `.env` file in `/backend`:
```
MONGODB_URI=your_mongodb_connection_string
PORT=5001
```

---

## API Endpoints (Summary)
- `POST /api/contacts` — Add contact
- `GET /api/contacts` — List contacts
- `DELETE /api/contacts/:id` — Delete contact
- `POST /api/sos` — Trigger SOS alert
- `POST /api/checkin/start` — Start check-in timer
- `POST /api/checkin/cancel` — Cancel check-in
- `GET /api/health` — Health check

---

## Deployment & CI/CD
- **CI/CD:** GitHub Actions workflows for build, test, and deploy (see `.github/workflows/`)
- **Backend:** Deploy to Render, Railway, or Heroku
- **Frontend:** Deploy to Vercel, Netlify, or GitHub Pages
- **Update frontend API URLs** to point to your deployed backend

---

## Monitoring
- **Health check:** `/api/health` endpoint
- **Uptime monitoring:** Use UptimeRobot, BetterStack, etc.

---

## Credits
- Built by Vinci-Plath for Week 7 DevOps/Deployment Assignment
- Inspired by real-world safety needs and best practices

---

## License
MIT (or as specified by your instructor) 