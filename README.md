# Friday Around Noon

A simple practice website for **fridayaroundnoon.com**. No build tools, just plain HTML and CSS.

## What each file does

- **index.html**: The page itself. It holds the words and structure: the heading, the short intro, and the footer. Browsers open this file first.
- **styles.css**: The look. Colors, fonts, spacing, and the sunny background all live here. `index.html` links to it.
- **README.md**: This file. It explains the project. GitHub shows it on the repo's front page.

## How to see it on your computer

Download the files and double-click `index.html`. It opens in your browser.

## How deployment works

1. **GitHub** stores the code. Every time you change a file and save (commit) it, GitHub keeps the new version.
2. **Vercel** watches this GitHub repo. When something changes, it publishes the site to the internet automatically, usually in under a minute. Since there is no build step, Vercel just serves the files as they are.
3. **GoDaddy DNS** points the domain name at Vercel. In Vercel you add `fridayaroundnoon.com` as a domain, and Vercel tells you which DNS records to add in GoDaddy (usually an `A` record for the root domain and a `CNAME` for `www`). After that, typing fridayaroundnoon.com takes visitors to this site.

To update the live site: edit a file, commit it to GitHub, and Vercel does the rest.
