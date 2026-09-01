# Wellness Eras Website

GitHub-ready static website for wellnesseras.com.

## Included

- Responsive landing page
- Preserved Sender universal script
- Preserved Sender form ID: `bmZ39R`
- Hero food asset in `images/hero-food.svg`
- 28 Day Plan page
- Privacy page
- Terms page
- No framework or build step required

## Change the hero image

Replace:

`images/hero-food.svg`

Then update the image extension/path in `index.html` if you use JPG or PNG.

The relevant line is:

`<img src="images/hero-food.svg" ...>`

## Sender integration

The supplied Sender account initialization and form ID were preserved from the original index file. Do not remove the Sender script in the `<head>` or the `data-sender-form-id="bmZ39R"` element unless you intentionally change the form.

## GitHub Pages

Upload all files to your repository root. If using GitHub Pages, set the Pages source to the branch/folder containing `index.html`.

## Custom domain

For GitHub Pages, add your custom domain in repository Settings > Pages. DNS records at your domain provider must point to the GitHub Pages configuration GitHub gives you.

## Important

The legal pages are starter copy, not legal advice. Review them for your actual business, jurisdiction, email practices, and tracking tools before publishing.
