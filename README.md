# laya-web

Playground for [laya-api](../laya-api): state + questions on the left, response on the right.

The only config is `VITE_API_BASE_URL` (build-time, see `.env.example`).

```bash
pnpm install
VITE_API_BASE_URL=http://localhost:8008 pnpm dev      # http://localhost:3007
```

Deploy: any static host (Vercel/Netlify: set `VITE_API_BASE_URL`, build `pnpm build`, output `dist`), or Docker:

```bash
docker build --build-arg VITE_API_BASE_URL=https://api.example.com -t laya-web .
docker run -d -p 3007:80 laya-web
```
