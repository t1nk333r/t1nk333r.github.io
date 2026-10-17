# t1nk333r.github.io

Where widget links from my Omalauncher build land:

- `w/` — the share page. A link is `https://t1nk333r.github.io/w#owl1.<data>`: the widget file,
  compressed, after the `#`, so it never reaches the server. The page unpacks it in the browser,
  shows the file, and opens it in the launcher. `#dpaste.<id>` links are widgets too big for one
  QR code, uploaded to dpaste.com.
- `.well-known/assetlinks.json` — lets Android open these links straight in the launcher
  (`dev.omalauncher`, signed with my key) without going through the browser.

The same repo deploys to Cloudflare Pages as `https://share.aloqaili.xyz/w`, the backup: a push
updates both. (A copy on my Feather server, which only answers at home and on Tailscale, has to be
copied there by hand.)

`w/index.html` is adapted from Simon Schubert's share page in
[omarchy-widgets](https://github.com/SimonSchubert/omarchy-widgets) under the MIT license (see
`LICENSE`); the launcher link and the import command use whichever host serves the copy.
