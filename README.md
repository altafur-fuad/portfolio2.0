# Altafur Rahman Fuad — Portfolio Website

Static single-page site (plain HTML/CSS/JS — no build step needed). Theme: dark green
"field ledger," consistent with the CrossMamba-Agri tracker.

## Files

```
portfolio/
├── index.html                # everything — layout, styles, and script are in this one file
├── assets/
│   ├── fuad-photo.jpeg                       # hero portrait
│   └── crossmamba-agri-thesis-proposal.pdf   # linked from the Research section
└── README.md
```

## Editing content

Everything lives in `index.html`. To change text, search for the section by its
`id` (`hero`, `about`, `education`, `research`, `projects`, `skills`, `contact`) and
edit the text directly — no build tools, no npm install, just save and refresh.

Common edits:
- **Tagline / bio** — inside `<section class="hero">` and `<section id="about">`
- **Projects** — each is a `<div class="proj-card">` block under `<section id="projects">`; copy/paste a block to add a new project
- **Contact info / social links** — `<section id="contact">`
- **Colors** — all defined once at the top of the `<style>` block under `:root { ... }` (e.g. `--accent-field`, `--accent-gold`)

## Running locally

No install needed — just open `index.html` in a browser. For live-reload while editing,
you can optionally run a simple local server:

```bash
cd portfolio
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deploy (GitHub + Vercel)

1. Push this folder to a new GitHub repo:
   ```bash
   cd portfolio
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/altafur-fuad/portfolio.git
   git push -u origin main
   ```
2. Go to [vercel.com](https://vercel.com), import the repo.
3. Framework preset: **Other** (it's static HTML — no build command, no output directory needed).
4. Deploy. Vercel will give you a live URL; add a custom domain later if you want.

## What's using placeholder/default content

- **Tagline** — used your draft as-is: *"Flutter developer & CS undergrad — building
  AI-powered agriculture research and full-stack mobile apps."* Change it in the hero
  section if you want something different.
- **About bio** — I wrote this from the info you gave me since you hadn't drafted one.
  Worth a read-through to make sure it sounds like you.
- **Location string** ("Chattogram, Bangladesh") — used your general location; update
  if you'd rather show the university's district (Chandanaish) or something else.

Everything else (education, thesis, projects, skills, contact, socials) is exactly
what you provided.
