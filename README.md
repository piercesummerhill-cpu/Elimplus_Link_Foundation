# ElimuPlus-Link Foundation website

A portable static website for ELIMUPLUS-LINK FOUNDATION (ELF). It has no build step and can be deployed to Cloudflare Pages, GitHub Pages, Netlify, Vercel, or traditional hosting.

## Files

- `index.html` — homepage content and accessible semantic markup
- `styles.css` — responsive visual design
- `assets/elimuplus-link-foundation-logo.jpeg` — supplied logo

## Preview locally

Double-click `index.html` to open it in a browser. For a more accurate local server preview, from this folder run:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Publish with GitHub and Cloudflare Pages

1. On GitHub, create a new **public** repository named `elimuplus-link-foundation`.
2. Upload `index.html`, `styles.css`, and the entire `assets` folder. Keep the folder structure unchanged.
3. Create or sign in to an ELF-controlled Cloudflare account. Enable two-factor authentication and add at least two trusted administrators.
4. In Cloudflare, choose **Workers & Pages** → **Create application** → **Pages** → **Connect to Git**.
5. Select the GitHub repository. For this static site, select a no-framework/static configuration. Use `/` as the output directory if Cloudflare requests it. Deploy.
6. Test the temporary `pages.dev` address on a phone and computer.

## Connect the .org domain after testing

Do not change DNS until the temporary site works.

1. In Cloudflare Pages, open the project → **Custom domains** → add `elimupluslinkfoundation.org` and `www.elimupluslinkfoundation.org`.
2. Cloudflare will display the exact DNS configuration required. Follow it exactly in the Northwest Registered Agent domain dashboard, or move DNS management to Cloudflare if you prefer.
3. Preserve all existing mail records. The public email currently uses the different `.com` domain: `info@elimupluslinkfoundation.com`; do not remove or change its MX, SPF, DKIM, or DMARC records.
4. Set one domain as the canonical redirect (normally `https://www.elimupluslinkfoundation.org` or the non-www version—choose one), then enable HTTPS once Cloudflare indicates it is ready.

## Content updates

Edit text in `index.html`; edit appearance in `styles.css`; replace the logo/photo files in `assets/` while preserving their names or updating the relevant `src` attributes. Commit and push changes to GitHub; Cloudflare Pages redeploys automatically.

## Donations and forms

No live donation processor or contact-form backend is included. The Support ELF button opens a draft email. Before enabling donations, ELF should approve the donation provider, legal entity, receiving bank account, accounting process, donor privacy disclosures, and applicable tax language. Replace the mail link only after those are confirmed.

To add a form later, use a reputable form backend such as Formspree or a serverless function. Do not put API keys, payment credentials, or private donor data in this repository.

## Ownership & security

- Keep domain, GitHub, Cloudflare, email, donation provider, and analytics accounts under ELF ownership.
- Use separate named user accounts, MFA, recovery codes, and at least two administrators.
- Never commit passwords, API keys, banking details, or donor information.
- Review access when volunteers or staff leave.

## Pre-launch checklist

- Confirm all phone numbers, address, registration number, and public email.
- Obtain written approval for leadership names, biographies, metrics, testimonials, reports, and photos.
- Confirm donation method before changing donation wording or links.
- Add a privacy policy before collecting form submissions, analytics data, or donations.
- Test keyboard navigation, screen-reader labels, phones, tablets, major browsers, and all links.
