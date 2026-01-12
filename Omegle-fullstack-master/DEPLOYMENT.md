Deployment checklist

Option 1 — Host backend separately + Vercel frontend (recommended)

1. Backend (Render / Railway / Fly)
   - Connect the repo and choose `server` as the service folder.
   - Environment variables to set: `PORT` (usually provided by the host), optionally `CLIENT_ORIGIN` (your frontend origin).
   - Build & Start: `npm install` then `npm start` (package.json uses `tsc && node dist/index`).

2. Frontend (Vercel)
   - Import repo into Vercel and set the **Root Directory** to `client`.
   - Add environment variable `VITE_BACKEND_URL` = `https://<your-backend-domain>`.
   - Deploy. Vercel will run `npm run build` and publish.

Quick local testing

- Run client locally: `cd client && npm install && npm run dev` (Vite)
- Run server locally: `cd server && npm install && npm start` (server listens on `PORT` or 8000)

Notes

- The client reads `VITE_BACKEND_URL` (fall back to `http://localhost:8000`).
- If you want to put both frontend and backend in one Vercel project, consider rewriting signalling to serverless functions (advanced; not covered here).
