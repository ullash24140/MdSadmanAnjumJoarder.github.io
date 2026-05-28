# Md. Sadman Anjum Joarder — Personal Portfolio

A modern, fully responsive personal portfolio website for **Md. Sadman Anjum Joarder**, Mechanical Engineer & Researcher.

Built as a single-file static site (no build tools required) and ready to be hosted **for free** on GitHub Pages.

---

## What's inside

```
portfolio/
├── index.html                 ← the whole site (HTML + CSS + JS, ~1 file)
├── 404.html                   ← friendly 404 page
├── .nojekyll                  ← tells GitHub Pages to serve files as-is
├── README.md                  ← this file
└── assets/
    ├── profile.jpg            ← (you add this — see step 2 below)
    └── profile-placeholder.svg
```

Features:
- Dark / light theme toggle (auto-detects system preference)
- Animated hero with conic-gradient avatar ring
- Sticky glassmorphism navigation
- Publication filter tabs (Published / Under Review / All)
- Scroll-reveal animations powered by IntersectionObserver
- Fully responsive — works on phone, tablet and desktop
- SEO + OpenGraph meta tags
- Zero build step, zero dependencies (only Google Fonts + FontAwesome CDN)

---

## How to publish on GitHub Pages (free, ~5 minutes)

### Step 1 — Create the repository

1. Go to **https://github.com/new** while logged in.
2. **Repository name:** for a clean URL like `https://<your-username>.github.io`, name it exactly:
   ```
   <your-github-username>.github.io
   ```
   e.g. if your username is `sadmananjum`, name the repo `sadmananjum.github.io`.
   (If you use any other name, the site will live at `https://<username>.github.io/<repo-name>/`.)
3. Make the repository **Public**.
4. Do **not** initialize with a README — we already have one.
5. Click **Create repository**.

### Step 2 — Add your profile picture

Save the profile photo from the chat as `profile.jpg` inside the `assets/` folder:

```
portfolio/assets/profile.jpg
```

The site automatically falls back to elegant "SA" initials if the image is missing, but having the real photo makes it look complete.

### Step 3 — Upload the files

**Option A — drag and drop (easiest):**
1. Open your new repo on GitHub.
2. Click **Add file → Upload files**.
3. Drag the entire **contents** of the `portfolio/` folder (not the folder itself) onto the page — `index.html`, `404.html`, `.nojekyll`, `README.md`, and the `assets/` folder.
4. Scroll down and click **Commit changes**.

**Option B — git command line:**
```bash
cd portfolio
git init
git add .
git commit -m "Initial portfolio"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-username>.github.io.git
git push -u origin main
```

### Step 4 — Enable GitHub Pages

1. Open your repo → **Settings** → **Pages** (in the left sidebar).
2. Under **Source**, choose **Deploy from a branch**.
3. Branch: **main**, folder: **/ (root)**. Click **Save**.
4. Wait 30–90 seconds. GitHub will show a green box: *"Your site is live at https://<your-username>.github.io/"*.

### Step 5 — Share the link

Your portfolio is now publicly available at:

```
https://<your-github-username>.github.io
```

Share it on:
- **LinkedIn → Edit Intro → Website** (`https://<your-username>.github.io`)
- Your **CV header**
- Your **email signature**
- **Google Scholar profile** (Homepage field)
- **ResearchGate** and **ORCID** profile links

---

## Customising the site later

Everything is in **one HTML file**, so editing is straightforward. Open `index.html` and look for these landmarks:

| What to change | Where to look |
|---|---|
| Page title / SEO description | `<title>` and `<meta name="description">` at top |
| Hero name / tagline | inside `<section class="hero">` |
| Quick facts (right card) | inside `class="facts-card"` |
| Research keyword chips | inside `class="chips"` |
| Research focus cards | inside `<section id="research">` |
| Publications | each `<article class="pub">` |
| Experience timeline | inside `class="timeline"` |
| Education cards | inside `<section id="education">` |
| Contact email / phone / LinkedIn | inside `class="contact-row"` |

To add a new publication, copy any existing `<article class="pub">` block and change the contents.

### Adding a Google Scholar / ORCID link
In the hero section there's a `class="hero-socials"` row. Replace the placeholder hrefs (`https://scholar.google.com/`, `https://orcid.org/`, `https://www.researchgate.net/`) with your actual profile URLs once you have them.

### Optional: custom domain
If you ever buy a domain (e.g. `sadmanjoarder.com`):
1. Add a file called `CNAME` (no extension) to the repo containing only your domain name.
2. Point an A record from your domain registrar to GitHub Pages IPs (185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153).
3. In **Settings → Pages → Custom domain**, enter your domain and enable **Enforce HTTPS**.

---

## Local preview before publishing

Just double-click `index.html` — it opens in any browser, no server needed.

For a slightly nicer preview with hot reload:
```bash
cd portfolio
python3 -m http.server 8080
# open http://localhost:8080
```

---

## Credit

Designed and built for **Md. Sadman Anjum Joarder**.
Fonts: Inter & Playfair Display (Google Fonts). Icons: FontAwesome 6 (CDN).
