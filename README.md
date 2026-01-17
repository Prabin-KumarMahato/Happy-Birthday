# Deploy to Vercel (Static Site)

This project is a static site located in the `aqsa/` folder (index.html + style.css + images).

## Option A: Deploy via Vercel CLI

1. Log in to Vercel (opens a browser for auth):

```bat
cd "c:\Users\Pravin Mahato\OneDrive\Desktop\card\aqsa"
vercel login
```

Follow the browser prompt to authorize, then return to the terminal.

2. Create and deploy a preview build:

```bat
vercel
```

- Answer prompts (default answers are fine for a static site).
- This returns a preview URL (e.g. https://your-project.vercel.app).

3. Deploy to production (stable URL):

```bat
vercel --prod
```

## Option B: Deploy via GitHub Import

1. Initialize a Git repo (if not already):

```bat
cd "c:\Users\Pravin Mahato\OneDrive\Desktop\card\aqsa"
git init
git add .
git commit -m "Initial commit"
```

2. Push to a new GitHub repository.

3. Visit https://vercel.com/new and import the repo.

- Framework preset: "Other" or "Static Site"
- Root directory: `aqsa` if the repo has multiple folders.
- No build command needed; Vercel serves static files automatically.

## Notes

- For simple static sites, no `vercel.json` is required. If you need custom redirects or headers later, add a `vercel.json`.
- Local preview (optional):

```bat
python -m http.server 5500
```

Then open http://127.0.0.1:5500/index.html
