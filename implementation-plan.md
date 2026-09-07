# Public Portfolio Implementation Plan

## Goal

Build a responsive public portfolio for Ibrahim Nurudeen Shehu that gives equal weight to frontend development and AI automation work. The dashboard and real automation workflow are intentionally deferred.

## Phase 0 — Content and Design Decisions

1. Collect the profile photo, project screenshots, CV files, and social links.
2. Confirm which projects are featured in Frontend mode and Automation mode.
3. Confirm the public contact email and preferred contact-form service.
4. Choose the visual direction: colours, font style, and overall tone.
5. Review portfolio wording so titles, achievements, and metrics are accurate.

**Done when:** All required public content and basic visual choices are ready.

## Phase 1 — Project Foundation

1. Create the React and Vite project setup.
2. Add Tailwind CSS, shadcn/ui, React Router, Framer Motion, and Lucide icons.
3. Create the main folder structure for pages, reusable components, assets, and content.
4. Create one local JSON file for profile, projects, experience, skills, and certifications.
5. Add the home page and a route for individual case studies.
6. Add a simple not-found page.
7. Set up light and dark themes.

**Done when:** The site opens locally, routes work, and shared styling is in place.

## Phase 2 — Core Public Experience

1. Build the navigation with section links, theme control, and Hire Me mode control.
2. Build the hero section with clear calls to action and social links.
3. Build the About section with profile photo, key highlights, and family fun fact.
4. Make the Frontend and Automation modes change the hero title, tagline, about text, featured work, and highlighted skills.
5. Save the selected mode and theme on the visitor's device.
6. Build the Experience section with expandable achievement details.
7. Build the Skills and Certifications sections.
8. Build the responsive footer.

**Done when:** The home page clearly represents both career directions on mobile and desktop.

## Phase 3 — Story and Proof of Work

1. Build the Tech Journey timeline from the career milestones in `ABOUT-ME.md`.
2. Add subtle scroll-based motion to make the journey feel like a story.
3. Build the projects grid with All, Frontend, Automation, and Fullstack filters.
4. Create project cards with screenshots, short summaries, tools used, and links.
5. Build a reusable project case-study page layout.
6. Add case-study content for the highest-priority projects first.
7. Add working links only where live URLs and repositories are available.

**Done when:** Recruiters can quickly scan work or explore full project stories.

## Phase 4 — Interactive Features

1. Build the Interactive Resume section.
2. Add Frontend, Automation, and Fullstack resume filters.
3. Show the matching experience, projects, skills, and certifications for each filter.
4. Connect each filter to the correct downloadable CV file.
5. Build the Live Automation Demo as a safe visual preview.
6. Show clear preview states: ready, running, and demo complete.
7. Explain that no email is sent in this version.
8. Build and test the contact form using the chosen form service.

**Done when:** The interactive areas are clear, useful, and do not promise a real automation that is not connected yet.

## Phase 5 — Analytics, Quality, and Launch

1. Add Firebase Analytics.
2. Track page views, project clicks, CV downloads, social-link clicks, and mode selection.
3. Check every page on small mobile, tablet, laptop, and large desktop screens.
4. Check keyboard navigation, readable contrast, labels, and visible focus states.
5. Improve image sizes and loading speed.
6. Test every route, filter, link, download, and form submission.
7. Add a custom page title, description, social-sharing image, and favicon.
8. Deploy to Vercel and test the live site.

**Done when:** The public site is polished, accessible, measurable, and live.

## Later Phase — Private Dashboard

Only begin after the public portfolio is launched and the data is moved from local JSON to Firestore.

1. Set up secure Firebase login.
2. Create protected dashboard pages.
3. Add content editing for each public section.
4. Add image and CV upload support.
5. Add analytics summaries for visits and clicks.
6. Connect the real n8n or Make automation webhook with abuse protection.

## Suggested Build Order

Start with Phases 0–2. They establish the message, structure, and visual experience. Then complete projects and case studies before adding the resume, preview demo, analytics, and launch polish.

