# MaxTrade redirect page

A tiny static page that sends visitors to MaxTrade. The link to this page never changes.
When your server's IP or address changes, you edit ONE line in `config.json`.

## Set up (once)
1. Create a new GitHub repository (for example `maxtrade`) and upload all files in this folder.
2. Repo **Settings → Pages → Build and deployment**: Source = "Deploy from a branch",
   Branch = `main`, Folder = `/ (root)`. Save.
3. After a minute your link is ready: `https://YOUR-USERNAME.github.io/maxtrade/`

## When the address changes
1. Open `config.json` in GitHub, tap the pencil (edit).
2. Change the url, for example:
   ```json
   { "url": "http://123.45.67.89:3000" }
   ```
3. Commit. The page picks up the new address on the next visit (GitHub can take 1–2 minutes).

## Notes
- Use the full address with `http://` or `https://` and the port if there is one.
- `404.html` is a copy of `index.html`, so a wrong sub-link on your page still redirects.
- Visitors see a "Continue" button after 4 seconds if the automatic redirect is blocked.
