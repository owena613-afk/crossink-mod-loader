# CrossInk Mod Loader

Open the page: https://owena613-afk.github.io/crossink-mod-loader/

One page for CrossInk mods on the Xteink X4 and X4 Pro:

- **Build firmware:** pick mods, readers and languages, and start a build in your builder repository. You need a GitHub fine-grained access token with *Actions: Read and write* for that repository. The token is kept only in your browser and is sent only to GitHub.
- **Flash a reader (USB):** in Chrome or Edge, plug a reader in and flash a build's zip (or a single `.bin`) straight from the page. It writes only the firmware slot the reader already starts from and checks every byte; books, progress and settings on the SD card aren't touched. Uses [esptool-js](https://github.com/espressif/esptool-js) (Apache 2.0, copy in `vendor/`).
- **Reader settings (SD card):** edit a reader's `/.crosspoint/mods/settings.json` with switches, then copy it back to the card.

The page is a single file (plus the flashing library in `vendor/`) with no server and no tracking.
