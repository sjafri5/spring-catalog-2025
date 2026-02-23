# Gulaab Garden - Catalog Website Instructions

## Your Setup

- **Live site:** https://gulaabgarden.com
- **GitHub repo:** https://github.com/sjafri5/spring-catalog-2025
- **Hosting:** Netlify (auto-deploys when you push to main)

## First Time Setup

```bash
git clone https://github.com/sjafri5/spring-catalog-2025.git
cd spring-catalog-2025
```

## How the Site Works

Everything is in one file: `index.html`. Your product images are in the `images/` folder.

### To add new images:
1. Drop new image files into the `images/` folder
2. Open `index.html` and find the `const images = [` array near the bottom
3. Add a new line like `"images/your-new-image.png",`

### To remove images:
1. Delete the line from the `images` array in `index.html`
2. Optionally delete the file from `images/`

### To change the hero text:
Search for these lines in `index.html` and edit them:
- `<h1>Spring Collection</h1>` - main title
- `<p class="subtitle">Handcrafted Block Print Textiles</p>` - subtitle
- `<p class="tagline">Artisan made...` - tagline

### To change the quote text:
Search for `Every piece tells a story` and change it.

### To make images link to product pages:
In the JavaScript section, find where grid items are created. Change the `onclick` to open a URL instead of the lightbox. For example, add a `data-url` attribute to each image in the array and update the click handler.

## Pushing Changes Live

```bash
git add .
git commit -m "describe your change"
git push
```

That's it. Netlify auto-deploys in about 15 seconds. Check gulaabgarden.com after a minute.

## Asking Claude Code to Help

You can give Claude Code these instructions:

> Pull down the repo at https://github.com/sjafri5/spring-catalog-2025.git - this is a static catalog site for Gulaab Garden (gulaabgarden.com). It's a single index.html with product images in the images/ folder. It auto-deploys to Netlify on push to main.
>
> [Then tell it what you want changed, for example:]
> - "Add these new product images and put them in the grid"
> - "Change the title to 'Summer 2025 Collection'"
> - "Make each image link to a specific product URL"
> - "Add a contact/inquiry section at the bottom"
> - "Change the color scheme to match my brand"
> - "Add product names and prices below each image"
> - "Reorder the images so the skirts come first"

After Claude makes changes, tell it to commit and push:

> Commit these changes and push to main. The site auto-deploys to gulaabgarden.com.
