# Soulvia lead page

Static page with a Formspree-backed contact form.

**Live site:** [https://soulviabusinessopportunity.vercel.app](https://soulviabusinessopportunity.vercel.app)

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

## 4. Google Ads (lead form goal)

After a successful submit, users land on **`thank-you.html`**. In Google Ads, use this as the conversion URL:

`https://soulviabusinessopportunity.vercel.app/thank-you.html`

UTM parameters from the landing page are preserved on the thank-you URL. Add your **Google tag** on both `index.html` and `thank-you.html` when you set up conversion tracking.
