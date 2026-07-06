# joshua-hwang.com deployment context

This folder is a complete static personal website.

Entry point:
- `index.html`

Important files:
- `style.css`
- `venn.html`
- `model-un.html`
- `shua.html`
- `photos.html`
- `essays.html`
- `goals.html`
- `assets/`

There is no build step, no package manager, no framework, and no server code.

## Desired deployment

Deploy the contents of this folder to `joshua-hwang.com`.

## GitHub setup

Create a GitHub repository, for example:

```text
joshua-hwang.com
```

Copy every file in this folder into the repository root, so `index.html` is at the root:

```text
index.html
style.css
venn.html
model-un.html
shua.html
photos.html
essays.html
goals.html
assets/
DEPLOY_CONTEXT.md
```

Commit and push.

## Vercel setup

Use Vercel as a static site host.

1. Import the GitHub repository into Vercel.
2. Framework preset: `Other`.
3. Build command: leave blank.
4. Output directory: leave blank or use `.`.
5. Root directory: repository root.
6. Deploy.
7. Add the custom domain `joshua-hwang.com`.
8. Follow Vercel's DNS instructions at the domain registrar.

Because this is a plain static site, Vercel should serve `index.html` directly.

## GitHub Pages alternative

If using GitHub Pages instead of Vercel:

1. Put this folder's contents at the repo root.
2. In GitHub, go to repository settings.
3. Enable Pages from the main branch root.
4. Add a `CNAME` file containing:

```text
joshua-hwang.com
```

5. Configure DNS at the registrar for GitHub Pages.

## Notes

- Do not move `assets/` unless all image and PDF paths are updated.
- The site uses relative links, so it works from the domain root.
- The public links intentionally point to:
  - `https://joinvenn.org/`
  - `https://kaerune.com/`
- The essay PDFs are local assets:
  - `assets/claude-my-baby.pdf`
  - `assets/bitch-be-gentle-monster.pdf`
