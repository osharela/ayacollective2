# Aya Collective — Website

Static website for **Aya Collective, LLC** — strategy, creative eco-systems, and cultural experiences.

Six self-contained pages. No build step, no dependencies, no image folders: every page carries its own CSS, fonts, logos and patterns inline, so uploading the files is the whole deployment.

## Pages

| File | Page |
|---|---|
| `index.html` | Home |
| `services.html` | Services |
| `difference.html` | The Difference |
| `process.html` | How Aya Works (The Aya Approach) |
| `about.html` | About |
| `connect.html` | Contact / Connect |

All filenames are lowercase and must stay flat in the web root — `index.html` is the default document.

## Editing

- **Text:** open the relevant `.html` and edit the copy directly. Each page is a single file.
- **Colour / type / spacing:** the design tokens live in the `<style>` block at the top of each page (`:root { --sienna: ... }` etc.).
- Add or remove pages by creating an `.html` file and adding a link in the `nav` block that appears in every page.

## Deploying

### Option A — Porkbun static hosting (GitHub Connect)
1. Push this repo to GitHub.
2. Porkbun → Hosting → your `ayacollective.llc` plan → **Connect to GitHub** → pick this repo and the `main` branch.
3. Set the publish root to `/` (the repo root already holds the HTML files).
4. Deploy. Re-deploy after each push.

### Option B — Porkbun File Manager
Upload the six `.html` files flat into the web root, replacing the old ones.

### Option C — GitHub Pages
Settings → Pages → Source: `Deploy from a branch` → `main` / `/ (root)`. The included `CNAME` sets the custom domain to `ayacollective.llc`; point the domain's DNS at GitHub per their instructions.

## Notes

- Enable SSL/Let's Encrypt on the host and point both `ayacollective.llc` and `www.ayacollective.llc` at the same root.
- The contact form on `connect.html` uses `mailto:info@ayacollective.llc` — it opens the visitor's mail client. Swap for a form service (Formspree, Netlify Forms, etc.) if you want in-page submissions.
- Contact details used across the site: `info@ayacollective.llc` · 818 · 917 · 5807 · ayacollective.llc
