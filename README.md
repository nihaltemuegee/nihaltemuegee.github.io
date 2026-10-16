# nihal-temuge-website

Personal website for Nihal Temüge — a single-page site built with plain HTML/CSS
(no build step, no dependencies), based on her CV. Meant to be hosted for free on
GitHub Pages at a URL that's easy to find by searching her name.

## Files

- `index.html` — Home page (landing page with photo, intro, and links to every section)
- `about.html` — About + skills
- `experience.html` — Work experience
- `education.html` — Education
- `projects.html` — Research & projects
- `publications.html` — Publications
- `contact.html` — Contact links
- `style.css` — all styling, shared by every page (light/dark mode aware)
- `favicon.svg` — browser-tab icon (a simple "NT" monogram)
- `assets/` — put a photo here (e.g. `assets/photo.jpg`) and swap it into the `<!-- PHOTO -->` comment in `index.html`'s hero section

## Preview it locally

No install needed — just serve the folder and open it in a browser:

```bash
cd ~/Desktop/nihal-temuge-website
python3 -m http.server 8000
```

Then open http://localhost:8000 in your browser. Press `Ctrl+C` in the terminal to stop it.

## Publish it for free on GitHub Pages

To get a URL like `https://nihaltemuegee.github.io/` that works well when someone
searches your name, GitHub has a special rule: if a repo is named exactly
`<your-username>.github.io`, it's served at the root of that URL automatically.
Your GitHub username is `nihaltemuegee`, so the repo must be named
`nihaltemuegee.github.io` exactly.

1. Go to https://github.com/new in your browser (while signed in as `nihaltemuegee`).
2. Repository name: `nihaltemuegee.github.io` — Public — don't initialize with a README (you already have one here).
3. Click "Create repository".
4. Back in the terminal, push this folder to it:

```bash
cd ~/Desktop/nihal-temuge-website
git init
git add .
git commit -m "Initial personal website"
git branch -M main
git remote add origin https://github.com/nihaltemuegee/nihaltemuegee.github.io.git
git push -u origin main
```

5. Wait 1–2 minutes, then visit https://nihaltemuegee.github.io/ — it should be live.
6. GitHub Pages is usually already on for a `<username>.github.io` repo. If the site
   doesn't load, check **Settings → Pages** in the repo and make sure "Source" is set
   to deploy from the `main` branch.

### Getting it to show up when someone googles your name

Being public on `nihaltemuegee.github.io` is most of it — Google crawls GitHub Pages
sites on its own, usually within days to a couple of weeks. To speed it up:

- Submit the URL at https://search.google.com/search-console (add the property, verify
  via the HTML-tag method, then use "Request Indexing" on the URL).
- Link to the site from somewhere Google already indexes you — e.g. add it to your
  LinkedIn profile's "Contact info" / featured links, and to your GitHub profile
  ("Edit profile" → Website).

## Updating the content later

Everything is in `index.html` — education, experience, skills, publications, and
contact links. Edit the text directly, then:

```bash
cd ~/Desktop/nihal-temuge-website
git add .
git commit -m "Update content"
git push
```

Changes usually appear on the live site within a minute or two.

## Notes

- Your phone number and your references' personal contact details (from the CV) were
  deliberately left off this public site — only your email, LinkedIn, and GitHub are
  shown. Add your phone back in `index.html` yourself if you want it public.
- The LinkedIn link uses the handle from your most recent CV
  (`linkedin.com/in/nihal-temuege`) — LinkedIn profiles can't be checked without
  logging in, so double-check that link resolves to your profile once the site is live.
