# Portfolio
# Surya Saran Teja — Portfolio

Personal portfolio of a full-stack software engineer, built with React, TypeScript, and Tailwind CSS. The site presents projects, experience, and skills through a single design idea: **the stack, cross-sectioned**.

**Live site:** [your-domain-or-vercel-url](https://your-domain-or-vercel-url)

![Portfolio screenshot](./docs/screenshot-home.png)

---

## About the design

Most portfolios say "full-stack" in a headline. This one shows it.

The signature element is a layered diagram with four horizontal bands — **Interface, API, Data, and Cloud** — styled like geological strata.

- **Hero:** on page load, a single request pulse travels down through the layers. Hovering a layer reveals the tools used at that level.
- **Projects:** every project carries a mini strata bar showing which layers it touched. Selecting a layer filters the project list.
- **Case studies:** each project page includes an architecture view built from the same strata system.

The same visual device works as navigation and information rather than decoration, so a recruiter sees end-to-end experience at a glance and an engineer sees exactly where the work happened.

### Design tokens

| Token | Hex | Role |
|---|---|---|
| Ink | `#14213D` | Text (light mode), background (dark mode) |
| Mist | `#EEF1F6` | Background (light mode) |
| Interface | `#7FA7D9` | Top stratum |
| API | `#4F7CAC` | Second stratum |
| Data | `#2E5A88` | Third stratum |
| Cloud | `#1B3A5C` | Bottom stratum |
| Signal | `#F2B134` | Request pulse, active filters, focus rings |

**Typography:** Schibsted Grotesk for headings and interface text, Newsreader for long-form case-study writing. Monospace appears only where it shows real code, such as API routes inside the strata diagram.

### UX principles

1. **The 30-second test.** Name, role, contact actions, and the strongest project are visible within one scroll on a laptop.
2. **Two paths.** Recruiters get a résumé link that is always in the header; engineers get detailed case studies.
3. **One motion moment.** The hero pulse runs once on load. Other motion responds only to user actions, and all motion respects `prefers-reduced-motion`.
4. **Plain, specific copy.** Sentence case and buttons that say exactly what they do.
5. **Accessible by default.** Responsive layouts, visible keyboard focus, and WCAG AA contrast in both themes.

---

## Features

- Interactive strata hero with a one-time load animation
- Project grid filterable by stack layer
- Case-study pages with problem, approach, architecture, challenges, and outcome
- Experience timeline
- Categorized skills section
- Contact form with validation and a downloadable résumé
- Light and dark themes that follow system preference, with a manual toggle
- Per-page titles, Open Graph previews, sitemap, and robots.txt
- Route-level code splitting and optimized images

---

## Tech stack

| Area | Tools |
|---|---|
| Framework | React 18, TypeScript, Vite |
| Styling | Tailwind CSS v4 |
| Routing | React Router |
| Motion | Framer Motion |
| SEO | react-helmet-async, static Open Graph tags |
| Forms | Formspree |
| Icons | lucide-react |
| Tooling | ESLint, Prettier (with Tailwind plugin) |
| Hosting | Vercel |

---

## Project structure

```
src/
├── components/   # Reusable UI: Header, Footer, StrataBar, ProjectCard
├── sections/     # Page sections: Hero, About, Projects, Experience, Skills, Contact
├── pages/        # Route-level pages: Home, ProjectDetail
├── data/         # Typed content: projects.ts, experience.ts, skills.ts
├── assets/       # Images and static media
├── App.tsx
└── main.tsx
public/
├── resume.pdf
├── og-image.png
├── robots.txt
└── sitemap.xml
```

All site content lives in `src/data/` as typed TypeScript files, so projects and experience can be updated without touching any UI code.

---

## Getting started

**Prerequisites:** Node.js 18 or later and npm.

```bash
# Clone the repository
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>

# Install dependencies
npm install

# Start the development server
npm run dev
```

The site runs at `http://localhost:5173`.

### Scripts

| Command | What it does |
|---|---|
| `npm run dev` | Starts the local development server |
| `npm run build` | Type-checks and builds for production |
| `npm run preview` | Serves the production build locally |
| `npm run lint` | Runs ESLint |

### Environment variables

Create a `.env` file in the project root:

```
VITE_FORMSPREE_ID=your_formspree_form_id
```

---

## Deployment

The site deploys automatically to Vercel on every push to `main`. A `vercel.json` rewrite sends all routes to `index.html`, so direct links to pages like `/projects/:slug` work correctly.

---

## Build log

This portfolio was built in 14 daily releases.

- [ ] Day 1 — Project setup and first deploy
- [ ] Day 2 — Layout, design tokens, and dark mode
- [ ] Day 3 — Strata hero
- [ ] Day 4 — About section
- [ ] Day 5 — Typed content data layer
- [ ] Day 6 — Projects grid with strata filter
- [ ] Day 7 — Routing and case-study pages
- [ ] Day 8 — Experience timeline
- [ ] Day 9 — Skills section
- [ ] Day 10 — Contact form and résumé download
- [ ] Day 11 — Motion and responsive polish
- [ ] Day 12 — SEO and Open Graph
- [ ] Day 13 — Performance and accessibility
- [ ] Day 14 — Launch v1.0

---

## Contact

**Surya Saran Teja D V** — Full-stack software engineer, Boston, MA

- Email: [suryasaranteja@gmail.com](mailto:suryasaranteja@gmail.com)
- LinkedIn: [linkedin.com/in/your-profile](https://linkedin.com/in/your-profile)
- GitHub: [github.com/your-username](https://github.com/your-username)

---

## License

The source code is available under the [MIT License](./LICENSE). Personal content — including text, photos, and résumé — is not covered by the license and may not be reused.
