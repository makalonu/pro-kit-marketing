# Social-media-content-website

Simple single-page static demo site (one `index.html`) for a contractor marketing kit.

## What this repo is

- A static HTML page using Tailwind via CDN and a small client-side script.
- There is no build system or bundler configured.

## Preview locally (macOS / zsh)

Option A — Open directly in your browser (quick):

```bash
open index.html
```

Option B — Simple static server (recommended for proper fetch/XHR behavior):

```bash
# Python 3 built-in server
python3 -m http.server 8000
# then open: http://localhost:8000
```

Option C — One-off Node server with npx:

```bash
npx http-server -p 8000
# or
npx serve -s . -l 8000
```

Option D — Add an npm dev script (optional):

```bash
npm init -y
npm install --save-dev live-server
# add to package.json: "start": "live-server --port=3000"
npm run start
```

## Build

There is no build step required to run this project as-is. If you later add Tailwind compilation or JS bundling, you can add a standard npm toolchain (Tailwind CLI, esbuild, webpack, etc.). I can scaffold that for you if desired.

## Security note — API keys

The page contains client-side code that will call an external content-generation API. Do NOT store any secret API key in client-side JavaScript — it will be public. Instead, create a server-side proxy or serverless function that keeps the key secret and forwards requests from the client.

## Deployment

- GitHub Pages: enable Pages from the `main` branch, root folder.
- Netlify / Vercel: connect the repository and deploy — both handle static sites automatically.
- Any static host (S3 + CloudFront, Firebase Hosting, etc.) will work.

## Next steps (optional)

- I can scaffold an npm dev setup (package.json + start/build scripts).
- I can implement a tiny Express server or serverless function to proxy the API securely.

If you want one of those, tell me which and I'll add it.
