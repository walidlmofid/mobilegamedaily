# MobileGameDaily.com

Your curated mobile game discovery site — powered by TikTok, linked to official stores.

## 🚀 Deploy to Netlify

1. Push this folder to a GitHub repo
2. Go to [netlify.com](https://netlify.com) → "Add new site" → "Import from Git"
3. Select your repo, leave build settings as default
4. Click "Deploy"
5. In Netlify → Domain settings → Add custom domain → `mobilegamedaily.com`

## 🎮 Adding / Editing Games

All games live in **`games.json`**. Each game object looks like this:

```json
{
  "id": "unique-slug",
  "title": "Game Name",
  "developer": "Developer Name",
  "genre": "Action/FPS",
  "rating": 4.5,
  "size": "2.4 GB",
  "platforms": ["Android", "iOS"],
  "image": "https://url-to-game-icon-or-banner.jpg",
  "description": "A short description of the game.",
  "features": ["Feature 1", "Feature 2", "Feature 3", "Feature 4"],
  "playStoreUrl": "https://play.google.com/store/apps/details?id=com.example.game",
  "appStoreUrl": "https://apps.apple.com/app/game-name/id123456789",
  "featured": true
}
```

### Field guide:
- **id**: URL-friendly slug (lowercase, hyphens)
- **featured**: Set `true` to show in the "Featured" section at the top
- **image**: Use the game icon URL from Google Play (right-click icon → copy image URL)
- **playStoreUrl / appStoreUrl**: The official store links. Remove the field if not available on that platform
- **platforms**: `["Android"]`, `["iOS"]`, or `["Android", "iOS"]`

### To add a new game:
1. Open `games.json`
2. Copy an existing game block
3. Update all fields
4. Commit & push — Netlify auto-deploys!

## 📱 Customization

- **TikTok link**: Search for `YOURTIKTOK` in `index.html` and replace with your handle
- **Colors**: Edit CSS variables at the top of `index.html` (`:root` block)
- **Logo**: Change the emoji in `.logo-icon` or replace with an `<img>` tag

## 📁 File Structure

```
├── index.html      ← The entire website (single file)
├── games.json      ← Your game data (edit this!)
├── netlify.toml    ← Netlify config
└── README.md       ← This file
```
