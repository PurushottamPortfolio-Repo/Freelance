````md
# Production Grade Company Portfolio Website Workflow
### Tech Stack
- React 19
- Vite
- Tailwind CSS v4
- React Router
- Axios
- React Helmet Async
- Framer Motion (Optional)
- React Hook Form
- Vercel (Client Review)
- Hostinger (Production)

---

# Overall Workflow

```
Requirement Gathering
        │
        ▼
Planning & Architecture
        │
        ▼
UI/UX Design
        │
        ▼
Project Setup
        │
        ▼
Development
        │
        ▼
Testing
        │
        ▼
Production Build
        │
        ▼
Deploy to Vercel
(Client Approval)
        │
        ▼
Client Feedback
        │
        ▼
Final Build
        │
        ▼
Deploy to Hostinger
        │
        ▼
Maintenance
```

---

# Phase 1 — Requirement Gathering

Collect

- Company Name
- Brand Colors
- Logo
- Typography
- Target Audience
- Competitors
- Services
- Products
- Projects
- Testimonials
- Team Members
- Contact Details
- Social Media
- Office Address
- Domain
- Hosting

Prepare

```
Project Requirement Document

Wireframes

Content List

Assets Folder
```

---

# Phase 2 — Project Architecture

```
src/
│
├── assets/
│
├── components/
│      Navbar
│      Footer
│      Buttons
│      Cards
│      Forms
│
├── sections/
│      Hero
│      About
│      Services
│      Projects
│      Testimonials
│      CTA
│      Contact
│
├── pages/
│      Home
│      About
│      Services
│      Projects
│      Contact
│      NotFound
│
├── hooks/
│
├── context/
│
├── utils/
│
├── constants/
│
├── api/
│
├── routes/
│
├── layouts/
│
└── App.jsx
```

---

# Phase 3 — Git Workflow

Initialize

```bash
git init
```

Create repository

```
GitHub
```

Branches

```
main

development

feature/navbar

feature/contact

feature/services

feature/footer

bugfix/*
```

Commit Style

```
feat:

fix:

refactor:

docs:

style:

build:
```

---

# Phase 4 — Environment Setup

Never hardcode

- API URL
- Email Keys
- Analytics IDs
- Secret Keys

Example

```
.env.local

.env.production
```

Example

```env
VITE_API_URL=https://api.company.com

VITE_SITE_URL=https://company.com

VITE_GOOGLE_ANALYTICS=xxxx

VITE_CONTACT_EMAIL=support@company.com
```

Never upload

```
.env

.env.local

.env.production
```

Add into

```
.gitignore
```

---

# Phase 5 — Install Dependencies

```bash
npm install
```

Install

```bash
npm install react-router-dom

npm install axios

npm install react-hook-form

npm install react-helmet-async

npm install react-toastify

npm install framer-motion

npm install react-icons

npm install clsx
```

---

# Phase 6 — Tailwind Setup

Create

```
Global Color System

Typography

Spacing

Breakpoints

Container

Theme Variables
```

Maintain

```
Primary

Secondary

Accent

Background

Surface

Text

Border

Success

Warning

Danger
```

---

# Phase 7 — Development

Develop page by page

```
Navbar

Hero

About

Services

Projects

Gallery

Testimonials

Contact

Footer
```

Each section should be

- Reusable
- Responsive
- Accessible

---

# Phase 8 — Responsive Design

Test

```
320px

375px

425px

768px

1024px

1280px

1536px
```

---

# Phase 9 — SEO

Every page should have

Title

Description

Canonical

Keywords

Open Graph

Twitter Card

Robots

Favicon

Sitemap

Manifest

Schema

Example

```
Helmet

title

meta

canonical
```

---

# Phase 10 — Performance

Optimize

Images

Fonts

Animations

Bundles

Code Splitting

Lazy Loading

Memoization

Preload Fonts

Compression

Tree Shaking

---

# Phase 11 — Accessibility

Use

ARIA

Keyboard Navigation

Alt Text

Semantic HTML

Proper Heading Order

Color Contrast

Focus States

---

# Phase 12 — Security

## Never expose

API Keys

JWT Secret

SMTP Password

Database Credentials

Private Tokens

Payment Keys

Server URLs

Admin Credentials

---

## Never commit

```
.env

node_modules

dist

.vscode/settings.json
```

---

## Input Validation

Validate

Forms

Email

Phone

URLs

Text Length

Prevent

XSS

Injection

Spam

---

## Contact Form

Never directly send email from frontend.

Preferred

```
Frontend

↓

Backend API

↓

Email Service
```

Examples

- EmailJS (small projects)
- Server API
- Cloud Function

---

## CORS

Allow only

```
Production Domain

Vercel Preview

Localhost
```

---

## HTTPS

Always use

```
https://
```

---

# Phase 13 — Testing

Test

Navigation

Forms

Images

SEO

Links

404

Responsiveness

Animations

Accessibility

Console Errors

Lighthouse

---

# Phase 14 — Production Build

```bash
npm run build
```

Preview

```bash
npm run preview
```

Fix all

Warnings

Errors

Console Logs

Unused Files

---

# Phase 15 — Upload to GitHub

```bash
git add .

git commit -m "Production Ready"

git push origin main
```

---

# Phase 16 — Deploy to Vercel

Connect

GitHub Repository

↓

Import Project

↓

Framework

```
Vite
```

↓

Environment Variables

↓

Deploy

Vercel automatically provides

```
Preview URL

Production URL
```

Example

```
company.vercel.app
```

---

# Phase 17 — Client Approval

Share

```
Preview URL
```

Collect

Design Changes

Content Changes

Image Updates

SEO Changes

Color Changes

Typography

Animations

Fixes

Repeat until approved.

---

# Phase 18 — Final Deployment (Hostinger)

Build

```bash
npm run build
```

Upload

```
dist/
```

into

```
public_html/
```

If SPA

Create

```
.htaccess
```

Example

```
RewriteEngine On
RewriteBase /
RewriteRule ^index\.html$ - [L]
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule . /index.html [L]
```

Point Domain

```
DNS

A Record

or

Hostinger Deployment
```

Enable

SSL

HTTPS

Compression

Caching

---

# Phase 19 — After Deployment

Verify

Homepage

Forms

SEO

404

Images

Robots

Sitemap

Analytics

Search Console

Performance

---

# Phase 20 — Monitoring

Monitor

Google Analytics

Search Console

Hostinger Logs

Performance

Broken Links

Backups

Security

---

# Recommended Folder Structure

```
project/

src/

public/

.env.local

.env.production

.gitignore

package.json

README.md

vite.config.js
```

---

# Production Checklist

## Development

- Requirements Completed
- Responsive
- Reusable Components
- Clean Architecture
- ESLint Passed
- No Console Errors

---

## SEO

- Titles
- Description
- Sitemap
- Robots
- Schema
- Open Graph

---

## Security

- No Secrets in Git
- Environment Variables
- HTTPS
- Form Validation
- XSS Prevention
- Sanitized Inputs

---

## Performance

- Lazy Loading
- Optimized Images
- Code Splitting
- Tree Shaking
- Compression
- Font Optimization

---

## Deployment

- GitHub
- Vercel Preview
- Client Approval
- Production Build
- Hostinger Upload
- SSL Enabled

---

# Complete Workflow Summary

```
Requirements
      │
      ▼
Design
      │
      ▼
React + Vite Setup
      │
      ▼
Tailwind Setup
      │
      ▼
Development
      │
      ▼
GitHub
      │
      ▼
Vercel Preview
      │
      ▼
Client Approval
      │
      ▼
Production Build
      │
      ▼
Hostinger Deployment
      │
      ▼
SSL + SEO + Analytics
      │
      ▼
Maintenance
```
````
