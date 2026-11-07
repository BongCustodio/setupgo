# SetupGo website — setup guide

## 1. Fill in your settings
Open `index.html`. Near the top, find the block that starts with `window.SETUPGO` and add your links:

| Setting | What to paste | Result on the site |
|---|---|---|
| `facebookPage` | Your Page link, e.g. `https://www.facebook.com/setupgodigital` | Live Facebook feed in the Connect section, plus a Messenger link |
| `youtubeChannel` | Your channel link, e.g. `https://www.youtube.com/@setupgo` | "Open channel" button goes to your channel |
| `youtubeVideoId` | The code after `v=` in a video link | Your video plays inside the page (loads only when clicked, so the page stays fast) |
| `googleProfile` | Your Google Business Profile or review link | "Find on Google" button |
| `formspreeId` | Your form ID from formspree.io | Support requests and ad submissions arrive in your email |

Leave any value as `""` and the site shows a simple link instead.

## 2. Set up Formspree (free)
1. Sign up at https://formspree.io with bcustodio2767@gmail.com.
2. Create a new form. Copy the ID at the end of its URL (`https://formspree.io/f/xqkrnaby` → `xqkrnaby`).
3. Paste it as `formspreeId`.

## 3. Manage ad listings
Ads that pass the screening are emailed to you. They are **not** published automatically.
To approve one, add it to `listings.json`:

```json
{ "title": "Product name", "category": "Industrial software", "description": "One sentence." }
```

Delete the two entries marked `"example": true` once you have real partners.

## 4. Publish on GitHub Pages
1. Create a repository, e.g. `setupgo-site`.
2. Upload `index.html`, `listings.json` and `.nojekyll`.
3. Go to Settings → Pages → Source: *Deploy from a branch* → `main` / root → Save.
4. The site goes live at `https://<your-username>.github.io/setupgo-site/` in about a minute.

To use your own domain (e.g. `setupgo.ph`), add it under Settings → Pages → Custom domain.

GitLab works the same way: upload the files and enable Pages for the project.
