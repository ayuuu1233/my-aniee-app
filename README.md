# Anime Recommendation — Single-file Web App

Unique + fun — recruiters love APIs. This repo contains a single-file demo (index.html) that lets you:
- Search anime (AniList GraphQL)
- Get mood-based recommendations (mood → genres mapping)
- Save favourites (localStorage)
- Responsive UI suitable for quick demos / portfolio

Live demo
- Deployed: https://your-live-demo-url.example  ← Replace this with your deployed URL

Screenshots
- Home / Search — `./screenshots/home.png`
- Mood recommendations — `./screenshots/mood.png`
- Favorites — `./screenshots/favorites.png`

(Place your screenshots in the repository `screenshots/` folder with the file names above. Example:)
![Home screenshot](./screenshots/home.png)

Features
- Search anime by title (uses AniList GraphQL)
- Mood-based recommendations (energetic, calm, funny, melancholic, mysterious)
- Save / remove favourites persisted to localStorage
- Minimal, responsive UI (single-file: index.html) — great for quick demos or embedding in a portfolio
- No backend required (but a server proxy or proper auth is recommended for production)

Files
- index.html — single-file app (HTML, CSS, JS)
- screenshots/ — put screenshot images here for README & portfolio

Quick start (local)
1. Clone the repo:
   git clone https://github.com/ayuuu1233/my-aniee-app.git
   cd my-aniee-app

2. Open locally:
   - Option A (quick): double-click index.html or open it in the browser
   - Option B (recommended to avoid some browser fetch restrictions): run a simple static server
     - Python 3: python -m http.server 8000
     - Node (http-server): npx http-server -p 8000
     Then open http://localhost:8000

Notes on the AniList API
- The app queries AniList GraphQL at https://graphql.anilist.co.
- For demo purposes the app makes requests directly from the browser; AniList allows basic queries without an API key.
- For production use consider proxying requests through your own API route (to avoid CORS/rate limits and to support authenticated endpoints).

Deploy / Live demo
Option A — Vercel (recommended for single-file and Next/static sites)
1. Go to https://vercel.com/new
2. Import this GitHub repo (ayuuu1233/my-aniee-app)
3. Set the root to the repo, choose "Framework Preset: Other", and deploy.
4. After deploy, copy the Live demo URL and replace the placeholder above.

Option B — GitHub Pages (single-file)
1. Commit `index.html` to the `main` branch.
2. In the repo settings → Pages → Source choose `main` branch and root (/) and save.
3. Wait a minute; your site will be available at https://ayuuu1233.github.io/my-aniee-app/
4. Copy that URL into the Live demo link above.

Option C — Netlify
1. Drag & drop the repo or index.html to Netlify, or connect the GitHub repo and deploy.
2. Copy the provided URL.

Customising README screenshots & live link
- Add your screenshots to `./screenshots/` using the filenames listed above.
- Update the "Live demo" URL in this README to the deployed URL.

Suggested next steps
- Add authentication + persistent favourites (Supabase, Firebase, or a small server and DB) so users can save favourites cross-device
- Improve UI/UX with Tailwind, Chakra UI, or Material UI
- Add pagination, caching, and error handling
- Add unit / integration tests and CI (GitHub Actions)

License
- MIT — feel free to use and customize this for your portfolio.

If you want, I can:
- Create the screenshots placeholders for you,
- Add a GitHub Pages workflow or GitHub Action to automatically deploy on push,
- Or open a PR with a prettier README or extra docs (just tell me which).
