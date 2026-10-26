# Friday Around Noon

A fictional, goofy beer-delivery website for **fridayaroundnoon.com**. Cold beer shows up at your office or home every Friday around noon — in the story. Nothing here is a real order.

Plain HTML and CSS. No build step. Vercel serves the files as they are.

## Pages

- **index.html**: The homepage. A sunny hero, the tagline, three selling points, and a button to the contact form.
- **how-it-works.html**: The four-step drop-off, plus a delivery-zone joke about where a cooler will and will not go.
- **pricing.html**: Three subscription tiers with silly names and fake prices (Desk Buddy, Meeting MVP, Floor Legend), and a short FAQ.
- **about.html**: The founder story. Casey Noon is not a real person. The empty office fridge is the joke.
- **contact.html**: The note form. Name, email, optional phone, a “Pick your Friday” dropdown, and a message.
- **thanks.html**: The thank-you page. The form sends people here after a successful submit. It is not in the menu.
- **styles.css**: The shared look. Every page links to this one file for colors, type, the nav, and the footer. The colors follow the logo: sunny yellow `#ffcb13`, coral `#fd6651`, and charcoal `#2d2e33`.
- **images/logo.png**: The full logo, trimmed and sized for the web. The homepage hero uses it.
- **images/logo-icon.png**: Just the truck and sun. The header on every page uses it next to the name.
- **images/favicon.png**: A small square of that same truck icon, for the browser tab.
- **README.md**: This file. GitHub shows it on the repo’s front page.

Every page uses the same header links and the same footer. The footer says this is a fictional demo business, that you must be 21 or older, and to drink responsibly.

## How the contact form works

The form on `contact.html` is a normal HTML form. It posts to Web3Forms at `https://api.web3forms.com/submit`. There is no JavaScript and no build.

1. **Access key.** A hidden input named `access_key` is set to `YOUR_WEB3FORMS_ACCESS_KEY`. That is a placeholder. Create a key at [web3forms.com](https://web3forms.com/), then replace the placeholder in `contact.html`. Web3Forms expects this key in the page. Until you swap it in, a submit will not arrive as email.
2. **Honeypot.** A hidden checkbox named `botcheck` sits in the form. People do not see it or fill it in. If a bot checks it, Web3Forms throws the submission out.
3. **Redirect.** A hidden input named `redirect` is `https://fridayaroundnoon.com/thanks.html`. After a successful send, Web3Forms sends the visitor to that thank-you page.
4. **The fields a person fills in.** Name, email, phone (optional), the Friday dropdown, and a message. Web3Forms puts those in the email. The email subject is “New Friday note from fridayaroundnoon.com”.

The thank-you page only appears when the key works and the send succeeds. Sending the form does not place an order or charge a card.

## How to see it on your computer

Open `index.html` in a browser. The links between pages work from the file itself. You do not need a server.

## How deployment works

1. **GitHub** stores the code. Every time you change a file and commit it, GitHub keeps the new version.
2. **Vercel** watches this GitHub repo. When something changes, it publishes the site, usually in under a minute. Because there is no build step, Vercel just serves the files as they are.
3. **GoDaddy DNS** points the domain at Vercel. In Vercel you add `fridayaroundnoon.com` as a domain, and Vercel tells you which DNS records to add in GoDaddy (usually an `A` record for the root domain and a `CNAME` for `www`). After that, the domain opens this site.

To update the live site: edit a file, commit it to GitHub, and Vercel does the rest.
