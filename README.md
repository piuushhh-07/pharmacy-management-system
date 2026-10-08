# MediCore — Pharmacy Management System

MediCore is a pharmacy management system built for small and medium medical
stores/pharmacies in India. It manages medicines, batches, expiry (FEFO),
billing/POS, customers, suppliers, purchases, reports, notifications, and
role-based access.

## Status

🚧 Early development — **Phase 1: Project foundation** is complete. No
functional UI or API exists yet; this phase only establishes the repository
layout, tooling, and conventions that later phases build on.

## Tech stack

- **Frontend:** HTML5, CSS3, vanilla JavaScript (no framework)
- **Backend:** Node.js, Express.js
- **Database:** PostgreSQL
- **API style:** REST, versioned under `/api/v1`
- **Charts:** Chart.js
- **Icons:** Lucide

## Project structure

```
pharmacy-management-system/
├── frontend/           # Static HTML/CSS/JS client
│   ├── pages/          # Secondary pages (inventory, sales, reports, ...)
│   ├── css/            # Stylesheets (design tokens, layout, components)
│   ├── js/             # Client-side modules (api, auth, dashboard, ...)
│   └── assets/
├── backend/
│   ├── src/
│   │   ├── config/
│   │   ├── controllers/
│   │   ├── middleware/
│   │   ├── models/
│   │   ├── routes/
│   │   ├── services/
│   │   └── utils/
│   ├── migrations/
│   ├── seeds/
│   └── tests/
├── README.md
├── .gitignore
└── SECURITY.md
```

All files currently in `frontend/` and `backend/src/` are placeholders —
each contains a single comment noting the phase that will implement it.

## Getting started (backend)

```bash
cd backend
cp .env.example .env     # fill in real DATABASE_URL and JWT_SECRET
npm install
npm run dev               # starts once Phase 8 adds src/server.js logic
```

The frontend is static; once pages have real content, open
`frontend/index.html` directly or serve `frontend/` with any static file
server.

## Roadmap

Development proceeds one phase at a time (see commit history): project
foundation → frontend design system → dashboard/inventory/expiry/customer/POS
UI → backend foundation → database schema → auth → inventory, expiry
(FEFO), sales, customer, supplier, purchase APIs → dashboard APIs → reports
→ notifications → user management → settings → testing → security audit →
production prep.

## Security

See [SECURITY.md](./SECURITY.md). Never commit `.env` files or real
secrets — use `.env.example` as the template.
