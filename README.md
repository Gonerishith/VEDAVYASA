# Vedavyasa EN High School Website

Production-ready full-stack school website built with React + Vite (frontend) and Express + MongoDB (backend).

## Stack

- Frontend: React, Vite, Tailwind CSS, React Router, Axios
- Backend: Node.js, Express.js
- Database: MongoDB (Mongoose)
- Auth: JWT, bcrypt password hashing
- Uploads: Multer (secure image uploads)

## Features

- Public pages: Home, About, Programs, Gallery, Alumni, News & Events, Contact
- Protected admin panel with JWT auth
- Full database-driven content management
- Student management (add/edit/delete/search)
- Gallery management (multi-category image records)
- Alumni management
- News & events management
- Programs management
- School info management (about, mission, vision, contact, stats)
- Contact message inbox in admin panel
- Visitor counter stored in database and shown in dashboard

## Default Admin Login

- Email: `gonerishi21@gmail.com`
- Password: `12345678`

This account is automatically created at backend startup if it does not exist.

## Project Structure

- `src/` frontend app
- `backend/` Express API + MongoDB + uploads

## Local Setup

### 1. Install dependencies

```bash
npm install
npm --prefix backend install
```

### 2. Configure environment

Create `backend/.env` using `backend/.env.example`:

```env
PORT=5000
MONGO_URI=mongodb://127.0.0.1:27017/vedavyasa_school
JWT_SECRET=replace-with-strong-secret
JWT_EXPIRES_IN=1d
CLIENT_URL=http://localhost:8080
PUBLIC_BASE_URL=
DEFAULT_ADMIN_EMAIL=gonerishi21@gmail.com
DEFAULT_ADMIN_PASSWORD=12345678
```

Optional frontend env (`.env` in project root):

```env
VITE_API_BASE_URL=http://localhost:5000/api
```

### 3. Run development

```bash
npm run dev
```

This starts:

- Frontend: `http://localhost:8080`
- Backend: `http://localhost:5000`

## Build

```bash
npm run build
```

## Production Deployment

### Frontend (Vercel)

- Build command: `npm run build`
- Output directory: `dist`
- Env: `VITE_API_BASE_URL=https://your-backend-domain/api`

### Backend (Render/Railway)

- Root directory: `backend`
- Start command: `npm start`
- Set env vars from `backend/.env.example`
- Ensure `CLIENT_URL` points to frontend domain
- Use MongoDB Atlas for `MONGO_URI`

## Notes

- Uploaded images are served from `/uploads` on backend.
- Set a strong `JWT_SECRET` before production.
- Keep `backend/.env` out of version control.
- Place your school logo at `public/school-logo.png` for site-wide branding.
