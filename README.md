# smart-waste-energy-management-
# Eco AI — Smart Waste & Energy Management

Eco AI is a web app that helps people sort waste correctly and see the energy
their recycling helps recover. It opens with a marketing landing page, then
leads into a monitoring dashboard for energy and waste performance.

## Pages

| Page | URL | What it does |
| --- | --- | --- |
| Landing page | `/` | Hero, feature list, community impact figures, how it works, benefits by audience, FAQ |
| Sign in | `/login` | Email and password sign-in, plus a Google button |
| Create account | `/signup` | Registration with name, role (Citizen, Recycling center, Municipality), email and password |
| Dashboard | `/dashboard` | Dark monitoring view: energy flow, waste streams, bin levels, alerts, sustainability score |

## Features

- **AI classification** — photograph any item and get its waste category
- **Recycling guidance** — disposal steps and the nearest accepting center
- **Energy estimation** — the energy that could be recovered from your waste
- **Smart collection** — pickup scheduling and efficient city routes
- **Energy flow chart** — grid consumption versus solar generation across the day
- **Waste breakdown** — weekly totals by stream (recycling, organic, general)
- **Smart bin levels** — fill percentage and pickup status, with overdue bins flagged
- **Alerts feed** — notifications for high usage and full bins
- **Sustainability score** — an at-a-glance performance ring

## Tech Stack

- [TanStack Start](https://tanstack.com/start) (React 19, Vite 7)
- TypeScript
- Tailwind CSS v4 (design tokens in `src/styles.css`)
- shadcn/ui components
- Recharts for charts
- Lucide icons

## Getting Started

```sh
npm install
npm run dev
```

Open http://localhost:8080 to view the site.

## Scripts

| Command | Description |
| --- | --- |
| `npm run dev` | Start the dev server |
| `npm run build` | Production build |
| `npm run preview` | Preview the production build |
| `npm run test` | Run tests |
| `npm run lint` | Lint the codebase |

## Project Structure

```text
src/
  assets/          images used by the app (hero illustration)
  components/      shared pieces (site header/footer, auth card shell, ui/)
  routes/          one file per page: index, login, signup, dashboard
  styles.css       colour tokens, dark dashboard scope, helper styles
  router.tsx       router setup
```

Routing is file-based: a file in `src/routes/` becomes a page, and
`routeTree.gen.ts` is generated automatically — never edit it by hand.

## Design Notes

- The site uses a light mint-and-forest theme defined by CSS variables.
- The dashboard keeps a dark console look inside a `.theme-eco-dark` scope, so
  both looks share one set of tokens.
- Fonts: Plus Jakarta Sans for headings, DM Sans for body text.

## Current Status

- All figures shown — impact totals, bin levels, alerts, charts — are sample
  data for demonstration.
- Sign-in and sign-up run in demo mode: any details open the dashboard, and no
  accounts are stored yet. Real accounts and saved data are the next step.
