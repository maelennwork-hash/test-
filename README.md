# SmallBiz CRM

Monorepo CRM app for small businesses.

## Structure

- `apps/api`: Express API (JWT auth, RBAC, Swagger docs)
- `apps/web`: Next.js web app (Tailwind + kanban pipeline)
- `packages/db`: Prisma schema + seed

## Local run

1) Start Postgres:

```bash
docker compose up -d postgres
```

2) Install:

```bash
npm install
```

3) Migrate + seed:

```bash
npm run db:migrate -w packages/db -- --name init
npm run db:seed
```

4) Run:

```bash
npm run dev
```

- Web: `http://localhost:3000`
- API: `http://localhost:4000`
- Swagger: `http://localhost:4000/docs`

Demo accounts:
- `admin@demo.com` / `Password123!`
- `user@demo.com` / `Password123!`

