# WCiA Project Website

Static multi-page site rebuild for the World's Children in Africa (WCiA) Project.

## Files
- index.html — Home
- about.html — About WCiA (mission narrative, cause-related product, events, donors' roundtable)
- mission-values.html — Vision, Mission, Core Values
- partnering.html — Ways to Partner / Support
- donate.html — Donate page (Stripe + Paystack links wired in)
- contact.html — Contact form + info
- style.css — Shared stylesheet for all pages

## How to publish
This is a fully static site — no build step, no server-side code required.
Upload all files (keeping them in the same folder, flat structure) to any of:
- Netlify / Vercel (drag-and-drop the folder)
- GitHub Pages
- Your existing cPanel / shared hosting via FTP (upload into public_html)
- Any static file host (S3 + CloudFront, Cloudflare Pages, etc.)

Just make sure index.html sits at the root of wherever your domain points.

## IMPORTANT: before the contact form works
The contact form on contact.html is wired to use Formspree (a free, no-backend
form-to-email service) but needs your own endpoint:

1. Go to https://formspree.io and create a free account.
2. Create a new form, and set its notification email to contact@wciaproject.org
   (or whichever inbox should receive messages).
3. Formspree will give you a form endpoint that looks like:
   https://formspree.io/f/xxxxabcd
4. Open contact.html, find this line near the form:
   <form id="contact-form" action="https://formspree.io/f/YOUR_FORMSPREE_ID" method="POST">
   and replace YOUR_FORMSPREE_ID with your real Formspree ID.

Until that's done, submitting the form will show a message asking visitors to
email or call directly instead of failing silently.

## Other things to swap in before going fully live
- Real photography (currently uses stock photos from Unsplash)
- Real social media links (currently placeholder # links in the footer/contact page)
- Terms of Use / Privacy Policy pages (currently placeholder # links)
- Confirm the Stripe and Paystack donation links in donate.html still match your
  live payment accounts.
