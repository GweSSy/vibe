# Our Team — Company Team Page

A finished, ready-to-publish static website that shows **photos and descriptions of 5 people** from your company.
No frameworks, no build step — plain HTML + CSS. You can edit everything directly on GitHub in the web browser.

📸 Placeholder photos are included so the site works immediately; replace them with real ones whenever you like.

---

## File structure

```
.
├── index.html                  ← EDIT THIS FILE (photos + descriptions)
├── css/
│   └── style.css               ← look & feel (usually no need to edit)
├── images/
│   ├── photo-1.jpg             ← Person 1's photo (replace placeholder)
│   ├── photo-2.jpg             ← Person 2's photo
│   ├── photo-3.jpg             ← Person 3's photo
│   ├── photo-4.jpg             ← Person 4's photo
│   └── photo-5.jpg             ← Person 5's photo
├── .github/workflows/deploy.yml← auto-publishes the site to GitHub Pages
├── .nojekyll                   ← required for GitHub Pages
├── .gitignore
├── LICENSE                     ← MIT
└── README.md                   ← this file
```

---

## How to edit content on GitHub (no tools needed)

1. Open this repository on **github.com**.
2. To change text: open `index.html`, click the **pencil icon ✏️ (Edit this file)**, change the text, then
   **"Commit changes"**. Every editable spot is marked with comments:

   ```html
   <!-- EDIT: ... -->
   your content here
   <!-- /EDIT -->
   ```

   In each person card you can change:
   - `<h2 class="name">` → person's name
   - `<p class="role">` → job title
   - `<p class="description">` → a few sentences about the person
   - `<img src="...">` → path to the photo

   Also search for `Company Name` (header, footer, page title) and replace it.

3. To replace a photo: click into the `images/` folder → **Add file → Upload files** →
   upload e.g. `jane.jpg` → then update the `<img src="images/jane.jpg">` line in `index.html`.

   > Tip: square photos look best, but any aspect ratio works — CSS crops them automatically (`object-fit: cover`).

4. After each commit to the `main` branch, the site re-publishes automatically (see below).

---

## Publishing to GitHub Pages (automatic)

This repo ships with a ready-made GitHub Actions workflow (`.github/workflows/deploy.yml`).

1. Create a repository on GitHub and push this project to its **`main`** branch:

   ```bash
   git init                      # skip if already a git repo
   git add .
   git commit -m "Team page"
   git branch -M main
   git remote add origin https://github.com/<your-user>/<your-repo>.git
   git push -u origin main
   ```

2. On GitHub, open **Settings → Pages → Build and deployment → Source** and select **GitHub Actions**.
3. That's it. After every push to `main`, your site goes live at
   `https://<your-user>.github.io/<your-repo>/`.

---

## Previewing locally

Just open `index.html` in a browser, or run a local server:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

---

## License

Released under the [MIT License](LICENSE) — use it however you like.
