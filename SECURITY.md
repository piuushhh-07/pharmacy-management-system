# Security Policy

MediCore is under active development. This document will grow alongside
the codebase; the items below are the baseline rules the project follows
from Phase 1 onward.

## Secrets

- Never commit `.env`, database credentials, JWT secrets, or API keys.
- `backend/.env.example` lists required variable **names** only.
- Real values live only in a local, git-ignored `backend/.env`.

## Planned protections (implemented in later phases)

- Password hashing with bcrypt
- JWT-based authentication with role-based authorization enforced on the
  backend (not just hidden in the UI)
- Parameterized SQL queries (no string-concatenated SQL)
- Input validation on both client and server
- Helmet for HTTP security headers
- CORS allow-list via `CORS_ORIGIN`
- Rate limiting on authentication endpoints
- Database transactions for any operation touching inventory/stock, so a
  failed sale or purchase rolls back cleanly

## Reporting a vulnerability

This is currently a private, pre-release project. If you find a security
issue, report it directly to the maintainer rather than opening a public
issue.
