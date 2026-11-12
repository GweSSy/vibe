# Our Team — Website Skeleton

A simple static website that shows **photos and descriptions of 5 people** from your company.
No frameworks, no build step — just open `index.html` in a browser.

## File structure

```
/workspace
├── index.html        ← EDIT THIS FILE (photos + descriptions)
├── css/
│   └── style.css     ← look & feel (usually no need to edit)
└── images/
    ├── photo-1.jpg   ← put Person 1's photo here (replace placeholder)
    ├── photo-2.jpg   ← put Person 2's photo here
    ├── photo-3.jpg   ← put Person 3's photo here
    ├── photo-4.jpg   ← put Person 4's photo here
    └── photo-5.jpg   ← put Person 5's photo here
```

## How to add your own content

Every editable spot in `index.html` is clearly marked with comments:

```html
<!-- EDIT: ... -->
your content here
<!-- /EDIT -->
```

### 1. Photos
Drop your real photos into the `images/` folder (e.g. `jane.jpg`) and update
the `<img src="...">` inside each card's `photo-slot`, e.g.:

```html
<img src="images/jane.jpg" alt="Photo of Jane Doe" />
```

Photos are automatically cropped to a square by CSS (`object-fit: cover`),
so any aspect ratio works — square originals look best.

### 2. Names, job titles and descriptions
Inside each card's `info-slot`, replace the text between the `EDIT` markers:

- `<h2 class="name">` → person's name
- `<p class="role">` → job title
- `<p class="description">` → a few sentences about the person

### 3. Company name
Search for `Company Name` in `index.html` (header and footer) and replace it.

## Previewing the site

Just open `index.html` in a browser, or run a local server:

```bash
cd /workspace
python3 -m http.server 8000
# then visit http://localhost:8000
```