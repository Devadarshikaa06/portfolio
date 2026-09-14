# Devadarshikaa 

A personal portfolio site built with React, Vite, TypeScript, Tailwind CSS, and Framer Motion.

## Run it locally

```bash
npm install
npm run dev
```

Then open the local URL Vite prints (usually `http://localhost:5173`).

## Build for production

```bash
npm run build
```

Output goes to `dist/`. Preview the production build with:

```bash
npm run preview
```

## Where to edit things

Everything personal lives in **`src/data/profile.ts`** — you shouldn't need to touch component code to update content.

| What | Where |
|---|---|
| Name, role, headline, bio | `profile` object in `src/data/profile.ts` |
| GitHub / LinkedIn / email / resume link | `profile.links` in `src/data/profile.ts` |
| Projects (SentinelAI, StudyMate AI, WeFix, Pet Care Tracker) | `projects` array in `src/data/profile.ts` |
| Skills / technology constellation | `skillCategories` in `src/data/profile.ts` |
| Research interests | `researchInterests` in `src/data/profile.ts` |
| Journey / timeline | `journey` array in `src/data/profile.ts` |
| Site colors, fonts, grid/grain effects | `src/index.css` (`@theme` block) |
| Resume file | drop a PDF into `public/` and point `profile.links.resume` at it (e.g. `/resume.pdf`) |
| Favicon | `public/favicon.svg` |

Anything wrapped in `[Editable: ...]` inside `profile.ts` is a placeholder — no facts, numbers, or achievements were invented. Fill those in with your real details, or remove the surrounding section if it doesn't apply.

## Project structure

```
src/
  components/     Loader, Nav, ProjectModal, LabBackground, Footer, brand icons
  sections/       Hero, About, Projects, Skills, Research, Journey, Contact
  data/           profile.ts — all editable content
  hooks/          useActiveSection, useReducedMotion
  App.tsx
  main.tsx
  index.css       design tokens + global styles
```

## Notes

- No backend, no API keys, no paid services required.
- The contact section uses a `mailto:` link — there's no fake contact form.
- Motion respects `prefers-reduced-motion`.
- Built and verified with `npm run build` (TypeScript project references + Vite build, zero errors).
