# CDR Advogados — Website

Site institucional da CDR Advogados, construído com **React + Vite + TypeScript + Tailwind CSS + shadcn/ui**.

## Stack

- **React 18** + **TypeScript**
- **Vite** (bundler)
- **Tailwind CSS** + **shadcn/ui** (UI components)
- **Supabase** (auth + database + edge functions)
- **React Router v6** (client-side routing)
- **TanStack Query** (server state)

---

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/your-org/cdr-website.git
cd cdr-website
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

Copy the example file and fill in your Supabase credentials:

```bash
cp .env.example .env.local
```

Open `.env.local` and set:

```
VITE_SUPABASE_URL=https://your-project-id.supabase.co
VITE_SUPABASE_ANON_KEY=your-anon-public-key
```

> ⚠️ Never commit `.env.local`. It is listed in `.gitignore`.

### 4. Run locally

```bash
npm run dev
```

Open [http://localhost:8080](http://localhost:8080).

---

## Deploying to Vercel

1. Push to GitHub.
2. Import the repo in [vercel.com](https://vercel.com).
3. Add environment variables in **Vercel → Project → Settings → Environment Variables**:
   - `VITE_SUPABASE_URL`
   - `VITE_SUPABASE_ANON_KEY`
4. Deploy. The `vercel.json` already handles SPA routing rewrites.

> In Supabase → Authentication → URL Configuration, add your Vercel production URL to **Redirect URLs** (e.g. `https://cdr-advogados.vercel.app/**`).

---

## Scripts

| Command | Description |
|---|---|
| `npm run dev` | Start dev server |
| `npm run build` | Production build |
| `npm run preview` | Preview production build locally |
| `npm run lint` | Run ESLint |
