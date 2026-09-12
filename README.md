# emrysschoemaker.com

Personal site for Emrys Schoemaker — researcher and practitioner working on
digital governance, digital identity, and AI policy for the Global Majority.

Plain HTML/CSS/JS, no build step.

## Structure

- `index.html` — Home / About
- `research.html` — Research & Writing (policy commentary + academic publications)
- `projects.html` — Institutional engagements + the `memex` project
- `contact.html` — Contact details
- `assets/css/style.css` — shared styles
- `assets/js/main.js` — small page script (footer year)
- `assets/img/` — images

## Local preview

```
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Deployment

Deployed via GitHub Pages, with a custom domain configured in `CNAME`
(`emrysschoemaker.com`). To deploy:

1. In the repo settings, enable **Pages** with the source set to this branch's
   root.
2. At your domain registrar / DNS provider, point `emrysschoemaker.com` at
   GitHub Pages:
   - `A` records for the apex domain to GitHub Pages' IPs (see GitHub's
     [Pages custom domain docs](https://docs.github.com/pages/configuring-a-custom-domain-for-your-github-pages-site)), or
   - a `CNAME`/`ALIAS` record if your DNS provider supports apex aliasing
     (e.g. Cloudflare's CNAME flattening).
3. Once DNS propagates, enable **Enforce HTTPS** in the Pages settings.

Note: this only covers hosting the site itself. It does not host email —
Proton and other web hosts are unrelated to inbox delivery.

## Email (separate from site hosting)

`emrys@schoemaker.io` needs its own setup, independent of where the site is
hosted. If using Proton Mail for the mailbox:

1. Add the domain (`schoemaker.io`) in Proton Mail's custom domain settings.
2. Add the MX, SPF, DKIM, and DMARC records Proton provides at your DNS
   provider for `schoemaker.io`.
3. Verify the domain in Proton once records propagate.

This is unrelated to the `emrysschoemaker.com` DNS records used for GitHub
Pages above — different domains, different record types, no conflict.

## Content still to fill in

- Real publication titles/citations under Research & Writing (currently
  placeholders)
- The `memex` repo itself (`github.com/Emrys-S/memex`) — linked from Projects
  but not yet created
