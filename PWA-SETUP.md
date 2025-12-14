# PWA Setup Instructions

Your Focus Notes app is now configured as a Progressive Web App (PWA)! Here's what you need to complete the setup:

## ✅ Already Done
- Created `manifest.json` with PWA configuration
- Created `sw.js` (Service Worker) for offline functionality
- Added PWA meta tags to `focus-notes.html`
- Added service worker registration script

## 📱 What You Need To Do

### 1. Create Icon Images
You need to create two PNG icon files and place them in the project root directory:

- **icon-192.png** - 192x192 pixels
- **icon-512.png** - 512x512 pixels

**Icon Tips:**
- Use a simple, recognizable design (the 📝 emoji or "FN" text works great)
- Make sure the icon has good contrast
- Use a square canvas with transparent or solid background
- The icon should look good at small sizes

**Free Icon Tools:**
- [Favicon.io](https://favicon.io/) - Generate icons from text/emoji
- [Canva](https://www.canva.com/) - Design custom icons
- [GIMP](https://www.gimp.org/) - Free image editor
- Online PNG generators from emoji

### 2. Enable HTTPS
PWAs require HTTPS to work (except on localhost for testing).

**Options for HTTPS hosting:**
- GitHub Pages (free, automatic HTTPS)
- Netlify (free, automatic HTTPS)
- Cloudflare Pages (free, automatic HTTPS)
- Your own server with Let's Encrypt (free SSL certificate)

### 3. Test the PWA

Once you have icons and HTTPS enabled:

1. Open your app in Chrome on Android
2. Open the browser menu (three dots)
3. Look for "Install app" or "Add to Home Screen"
4. Tap it and confirm
5. The app icon will appear on your home screen!

**Testing Offline:**
1. Install the app
2. Open it once (this caches the files)
3. Turn on Airplane mode
4. Open the app - it should still work!
5. Your notes are stored in localStorage, so they persist

## 🔍 Troubleshooting

**"Install" option doesn't appear:**
- Make sure you're using HTTPS (or localhost)
- Check that icon files exist and are accessible
- Open Chrome DevTools > Application > Manifest to see any errors
- Ensure the service worker is registered (DevTools > Application > Service Workers)

**App doesn't work offline:**
- Check DevTools > Application > Service Workers
- Make sure the service worker is "activated and running"
- Try clearing the cache and reloading

## 📂 File Structure
```
focus-notes/
├── focus-notes.html    (main app file)
├── manifest.json       (PWA configuration)
├── sw.js              (service worker)
├── icon-192.png       (← you need to create this)
└── icon-512.png       (← you need to create this)
```

## 🎨 Current Theme Colors
The manifest uses your app's header color (#2c3e50) for the theme. If you want to change this, edit the `theme_color` and `background_color` in `manifest.json`.
