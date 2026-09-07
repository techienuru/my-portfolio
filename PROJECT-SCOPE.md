# Portfolio Website — Project Scope
*Stack: React + Tailwind CSS + Shadcn/UI + Firebase Analytics + Framer Motion*

---

## Overview
A highly differentiated personal portfolio website built with React, Tailwind CSS, and Shadcn/UI. Unlike typical developer portfolios that are static brochures, this is a **living, interactive product** — with a cinematic scroll storytelling experience, role-based content switching, a live automation demo, an AI-assisted interactive resume, project case study pages, and a private dashboard for full content management. Data is stored in a local JSON file with Firebase used immediately for analytics, and full Firebase Firestore migration planned post-v1.

---

## Problem
Most developer portfolios fail on three levels:

1. **Static and outdated** — updating a project, certification, or work experience requires going into the codebase, editing files manually, and redeploying. For someone actively job hunting, this is a critical bottleneck.

2. **Generic and forgettable** — the typical hero → about → projects → contact structure tells recruiters nothing about who you are as a person, how you think, or what makes you different from the 200 other developers who applied.

3. **One-size-fits-all** — a frontend recruiter and an automation client land on the same page and see the same content, even though what matters to each of them is completely different. Most portfolios make no attempt to speak to different audiences.

---

## Solution
A dynamic, story-driven portfolio that:
- Tells your journey cinematically as visitors scroll — not just lists facts
- Switches content intelligently based on whether the visitor cares about frontend or automation work
- Lets visitors experience your automation skills live — not just read about them
- Gives recruiters a filterable, interactive resume that restructures itself around their role
- Showcases projects as full case studies with depth and results
- Tracks exactly who visits, what they look at, and how long they stay
- Is fully managed through a private dashboard — no code changes ever needed after launch

---

## Unique Features

### 1. Live Automation Demo
A dedicated interactive section where visitors can trigger a real automation workflow live on the portfolio. The visitor enters their name and email, clicks a button, and a Make.com or n8n workflow fires in real time — sending them a personalized welcome email from Ibrahim. A status indicator shows the workflow running and confirms when the email has been sent. This transforms "I build automations" from a claim into a demonstration.

**What makes it unique:** No other developer portfolio in Nigeria — or most of the world — lets a recruiter trigger a live automation from the portfolio itself.

---

### 2. Interactive Resume
A dedicated resume section that restructures itself based on the visitor's role interest. Three filter buttons — **Frontend**, **Automation**, **Fullstack** — dynamically show and hide relevant experience entries, projects, skills, and certifications. A recruiter hiring for a frontend role sees only frontend-relevant content. An automation client sees only automation work. Everything animates smoothly between states.

**What makes it unique:** It does what Teal HQ does for job applications — but live, in real time, for every visitor, automatically.

---

### 3. Project Case Study Pages
Every project gets its own dedicated route and full case study page — not just a card with a GitHub link. Each case study tells the complete story:
- **Overview** — what the project is in one paragraph
- **Problem** — what was broken or missing before it existed
- **Solution** — what was built and why those decisions were made
- **Tech Stack** — tools used with brief reasoning
- **Results** — metrics and outcomes
- **Screenshots** — visual walkthrough of the product
- **Links** — live URL and GitHub

**What makes it unique:** Technical hiring managers and clients want depth. A case study page signals a product thinker, not just a code writer.

---

### 4. Visitor Analytics Dashboard
Firebase is integrated immediately — not waiting for post-v1 — specifically to power a visitor analytics section inside the private dashboard. Tracks:
- Total portfolio visits (daily, weekly, all-time)
- Which sections visitors scroll to
- Which projects get the most clicks
- Which links (GitHub, Live URL, CV download) get clicked
- Referrer source (LinkedIn, direct, job board)

This gives real data on what's working — which projects attract attention, which CV version is driving traffic, and how long visitors are staying.

**What makes it unique:** Most developers have no idea if anyone is even looking at their portfolio. This turns it into a feedback loop.

---

### 5. "Hire Me" Mode Toggle
A persistent toggle — visible in the navigation — that switches the entire portfolio between two targeted experiences:

| | Frontend Mode | Automation Mode |
|---|---|---|
| Hero title | Frontend Developer | AI Automation Engineer |
| Hero tagline | Frontend-focused | Automation-focused |
| Featured projects | Frontend projects | Automation projects |
| Skills highlighted | React, JS, Tailwind | Make, n8n, Zapier, Airtable |
| About paragraph | Frontend angle | Automation angle |

The toggle state is saved in localStorage so it persists across page refreshes. Both modes are fully managed from the dashboard.

**What makes it unique:** One portfolio, two targeted experiences — without maintaining two separate websites.

---

## Sections — Public UI

### 1. Hero
- Full name, current job title (switches with Hire Me mode)
- One-line personal tagline (switches with Hire Me mode)
- CTA buttons: View Projects, Try Live Demo, Download CV
- Social links: GitHub, LinkedIn, Twitter/X
- Hire Me mode toggle (Frontend | Automation)
- Light/dark mode toggle
- Animated entrance using Framer Motion

### 2. About
- Profile photo
- About me paragraph (two versions — one per Hire Me mode)
- Key highlights: current role, tools, open to work status
- Fun fact: "My family has never visited a phone repair shop"

### 3. Tech Journey — Cinematic Scroll Timeline
- Full-screen cinematic scroll experience built with Framer Motion
- As the visitor scrolls, each milestone animates into view like a story unfolding
- Each milestone includes: year, title, short story description, type tag
- Milestone types: education, job, project, achievement, certification
- Example milestones:
  - "Computer Science was chosen for me — not by me" (2020)
  - "Two years of lectures without direction" (2020–2022)
  - "IT placement. First line of working code. Everything changed." (2022)
  - "Built my first full-stack app" (2023)
  - "Placed 3rd — Nasarawa State Virtual Hackathon" (2024)
  - "Joined 3MTT Cohort 3" (2025)
  - "Shipped 4 automation systems" (2025)
  - "Interning at Dotmac Technology" (2026)

### 4. Live Automation Demo
- Visitor enters name and email
- Clicks "Trigger Demo" button
- Real Make.com/n8n workflow fires
- Status indicator: Idle → Running → Success/Failed
- Visitor receives a personalized welcome email
- Short explanation of what just happened under the hood

### 5. Interactive Resume
- Role filter buttons: Frontend | Automation | Fullstack
- Smooth animated content switch per filter
- Shows: relevant experience, projects, skills, certifications
- Download CV button (downloads the version matching the active filter)

### 6. Experience
- Company name, role, type, duration, location
- Summary paragraph
- Metric-driven bullet point highlights
- Expandable/collapsible per entry

### 7. Projects (Grid + Case Studies)
- Filterable grid: All | Frontend | Automation | Fullstack
- Each card: thumbnail, name, short description, tech tags, links
- Featured projects shown prominently
- Each project links to its own full case study page

### 8. Skills
- Grouped by category: Languages, Frameworks, Databases, Automation Tools, Tools & Concepts
- Each skill shows name and proficiency level
- Switches highlighted skills based on Hire Me mode

### 9. Certifications
- Certificate name, issuing body, date
- Optional image or external link

### 10. Contact
- Contact form: name, email, message
- Direct email link
- Social links
- Optional: trigger a small automation on form submit (notify via Telegram/Slack)

---

## Dashboard (Private — Auth Protected)

### Authentication
- Username and password login
- Password stored hashed (bcrypt)
- Session persists via localStorage token until manual logout
- Unauthenticated users redirected to login

### Dashboard Home
- Quick stats: visits today, total projects, skills count, certifications, experience entries, journey milestones
- Recent visitor activity feed (from Firebase)
- Quick action buttons: Add Project, Add Milestone, Add Experience

### Analytics Section
- Total visits: daily, weekly, all-time chart (Firebase data)
- Top sections visited
- Top projects clicked
- Top links clicked (GitHub, live URL, CV)
- Referrer breakdown

### Manage Hire Me Modes
- Edit hero title, tagline, about paragraph for Frontend mode
- Edit hero title, tagline, about paragraph for Automation mode
- Set featured projects per mode
- Set highlighted skills per mode

### Manage Hero
- Edit name, titles, tagline
- Upload CV file
- Update social links

### Manage About
- Edit about paragraphs (both modes)
- Upload/change profile photo
- Edit key highlights

### Manage Tech Journey
- Add, edit, delete timeline milestones
- Set milestone type and year
- Write milestone story description
- Reorder milestones

### Manage Live Demo
- Configure which automation workflow URL to call
- Edit the demo section headline and description
- Toggle demo section on/off

### Manage Experience
- Add, edit, delete work experience entries
- Add/remove bullet point highlights
- Set employment type and dates

### Manage Projects
- Add, edit, delete projects
- Upload project thumbnail
- Toggle featured status per Hire Me mode
- Add/remove tech stack tags
- Set live URL and GitHub link
- Write full case study content per project (Overview, Problem, Solution, Tech Stack, Results, Screenshots, Links)

### Manage Skills
- Add, edit, delete skills
- Assign to category
- Set proficiency level
- Tag skills to Hire Me mode (frontend, automation, both)

### Manage Certifications
- Add, edit, delete certifications
- Upload certificate image or add external link
- Set issuing body and date

---

## Features Summary

### Public UI
- Fully responsive — mobile, tablet, desktop
- Light and dark mode (preference saved in localStorage)
- Cinematic scroll storytelling for Tech Journey section
- Hire Me mode toggle — switches entire portfolio between Frontend and Automation experience
- Live automation demo — visitor triggers a real Make.com/n8n workflow
- Interactive resume — role-based filter restructures content dynamically
- Project case study pages — full story per project with own route
- Project grid with tag filtering
- Featured projects highlight reel
- Smooth Framer Motion animations throughout
- Downloadable CV (version matches active Hire Me mode)
- Working contact form

### Dashboard
- Protected by username/password authentication (hashed)
- Full CRUD for all sections
- Analytics powered by Firebase (visits, clicks, referrers)
- Hire Me mode content management
- Live demo configuration
- Case study content editor per project
- Image upload for profile photo, project thumbnails, certificates
- Live preview link to public portfolio

---

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | React (Vite) |
| Styling | Tailwind CSS |
| UI Components | Shadcn/UI |
| Routing | React Router v6 |
| State Management | React Context API |
| Animations | Framer Motion |
| Icons | Lucide React |
| Data Layer | JSON file (local) |
| Analytics | Firebase (immediate) |
| Authentication | Username/password (hashed, stored in JSON) |
| Live Demo | Make.com or n8n webhook |
| Future DB | Firebase Firestore (full migration post-v1) |

---

## Folder Structure

```
src/
├── assets/
├── components/
│   ├── ui/                  # Shadcn components
│   ├── public/              # Public UI section components
│   │   ├── Hero.jsx
│   │   ├── About.jsx
│   │   ├── TechJourney.jsx
│   │   ├── LiveDemo.jsx
│   │   ├── InteractiveResume.jsx
│   │   ├── Experience.jsx
│   │   ├── Projects.jsx
│   │   ├── Skills.jsx
│   │   ├── Certifications.jsx
│   │   └── Contact.jsx
│   └── dashboard/           # Dashboard section components
│       ├── Analytics.jsx
│       ├── ManageHireMe.jsx
│       ├── ManageProjects.jsx
│       ├── ManageExperience.jsx
│       ├── ManageSkills.jsx
│       ├── ManageJourney.jsx
│       ├── ManageCertifications.jsx
│       └── ManageLiveDemo.jsx
├── context/
│   ├── AuthContext.jsx
│   └── HireMeContext.jsx
├── data/
│   └── portfolio.json       # All content lives here
├── firebase/
│   └── analytics.js         # Firebase analytics config
├── pages/
│   ├── Home.jsx
│   ├── Login.jsx
│   ├── Dashboard.jsx
│   └── CaseStudy.jsx        # Dynamic route per project
├── routes/
│   └── ProtectedRoute.jsx
└── App.jsx
```

---

## Build Phases

### Phase 1 — Foundation
- Project setup: Vite + React + Tailwind + Shadcn
- Routing setup with React Router v6
- JSON data layer structure
- Auth system (login, protected routes, session)
- Firebase analytics integration
- Light/dark mode

### Phase 2 — Public UI
- Hero section with Hire Me toggle
- About section
- Tech Journey cinematic scroll
- Experience section
- Skills section
- Certifications section
- Contact form

### Phase 3 — Unique Features
- Live Automation Demo section
- Interactive Resume with role-based filter
- Projects grid with filtering
- Project case study pages (dynamic routes)
- Hire Me mode context wiring across all sections

### Phase 4 — Dashboard
- Dashboard home with analytics
- CRUD for all sections
- Hire Me mode content management
- Case study editor per project
- Live demo configuration panel

### Phase 5 — Polish & Launch
- Framer Motion animations throughout
- Full mobile responsiveness audit
- Performance optimization
- Deploy to Vercel

---

## Future Improvements (Post v1)
- Full Firebase Firestore migration (replace JSON)
- Google OAuth for dashboard login
- Blog/articles section
- Email notification on contact form submission
- AI chat widget — answers recruiter questions about Ibrahim from his CV
- Multi-language support (English + Hausa)

---

*Version: 2.0*
*Reviewed as: Senior Software Engineer (5+ years — Fintech, EdTech, SaaS, HealthTech, Portfolio products)*
*Stack: React + Tailwind CSS + Shadcn/UI + Firebase + Framer Motion*
*Data: JSON (Firebase Firestore migration planned post-v1)*