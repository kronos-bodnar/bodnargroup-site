# bodnargroup.com

Static rebuild of the Bodnar Investment Group site (moved off Squarespace). Plain HTML + CSS, no build step, hosted on GitHub Pages.

- `index.html`: the whole site (one page)
- `style.css`: styles (brand blue `#0082cb`, Poppins headings, Esteban body)
- `img/`: images pulled from the live Squarespace site

Contact form: posts to FormSubmit → accounting@bodnargroup.com (one-time activation email must be clicked in that inbox).

## Deploy
GitHub Pages serves the `gh-pages` branch (Pages was auto-enabled by pushing it; the PAT can't hit the Pages API). Push changes to both: `git push origin main main:gh-pages`.

## Go-live checklist
1. Remove the `noindex` meta tag
2. ~~Wire the contact form~~ done (FormSubmit → accounting@)
3. Add a `CNAME` file containing `www.bodnargroup.com`
4. GoDaddy DNS: replace the 4 Squarespace A records with GitHub's (185.199.108.153, .109.153, .110.153, .111.153); point `www` CNAME at `kronos-bodnar.github.io`. Do NOT touch MX/TXT (Microsoft 365 email).
