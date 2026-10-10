# ibrohimovasharifa-hash.github.io

Portfolio of Sharifa Ibrohimova: marketing operations and campaign analytics.

Live: https://ibrohimovasharifa-hash.github.io/

## How it's built

- HTML, CSS and vanilla JavaScript. No framework, no static site generator, no template, no build step. Code written with AI assistance; structure, tracking, CRM integration and testing specified, configured and verified by me.
-  Hosted on GitHub Pages. Jekyll processing is disabled with `.nojekyll`, so files are served exactly as committed.
- Mobile-first layout, tested down to 375px width.

## Status

In build, October 2026. Items are ticked only once shipped and verified.

- [ ] Semantic HTML: Home, Case studies, About, Contact
- [ ] Responsive CSS, verified at 375px
- [ ] Contact form sent to HubSpot CRM with vanilla JavaScript
- [ ] Google Tag Manager container, with GA4 configured through GTM
- [ ] Two GA4 custom events and one key event
- [ ] Yandex Metrica through GTM
- [ ] UTM taxonomy for CV, LinkedIn and job-board links
- [ ] Meta titles and descriptions, Open Graph tags, sitemap.xml, robots.txt
- [ ] PageSpeed audit with one documented improvement
- [ ] Automated broken-link check on every push

## Structure

    /                       Home
    /case-studies/<slug>/   One folder per case study
    /about/
    /contact/
    /ru/                    Reserved for a Russian version

## Commit messages

Imperative, one change per commit: "Add contact form", "Fix nav overflow at 375px".
