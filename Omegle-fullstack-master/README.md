<h1 align = "center"> 

![iggle](https://github.com/amitanshusahu/Omegle-fullstack/assets/83657737/fdeae2a5-a5aa-456a-9160-aeb87e265e8c)


</h1>


---

<div align="center">
  
![gihub-thumbnail](https://github.com/amitanshusahu/Omegle-fullstack/assets/83657737/7371b48d-da29-4c9b-bbb9-7b6e73207935)

[🔴 watch demo on youtube](https://youtu.be/GZyKcIvQqi8)

</div>

---

## 📌 Set up project
- clone the repo and go into it
```bash
git clone https://github.com/amitanshusahu/Omegle-fullstack/ & cd Omegle-fullstack/
```
- go to the client folder and start dev server
```bash
cd client && npm run dev
```
- go to the server folder and start server
```bash
cd ../server && npm start
```

## Useful Links

- [WebRTC Crash Course - deep dive](https://youtu.be/FExZvpVvYxA)

---

## 🚀 Deploying (simple path)

This repo contains a separate frontend (`client/`) and backend (`server/`). The easiest, most reliable way to deploy is to host the backend on a Node host (Render, Railway, Fly, etc.) and deploy the frontend on Vercel. 

Quick steps (Option 1):

1. Deploy the `server/` folder to Render/Railway/Fly using the default `npm start` (it runs `tsc && node dist/index`). Make sure to set `PORT` and, optionally, `CLIENT_ORIGIN` (CORS) in service environment variables.
2. In the `client/` set `VITE_BACKEND_URL` to your backend URL (for example `https://your-backend.onrender.com`) and add it in Vercel Project Settings as `VITE_BACKEND_URL`.
3. On Vercel, import the GitHub repo and set the Root Directory to `client`. Vercel will detect Vite and run `npm run build`.

Notes:
- The client now reads backend from `VITE_BACKEND_URL` (falling back to `http://localhost:8000` for local development).
- The server uses `process.env.PORT` and `process.env.CLIENT_ORIGIN` for CORS.
- If you prefer a single Vercel project, you can convert the signalling server to serverless functions (advanced). 

---

<h1 align="center"> Star the Repo ⭐ </h1>
