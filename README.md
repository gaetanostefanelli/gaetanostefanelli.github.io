# academic-hugo-minimal

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Hugo](https://img.shields.io/badge/Hugo-Extended_v0.120+-blue.svg)](https://gohugo.io/)
[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/AndreaAndolfatto/academic-hugo-minimal)

A minimal, responsive Hugo theme for academic personal websites.

**Live demo:** [andreaandolfatto.com](https://andreaandolfatto.com)

---

## Features

- Clean, minimal design — no clutter, no JavaScript frameworks
- Fully responsive (mobile, tablet, desktop)
- Research papers section with card layout
- Teaching section
- Social links (email, Google Scholar, SSRN, LinkedIn)
- CV download button
- Optional Google Analytics
- Zero external dependencies (only [Inter](https://fonts.google.com/specimen/Inter) font from Google Fonts)
- ~800 lines of hand-written CSS

## Requirements

- [Hugo Extended](https://gohugo.io/installation/) v0.120 or later

## Quick Start

```bash
# 1. Clone the repo
git clone https://github.com/YOUR_USERNAME/academic-hugo-minimal.git
cd academic-hugo-minimal

# 2. Edit hugo.yaml with your information (see Customization below)

# 3. Add your photo
cp /path/to/your/photo.jpg static/images/avatar.jpg
# Then update layouts/index.html line 5: change avatar.svg → avatar.jpg
# (or keep as .jpg and update layouts/index.html line 5)

# 4. Add your CV
cp /path/to/your/CV.pdf static/files/CV.pdf

# 5. Preview locally
hugo serve

# 6. Build for deployment
hugo
```

## Customization

### 1. Your identity — `hugo.yaml`

```yaml
title: "Your Name"
params:
  authorName: "Your Name"
  institution: "Your University"
  description: "Ph.D. student in [Field] at [University]"
  bio: "I am a Ph.D. student in [Field] at [University]."
  bioKeywords:
    - "Asset Pricing"
    - "Machine Learning"
  email: "yourname@university.edu"
  googleScholarURL: "https://scholar.google.com/citations?user=XXXXXXXX"
  ssrnURL: "https://papers.ssrn.com/sol3/cf_dev/AbsByAuth.cfm?per_id=XXXXXXX"
  linkedinURL: "https://www.linkedin.com/in/your-handle/"
  cvFile: "/files/CV.pdf"
  googleAnalyticsID: "G-XXXXXXXXXX"  # leave empty to disable
```

### 2. Research papers — `content/research/_index.md`

Edit the HTML directly. Each paper uses a `.paper-card` div:

```html
<div class="paper-card">
  <h3>Your Paper Title</h3>
  <p class="paper-meta">with <a href="#">Coauthor</a> · [<a href="#">SSRN</a>]</p>
  <p><span class="paper-label">Abstract:</span> Your abstract here.</p>
  <p><span class="paper-label">Presentations:</span> Conference A, Conference B</p>
</div>
```

### 3. Teaching — `content/teaching/_index.md`

Edit the markdown list directly.

### 4. Contact — `content/contact/_index.md`

Replace email and office address.

### 5. Photo — `static/images/`

Replace `avatar.svg` with your own photo. To use a JPEG:
1. Copy your photo to `static/images/avatar.jpg`
2. In `layouts/index.html` line 5, change `avatar.svg` → `avatar.jpg`

### 6. CV — `static/files/CV.pdf`

Drop your compiled CV here. The filename is configured via `cvFile` in `hugo.yaml`.

## Deployment

The site builds to `/public/` via `hugo`. You can deploy to:
- [GitHub Pages](https://gohugo.io/hosting-and-deployment/hosting-on-github/)
- [Netlify](https://gohugo.io/hosting-and-deployment/hosting-on-netlify/)
- [Vercel](https://gohugo.io/hosting-and-deployment/hosting-on-vercel/)

## License

MIT
