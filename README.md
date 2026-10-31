# Subscription Hub

A responsive subscription-management dashboard starter inspired by the supplied warm, minimalist reference. Built with Next.js App Router, React, TypeScript, Tailwind-ready structure, Lucide icons, and Supabase dependencies.

## Current implementation

- Responsive dashboard UI with warm neutral colors, rounded cards, and subscription list.
- Monthly spend calculated from active local demo records.
- Search subscriptions by service name.
- Add a subscription through a validated client-side form.
- Upcoming payments and reminder panels.
- Accessible labels for icon-only controls and mobile responsive layout.
- Supabase schema migration starter and environment template.

**Important:** The dashboard currently uses clearly illustrative in-memory demo records. Authentication, persistent CRUD, email detection, reminder delivery, company billing workflows, and production authorization still require implementation and configuration. Do not deploy this starter as a finished production billing system.

## Run locally

1. Install Node.js 20.9+.
2. Copy `.env.example` to `.env.local`.
3. Run `npm install`.
4. Run `npm run dev`.
5. Open `http://localhost:3000`.

The dashboard can render without Supabase credentials. Database features are not connected yet.

## Supabase setup

Create a Supabase project, set `NEXT_PUBLIC_SUPABASE_URL` and `NEXT_PUBLIC_SUPABASE_ANON_KEY` in `.env.local`, then apply migrations using the Supabase CLI or SQL editor. Review all RLS policies before adding application data.

## Planned production milestones

1. Supabase SSR auth, verified sessions, password reset, protected routes.
2. Personal subscription CRUD and owner-scoped RLS.
3. Reminder scheduling with idempotency and in-app notifications.
4. Business tenants, memberships, customer/product/plan records.
5. Quotes, invoices, payment ledger, audit trail and state transitions.
6. Gmail OAuth with minimum read-only scope and user-reviewed extraction.
7. Vitest, React Testing Library and Playwright coverage.

## Scripts

- `npm run dev` — local development
- `npm run build` — production build
- `npm run start` — serve production build
- `npm run lint` — ESLint
- `npm run typecheck` — TypeScript checks
