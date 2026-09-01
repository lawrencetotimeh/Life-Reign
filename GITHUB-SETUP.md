# Getting this onto GitHub

The repo is already created: **github.com/lawrencetotimeh/Life-Reign** (empty, no README/.gitignore/license — correct).

This folder is already a local git repo with its commit history (initial build, copy revision, this file). To push it up:

1. Unzip `LifeReign-website-v2.zip` somewhere on your Mac if you haven't already.
2. Open Terminal, `cd` into the unzipped folder.
3. Run:

```
git remote add origin https://github.com/lawrencetotimeh/Life-Reign.git
git branch -M main
git push -u origin main
```

On that last command, Git will likely pop open a browser window asking you to log into GitHub (your normal login, not a token you type in) — approve it and the push continues automatically. If it instead asks for a username/password in the terminal, don't type your GitHub password; GitHub no longer accepts that. Either create a Personal Access Token at github.com/settings/tokens (classic, "repo" scope) and paste that in as the password, or install GitHub Desktop and use it to do the push visually instead.

That's it — your full commit history goes up with it.

## Connecting to Netlify afterward

Once it's on GitHub: log into Netlify, "Add new site" → "Import an existing project" → pick this repo. Leave the build command blank and set the publish directory to `/` (this is a plain static site, no build step). Netlify will give you a `*.netlify.app` URL immediately; point lifereigndc.org at it once the domain is purchased (Netlify's DNS instructions will give you the exact records to add in GoDaddy).
