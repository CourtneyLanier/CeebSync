CeebSync Icons + Manifest
=========================

What this is
-------------
A minimal, non-PWA manifest with Android-ready icons so your S23 home screen shortcut uses your logo.

Files
-----
/manifest.webmanifest
/icons/icon-192.png
/icons/icon-512.png
/icons/maskable-192.png
/icons/maskable-512.png

How to install
--------------
1) Copy `manifest.webmanifest` to your site root.
2) Copy the entire `icons` folder to `/icons` at your site root.
3) Add the following to your HTML <head>:

   <link rel="manifest" href="/manifest.webmanifest">
   <meta name="theme-color" content="#C3D6A0">
   <!-- Optional fallbacks -->
   <link rel="icon" href="/icons/icon-192.png" sizes="192x192">

4) Deploy your site (Netlify) and then on your S23:
   - Delete the old home screen shortcut.
   - Open your site in Chrome/Samsung Internet.
   - Menu → Add to Home screen.

Troubleshooting
---------------
• If the old icon persists, clear site data or append a version to icon URLs in manifest, e.g. /icons/icon-192.png?v=2
• Ensure your server serves manifest with Content-Type: application/manifest+json
• Verify in Chrome DevTools → Application → Manifest that icons are detected.

Swapping in your real logo later
--------------------------------
Replace the PNGs in /icons with your logo exports (192x192 and 512x512). Keep at least 12–20% transparent padding around the artwork, and keep the maskable versions too so Android doesn’t crop.
