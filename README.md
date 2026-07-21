# Phan Anh Tu — Personal Academic Website

Personal academic website of **Assoc. Prof. Phan Anh Tu** — Vice President of the School of Economics, Can Tho University, Vietnam.

**🌐 Live site: [https://thuyhuongctu.github.io/phan-anh-tu-website/](https://thuyhuongctu.github.io/phan-anh-tu-website/)**

This is a static, single-file website: everything lives in `index.html`, which contains all pages — Home, Research, Teaching, CV, Events, Me Blog, Photos, Aphorisms, 3L Learning, and Contact. Page switching is handled with hash-based JavaScript navigation (`#research`, `#cv`, …), with dark-mode support and a responsive layout for mobile devices.

## How to run

### 1. Run locally

Simply open `index.html` in a browser (double-click the file), or start a simple web server:

```bash
# If Python is available:
python3 -m http.server 8000
# Then open: http://localhost:8000
```

### 2. Deployment (GitHub Pages — free)

The repository ships with an automatic deployment workflow (`.github/workflows/deploy.yml`). Deployment is already configured and live. Every push to the default branch automatically rebuilds and republishes the site within 1–2 minutes.

One-time setup (already done):

1. Repository visibility set to **Public** (GitHub Pages is free for public repositories).
2. **Settings → Pages → Source** set to **GitHub Actions**.

### 3. Custom domain (optional)

To serve the site under a custom domain (e.g. a university subdomain such as `phananhtu.ctu.edu.vn`, or a purchased domain like `phananhtu.com`):

1. Go to **Settings → Pages → Custom domain** and enter the domain.
2. Point the domain's DNS to GitHub Pages (a CNAME record to `thuyhuongctu.github.io`) following GitHub's instructions.

## Pre-launch checklist

- [ ] **Portrait photo**: replace the "PAT" placeholder in `index.html` with a real portrait (square crop).
- [x] **University logos**: official Can Tho University and School of Economics logos are in use (`assets/logo-ctu.png`, `assets/logo-soe.png`).
- [ ] **CV file**: place the PDF at `assets/Phan_Anh_Tu_CV_May2026.pdf` (the "Download CV" button points to this path).
- [ ] **Contact form**: currently opens the visitor's email client (mailto). A hosted form backend (e.g. Formspree or Basin) can be connected if direct message delivery is preferred.

## Project structure

```
├── index.html              # The entire website (HTML + CSS + JavaScript)
├── assets/                 # Logos, favicon, CV PDF, images, …
└── .github/workflows/
    └── deploy.yml          # Automatic deployment to GitHub Pages
```
