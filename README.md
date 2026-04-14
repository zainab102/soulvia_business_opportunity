# Soulvia lead page

Static page with a Formspree-backed contact form.

## 1. Formspree

1. Sign up at [formspree.io](https://formspree.io) and create a new form.
2. Copy the form id from the endpoint URL (`https://formspree.io/f/abcxyz` → id is `abcxyz`).
3. Open `config.js` and set `window.SOULVIA_FORMSPREE_ID` to that id. (This project is already set to `xwvapwqd`; change both `config.js` and the form `action` in `index.html` if you create a new form.)
4. In the Formspree dashboard, add your team email for notifications and confirm the address when they email you.

## 2. Deploy

**Netlify:** drag and drop this folder in [Netlify Drop](https://app.netlify.com/drop), or connect the repo. Publish directory is the project root (see `netlify.toml`).

**Vercel:** import the repo; root directory is this folder. `vercel.json` is optional.

**Cloudflare Pages:** connect the repo, build command empty, output directory `/` (root).

Upload at minimum: `index.html`, `config.js`, and the `assets/` folder (logo).

## 3. After deploy

- Open your live URL on a phone and submit a test lead.
- In Formspree, check **Submissions** and your inbox.
- Optional: turn on reCAPTCHA or rules in Formspree if you get spam.
