# Perpustakaan

A React and Vite starting point for a library application. The current interface is still the starter screen.

**React · Vite · Vitest** · Early scaffold

## Current scope

The project contains the frontend scaffold and its starter-screen test. Library
catalogs, borrowing, returns and account workflows are **not implemented** yet.
The Supabase client is listed as a dependency but the starter screen does not use it.

## Run locally

Use **Node.js 22.12+**; CI uses Node.js 24.

```sh
git clone https://github.com/EGYYFZA/perpustakaan.git
cd perpustakaan
npm ci
npm start
```

Open **http://127.0.0.1:5173**.

```sh
npm test
npm run build
```

The production output directory is <code>dist/</code>.

## Adding backend integration

Use your own project settings from [.env.example](.env.example). Vite exposes
<code>VITE_*</code> variables to the browser: never put service-role keys or other
secrets in them. Database access still requires RLS and least-privilege grants.
Local environment files stay out of Git. Read [SECURITY.md](SECURITY.md).
