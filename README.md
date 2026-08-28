# Wellness Eras — site

A plain HTML/CSS site, no build step, no framework. Pages:

- `index.html` — landing page, free 7 Day Plan opt-in
- `welcome.html` — delivery page shown right after signup, plus a soft offer for the 28 Day Plan
- `28-day-plan.html` — product page for the $2.99 28 Day Plan
- `privacy.html` / `terms.html` — linked in every footer
- `favicon`, `apple-touch-icon.png`, `og-image.png` — browser tab icon and social share preview, generated from the brand mark, no action needed unless you want to change the logo later

## 1. Push to GitHub

```bash
cd wellness-eras-site
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/wellness-eras-site.git
git push -u origin main
```

## 2. Deploy on Vercel

- Go to vercel.com, "Add New Project", import this GitHub repo
- Framework preset: "Other" (no build command needed, it's static HTML)
- Deploy. Vercel serves the HTML files as-is.

## 3. Connect wellnesseras.com

In the Vercel project, go to Settings > Domains, add `wellnesseras.com` and
follow the DNS instructions Vercel gives you (usually an A record or CNAME
at your domain registrar). This is separate from the SPF/DKIM/DMARC records
for your email sending domain, those live in the same DNS panel but don't
conflict with this.

## 4. Wire up MailerLite (email capture)

In `index.html`, find this block:

```html
<form class="ml-embed" action="https://assets.mailerlite.com/jsonp/YOUR_ACCOUNT_ID/forms/YOUR_FORM_ID/subscribe" method="post" target="_blank">
```

Replace `YOUR_ACCOUNT_ID` and `YOUR_FORM_ID` with the values from your
MailerLite account under Forms > Embedded forms > this form > Embed code.
If you'd rather use MailerLite's own generated embed snippet instead of this
custom-styled form, you can paste their `<script>` embed directly in place
of the `<form>` block, the surrounding layout will still hold its shape.

After someone signs up, point their MailerLite automation's redirect (or
their "after subscribing" setting) to `https://wellnesseras.com/welcome`,
that's what actually delivers the free plan.

## 5. Add the real PDF

Drop your finished 7 Day Plan PDF into `downloads/` and name it
`wellness-eras-7-day-plan.pdf`. The download button on `welcome.html`
already points there, no other change needed.

## 6. Wire up the 28 Day Plan checkout

In `28-day-plan.html`, find:

```html
<a class="btn btn-primary" href="https://buy.stripe.com/YOUR_CHECKOUT_LINK">
```

Replace with your real MailerLite digital product checkout link (from
MailerLite's Digital Products / Stripe integration, see MailerLite's
"Sell Stripe Products" setup) or a direct Stripe Payment Link.

## Editing content

There's no templating, each page is a full standalone HTML file sharing
`styles.css`. Copy is written directly in the HTML, search for the text
you want to change and edit it in place.
