# sixtyleads

Outreach dashboard for the Sixty by DevMate email campaign (UK + USA).

A single static page (`index.html`) — no build step. Deploy it on any static host (Vercel, Netlify, GitHub Pages) or open it locally.

- Data lives in Supabase (`sixty_leads`, `sixty_email_events`, `sixty_campaign_runs`).
- The page only uses the Supabase **publishable** key. Tables are not readable with it: every request goes through `dash_*` database functions that require a login session.
- Login is checked server-side (bcrypt hash in `dashboard_users`); sessions last 7 days.

Features: overview KPIs and daily chart, pipeline, results by country and industry, campaign runs, searchable leads with details and email history, status / notes editing, CSV import (Apollo, Clay, Sales Navigator exports) and CSV export.
