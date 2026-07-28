# WCiA Project Website

Static multi-page site rebuild for the World's Children in Africa (WCiA) Project.

## Pages
- index.html — Home (rotating hero slider, "Explore WCiA" cards, latest news)
- about.html — About WCiA Project (mission narrative + UNICEF statistics)
- product.html — About Our Cause-Related Product (Children's Writing Companion)
- events.html — About Our Events
- roundtable.html — About WCiA Donors' Round Table
- mission-values.html — Vision, Mission, Core Values, Our Approach
- partnering.html — Ways to Partner / Support
- donate.html — Donate (Stripe + Paystack links wired in)
- contact.html — Contact form + info (Formspree-connected)
- terms.html — Terms of Use
- privacy.html — Privacy Policy
- style.css — Shared stylesheet for all pages

## How to publish
Fully static site — no build step required. Upload all files (flat structure,
same folder) to Netlify, GitHub Pages, or any static host. Make sure
index.html sits at the root of wherever your domain points.

## Contact form
The contact form is wired to Formspree: https://formspree.io/f/mrenjqwl
Submissions are emailed to whatever address is registered on that Formspree
account. To change the destination email, log into formspree.io and update
the form's notification settings — no code changes needed.

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
