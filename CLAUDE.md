# PersonalWeb — hassairi.com

## What This Is
Personal website and blog hosted on GitHub Pages at hassairi.com. Static HTML, no 
build system, no framework. Deployed by pushing to `git@github.com:kaisarea/hassairi.com.git`.

## Site Structure
- `index.html` — main page (About, Research, Path sections)
- `story.html`, `life.html`, `reading.html` — personal pages
- `causal-inference.html`, `data-at-scale.html`, `measurement.html`, `ml-nlp.html`, 
  `survey.html`, `leadership.html` — research/expertise pages
- `blog/index.html` — blog listing page
- `blog/*.html` — individual blog posts
- `cs/` — Czech language versions
- `story.css` — shared stylesheet (template based)
- `sitemap.xml`, `robots.txt` — SEO
- `favicon.svg` — site icon

## Blog Post Template
All blog posts follow the same HTML structure:
- `nav` with links back to main site and blog index
- `story-hero` header with `story-kicker` (date) and `story-title`
- `story-body` > `story-container` with `story-chapter` sections
- `story-aside-label` for section headers within chapters
- `story-lede` class on the opening paragraph
- `story-coda` class on the closing section (with `story-divider`)
- Further reading section as a styled `<ul>`
- Footer with back-link to blog index

Each post includes: meta description, canonical URL, Open Graph tags, Twitter Card 
tags, and JSON-LD Article schema.

## Blog Posts (newest first)
- `governance-system.html` — Context engineering and AI agent governance (Aug 2026)
- `unforced-error.html` — European IT rationing / Draghi Report (Jul 2026)
- `virtuous-cycle.html` — AI learning virtuous cycle (Jul 2026)
- `excel-all-the-way-down.html` — FP&A data platform architecture (Jul 2026)
- `marginal-returns-cross-tabs.html` — Analytics vs dashboarding (May 2026)
- `head-start-dual-language-learners.html` — ECRQ publication (Apr 2026)

## When Adding a New Blog Post
1. Create the HTML file in `blog/` using the template above
2. Add an entry to `blog/index.html` (newest first)
3. Add a `<url>` entry to `sitemap.xml` with priority 0.9
4. Commit all three files together

## Deployment
- Git remote is SSH: `git@github.com:kaisarea/hassairi.com.git`
- SSH key at `~/.ssh/id_ed25519` requires a passphrase — user must push manually
- After committing, provide the push command for the user to run

## Writing Style (blog posts)
- First person, measured tone — do not oversell or make claims beyond personal experience
- Do not speak for others unless quoting them
- Precise language — the author will push back on imprecision
- Prose over bullet points in the body; lists acceptable in Further Reading
- Confidentiality: do not include employer-identifying details (company names, specific 
  financial figures, system names, organizational structure)
