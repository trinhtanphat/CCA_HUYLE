# CCA_HUYLE Landing Page Clone

This project is a full frontend clone of https://cca.saniio.com with local assets.

## What is included

- Full homepage layout and sections from the source site
- Local CSS, JS, image, video, and font assets (no remote font dependency for icon packs)
- Extra expert testimonial section added near the end of the page
- Performance tuning in main script for smoother scroll and resize behavior

## Project structure

- index.html
- css/
- js/
- images/
- video/
- fonts/

## Run locally

Option 1: Python

1. Open terminal in project root
2. Run:

   python -m http.server 5500

3. Open:

   http://localhost:5500

Option 2: Node serve

1. Open terminal in project root
2. Run:

   npx serve .

3. Open the URL shown in terminal

## Deployment checklist

1. Upload all files and folders exactly as-is to your server root
2. Keep relative paths unchanged
3. Ensure these folders are included:
   - css
   - js
   - images
   - video
   - fonts
4. Hard refresh browser after deploy to clear old cache

## Avatar note

The expert testimonial section uses this avatar path:

images/expert/le-dinh-huy.jpg

If your image is not showing, verify the file exists at that exact path and name.

## Performance notes

The script was tuned to reduce heavy main-thread work:

- Resize handler is debounced
- Scroll handler is frame-throttled with requestAnimationFrame
- Background loop moved from setInterval to requestAnimationFrame
- Heavy motion effects are reduced when browser prefers reduced motion

## Credits

Original design/content source: https://cca.saniio.com
