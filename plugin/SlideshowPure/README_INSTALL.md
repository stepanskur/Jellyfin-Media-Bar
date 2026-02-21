Installation
------------

1) Copy the `SlideshowPure` folder to your Jellyfin server web extensions directory.

Linux (example):

```bash
# stop jellyfin service first (optional but recommended)
sudo systemctl stop jellyfin

sudo mkdir -p /var/lib/jellyfin/web/extensions/SlideshowPure
sudo cp -r plugin/SlideshowPure/* /var/lib/jellyfin/web/extensions/SlideshowPure/

# start jellyfin
sudo systemctl start jellyfin
```

Windows (example):

1. Copy the `SlideshowPure` folder to `%ProgramData%\\Jellyfin\\Server\\web\\extensions\\SlideshowPure`.
2. Restart the Jellyfin service.

2) Clear browser cache (or open in private window) to ensure new scripts/styles are loaded.

Notes
-----
- The plugin files include `slideshowpure.js` and `slideshowpure.css` — the script is defensive and will continue to show server metadata/images even if external services (YouTube, SponsorBlock, translation chunks) are unreachable.
- If you want to revert, remove the `SlideshowPure` folder from the `web/extensions` directory and clear the browser cache.

If you want, I can also produce a zip package for easier deployment or add an auto-inject snippet that appends the script to the Jellyfin web client HTML.
