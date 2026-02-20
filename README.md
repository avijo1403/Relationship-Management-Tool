# Relationship Management Tool

> Lightweight full-stack app for managing investors and investments (client + server + functions).

## Contents
- Client: React + Vite (UI components in `client/components`)
- Server: API and routes in `server`
- Netlify functions: `netlify/functions`
- Shared types and helpers: `shared`
- Database setup: `database-setup.sql`

## Quick start

1. Copy environment template:

```bash
cd Relationship-Management-Tool
cp .env.example .env
```

2. Install dependencies and run the app (separate services):

```bash
# install in root (if needed)
npm install

# client
cd client
npm install
npm run dev

# server
cd ../server
npm install
npm run dev
```

If you use Netlify for functions, follow `netlify` folder instructions or use `netlify dev` from the project root.

## Database

Use the provided `database-setup.sql` to create the database schema. If the app uses Supabase (see `client/lib/supabase.ts`), configure the Supabase URL and key in `.env`.

## Project structure (high level)

- `client/` — Vite + React UI. Key files:
  - `client/App.tsx`, `client/main.tsx`
  - `client/components/*` — UI + feature components
  - `client/lib/supabase.ts` — Supabase helper
- `server/` — API server (routes and server entry)
- `netlify/` — serverless functions for Netlify
- `shared/` — shared types and helpers used by client/server
- `database-setup.sql` — SQL to initialise DB
- `AGENTS.md`, `DEPLOYMENT.md` — additional docs

## Scripts

Check `package.json` files in the root, `client`, and `server` for available scripts (install/build/dev/test).

## Deployment

See `DEPLOYMENT.md` for deployment notes. The repo includes `netlify.toml` and `vercel.json` for common hosts.

## Useful files

- `AGENTS.md` — architecture/agents notes
- `components.json` — UI component metadata
- `database-setup.sql` — DB schema and seed

## Contributing

Please open issues or PRs. Keep changes focused and include small, testable commits.

## License

Add your license here (e.g. MIT) or include a `LICENSE` file.

---
Created to make onboarding and local development straightforward. If you want, I can expand sections with exact scripts and environment variables from `package.json` and `.env.example`.
