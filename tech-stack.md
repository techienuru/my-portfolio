# Portfolio Technology Stack

This stack is chosen for a fast, polished, responsive portfolio that can grow into the planned dashboard later.

## Public Portfolio (Now)

| Area | Choice | Why it fits this project |
|---|---|---|
| App framework | React + Vite | Fast development and simple deployment to Vercel. |
| Language | JavaScript (ES6+) | Matches Ibrahim's current frontend strengths and keeps the first version approachable. |
| Styling | Tailwind CSS | Makes responsive layouts and dark mode quick to build consistently. |
| Reusable UI | shadcn/ui | Provides accessible building blocks for buttons, forms, tabs, dialogs, and filters. |
| Routing | React Router | Supports the home page and a dedicated page for each project case study. |
| Animation | Framer Motion | Powers the journey timeline, smooth section reveals, and mode switching. |
| Icons | Lucide React | Clean, consistent icons for links, controls, and status messages. |
| Content source | Local JSON file | Keeps portfolio content in one editable place for version 1. |
| Browser storage | localStorage | Remembers the selected Hire Me mode and light/dark theme. |
| Analytics | Firebase Analytics | Tracks visits and important clicks without building a dashboard yet. |
| Forms | Native form validation + Formspree or Web3Forms | Lets the contact form work without building a backend. Choose one before implementation. |
| Deployment | Vercel | Straightforward hosting, preview links, and React routing support. |

## Live Automation Demo (Preview Only)

The first version will show the form, workflow steps, and a simulated success state. It will not collect or send visitor information.

When ready, connect it to one of these:

- n8n webhook, if you want full control and flexible workflows.
- Make webhook, if you prefer a faster no-code setup.

## Dashboard (Later)

Do not use a JSON file or browser-only login for a live admin dashboard. Those options are useful for a local prototype but are not secure after deployment.

| Area | Recommended choice | Purpose |
|---|---|---|
| Database | Firebase Firestore | Stores projects, profile content, and dashboard edits online. |
| Login | Firebase Authentication | Secures dashboard access. |
| Image storage | Firebase Storage | Stores profile photos, project screenshots, certificates, and CVs. |
| Server-side protection | Firebase Security Rules / Cloud Functions | Prevents visitors from changing private content. |

## Not Included in Version 1

- Private dashboard
- Real automation webhook or personalised email
- Image upload system
- Firestore content migration
- AI chat widget

