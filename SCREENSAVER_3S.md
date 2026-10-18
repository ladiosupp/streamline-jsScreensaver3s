# Screensaver 3s

This repository is a copy of [decentespresso/streamline-js](https://github.com/decentespresso/streamline-js) with one behavioral change:

- **Screensaver unlock:** press and hold for 3 seconds instead of tapping.
- A progress ring is drawn around the press point and fills over the three seconds.
- Releasing early, dragging away, or a second pointer cancels the unlock.
- Everything else is unchanged from upstream.

The screensaver is the wallpaper shown when the DE1 sleeps. The hold is handled in `src/modules/ui.js`; a plugin's screensaver button remains a separate tap target and does not start the hold.

Upstream is GPL-3.0-or-later; this copy keeps the same license.
