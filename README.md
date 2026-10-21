# Perpustakaan

An early React scaffold for a library application. The current interface is still the starter screen; library workflows are not implemented.

## Stack

React and Vite, with the Supabase client listed as a dependency. Tests use Vitest and Testing Library. Use Node.js 22.12 or newer (tested environment: Node.js 24).

## Development

```sh
npm ci
npm start
```

If adding Supabase integration, copy `.env.example` to `.env` and configure your own project. The current starter screen does not use these variables. Read public settings through `import.meta.env.VITE_SUPABASE_URL` and `import.meta.env.VITE_SUPABASE_ANON_KEY`. Never put a Supabase `service_role` key or other secret in a `VITE_*` variable: those variables are exposed to the browser. Old `REACT_APP_*` variables are no longer read; existing local environment files are not changed automatically.

Supabase public/anon keys require Row Level Security and least-privilege grants on the database. Keeping an anon key out of Git does not replace those controls.

## Checks

```sh
npm test
npm run build
```

Local environment files are ignored. See [SECURITY.md](SECURITY.md).

Production output is `dist/` (previously `build/` under Create React App). Configure static hosting to publish `dist/`. `npm start` now serves development on loopback port 5173. The starter screen and its existing link test are retained; `eject` is no longer applicable.
