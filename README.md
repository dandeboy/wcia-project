# WCiA Project Website

Static multi-page site rebuild for the World's Children in Africa (WCiA) Project.

## Pages
- index.html — Home (rotating hero slider, "Explore WCiA" cards, latest news)
- about.html — About WCiA Project (mission narrative + UNICEF statistics)
- product.html — About Our Cause-Related Product (Children's Writing Companion)
- events.html — About Our Events
- roundtable.html — About WCiA Donors' Round Table
- join-roundtable.html — Donor's RoundTable registration form (file upload — Netlify Forms)
- mission-values.html — Vision, Mission, Core Values, Our Approach
- partnering.html — Ways to Partner / Support
- donate.html — Donate (Stripe + Paystack links wired in)
- contact.html — Contact form + info (Netlify Forms)
- terms.html — Terms of Use
- privacy.html — Privacy Policy
- style.css — Shared stylesheet for all pages

## How to publish
Fully static site — no build step required. Upload all files (flat structure,
same folder) to your GitHub repo, which Netlify auto-deploys from.

**Important — both forms below only work once deployed on Netlify.** They
will NOT work if opened locally, hosted on GitHub Pages, Vercel, or any
non-Netlify platform — Netlify detects and processes these forms
automatically at deploy time by scanning the built HTML for the
`data-netlify="true"` attribute. On any other host, submitting shows the
JS error message instead of succeeding.

## Contact form (contact.html)
Wired to **Netlify Forms** — no external account needed. After your next
deploy, submissions appear in Netlify dashboard → your site → **Forms** →
"contact". Turn on email notifications there (Forms → Settings → Form
notifications) so you get pinged whenever someone submits, instead of
having to check the dashboard manually.

## Donor's RoundTable registration form (join-roundtable.html)
Also wired to **Netlify Forms**, which is why this one was switched over in
the first place — it includes a file upload field (Donor Profile), and
Formspree's free tier doesn't support file uploads. Submissions (including
uploaded files) appear under Forms → "roundtable-registration" in the same
dashboard.

Real-world file size limits are considerably lower than the "2GB" text
copied from the original site's copy (that number was likely aspirational
even there) — Netlify's practical ceiling for form file uploads is much
smaller. If large files matter, this may need a dedicated upload service.

## Images
All images are pulled live from wciaproject.org's WordPress media library.
This means:
- No large image files bloat this download
- If an image is ever removed/renamed on wciaproject.org, it will break here too
- For full independence from the old site, download the images used and
  update the <img src="..."> and background-image url("...") references to
  point to local files instead

## Social media
WCiA does not currently have confirmed, dedicated social media accounts
(the links on the live site point to generic platform homepages, not WCiA's
own profiles) — so no social icons are included here. Add them back in the
footer of style.css / each page's <footer> once real accounts exist.

## Still using placeholder/example content
- Bank transfer details (contact.html directs enquiries here — real account
  details need to be added once available)
- "Read Our Latest News" section — no news system yet, shows "coming soon"
