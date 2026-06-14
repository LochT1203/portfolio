# Bob Thambeliyagoda — Portfolio Site

Personal engineering portfolio. Built with plain HTML/CSS — no frameworks, no build step, no dependencies.

Live at: `https://YOUR-USERNAME.github.io/portfolio`

---

## Deploy to GitHub Pages (5 minutes)

1. **Create a new repo** on GitHub — name it `portfolio` (or anything you like)
2. **Upload these files** by dragging the whole folder into the GitHub web UI, or via terminal:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/portfolio.git
   git push -u origin main
   ```
3. Go to your repo → **Settings → Pages**
4. Under *Source*, select **Deploy from a branch** → `main` → `/ (root)`
5. Hit **Save** — your site will be live in ~60 seconds

---

## File structure

```
portfolio/
├── index.html          ← the entire site (one file)
├── README.md           ← this file
├── images/             ← project photos go here
│   ├── cubesat.jpg
│   ├── axolotl.jpg
│   ├── puttpal.jpg
│   ├── voice-assistant.jpg
│   ├── print-farm.jpg
│   └── catastrophe-cam.jpg
└── assets/
    └── resume.pdf      ← your resume PDF goes here
```

---

## Checklist before going live

- [ ] Add your **email address** (two spots in the Contact section — search `YOUR@EMAIL.COM`)
- [ ] Add your **LinkedIn URL** (search `YOUR-HANDLE`)
- [ ] Add your **GitHub username** (search `YOUR-USERNAME`)
- [ ] Drop your **resume PDF** into `assets/resume.pdf`
- [ ] Add **project photos** into `images/` and swap the placeholder `<div class="project-img">` elements for `<img>` tags:
  ```html
  <!-- Before -->
  <div class="project-img">Add photo — 600×338px</div>

  <!-- After -->
  <img class="project-img" src="images/cubesat.jpg" alt="LASAGNA-E CubeSat payload" />
  ```
- [ ] Wire up the **contact form** with [Formspree](https://formspree.io) (free) — instructions are in the JS comments at the bottom of `index.html`
- [ ] Update the `<title>` and `og:` meta tags at the top of `index.html` if you want custom link previews

---

## Adding a project

1. Open `index.html` and find the `<!-- PROJECTS -->` section
2. Duplicate any `.project-card` block
3. Use `class="project-card featured"` to make it span the full width (good for your hero project)
4. Add your photo to `images/` and update the `src`

## Adding a blog post

1. Find the `<!-- BUILD LOG -->` section
2. Duplicate an `<a class="blog-row">` block
3. Add it at the **top** of `.blog-list` (newest first)
4. Set `href` to your post URL, or `"#"` if it's not published yet

---

## Custom domain (optional)

If you have a domain (e.g. `bobtham.com`):
1. In GitHub Pages settings, enter your domain under *Custom domain*
2. Add a `CNAME` record at your DNS provider pointing to `YOUR-USERNAME.github.io`
3. GitHub will handle the SSL certificate automatically
