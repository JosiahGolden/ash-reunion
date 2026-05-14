# Audi & Mary Ash Family Reunion Website

A single-page static website for the Ash Family Reunion — July 16–19 at Pine Hills Group Camp, Lincoln State Park, Indiana.

---

## Deploy in 3 Steps

### Option A — GitHub Pages (free)

1. **Create a GitHub repository**
   Go to [github.com/new](https://github.com/new), name it something like `ash-reunion`, make it **Public**, and click *Create repository*.

2. **Upload the files**
   Drag and drop all four files (`index.html`, `style.css`, `script.js`, `README.md`) into the repository using the GitHub web interface, or run:
   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/ash-reunion.git
   git push -u origin main
   ```

3. **Enable GitHub Pages**
   Go to the repository → **Settings** → **Pages** → under *Branch*, select `main` and click **Save**. Your site will be live at `https://YOUR-USERNAME.github.io/ash-reunion` within a minute or two.

---

### Option B — Netlify (free, even easier)

1. Go to [netlify.com](https://netlify.com) and sign up for a free account.
2. From your Netlify dashboard, drag the **entire project folder** onto the deploy area that says *"Drag and drop your site folder here."*
3. That's it — Netlify gives you a live URL instantly (e.g. `https://ash-reunion.netlify.app`). You can customize the subdomain name in the site settings.

---

## How to Edit Content

All content lives in `index.html`. Each section is clearly marked with a comment like:

```html
<!-- ═══════════════════════════════════════════════════════
     HERO SECTION
     Edit: headline, dates, location...
     ═══════════════════════════════════════════════════════ -->
```

Open `index.html` in any text editor (Notepad works, VS Code is better) and search for the section you want to update.

### Quick-edit cheat sheet

| What to change | Search for in index.html |
|---|---|
| Reunion name / title | `Audi &amp; Mary Ash` |
| Dates | `July 16` |
| Location | `Pine Hills` |
| Welcome text | `Come hungry. Come ready.` |
| Schedule events | `timeline-item` |
| RSVP email | `reunion@example.com` |
| Cabin booking link | `reserveamerica.com` |
| Footer text | `footer-copy` |

---

## Adding Real Photos to the Gallery

1. Put your image files in the same folder as `index.html` (e.g. `photo1.jpg`, `grandma-2019.jpg`)
2. In `index.html`, find a `<!-- PHOTO SLOT -->` comment inside the gallery section
3. Replace the entire `<div class="gallery-placeholder">...</div>` block with:
   ```html
   <img src="your-photo-filename.jpg" alt="Brief description of the photo">
   ```
4. Repeat for each slot. You can add more slots by copying a `<div class="gallery-item">` block.

**Example — before:**
```html
<div class="gallery-item">
  <div class="gallery-placeholder">
    ... camera icon svg ...
  </div>
</div>
```

**After:**
```html
<div class="gallery-item">
  <img src="family-cookout-2022.jpg" alt="Family cookout, summer 2022">
</div>
```

---

## File Structure

```
reunionSite/
├── index.html   ← All page content lives here
├── style.css    ← All visual styling
├── script.js    ← Mobile nav, tabs, FAQ, scroll animations
└── README.md    ← This file
```

No build tools, no frameworks, no dependencies beyond Google Fonts (loaded from CDN). Edit any file in a text editor and redeploy.
