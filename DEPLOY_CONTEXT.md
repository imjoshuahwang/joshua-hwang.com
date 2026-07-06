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

## Current deployment status

Completed:
- GitHub repository created: `https://github.com/imjoshuahwang/joshua-hwang.com`
- Site files pushed to GitHub on `main`
- Vercel project created: `joshua-hwang-com`
- Vercel production deployment is live:
  - `https://joshua-hwang-com.vercel.app`
  - deployment URL: `https://joshua-hwang-h9j45iu0f-imjoshuahwang-7950s-projects.vercel.app`
- `joshua-hwang.com` and `www.joshua-hwang.com` were added to the Vercel project.

Remaining:
- DNS at Spaceship must be changed. The domain currently uses:
  - `launch1.spaceship.net`
  - `launch2.spaceship.net`

Vercel says the current domain DNS is invalid because the apex still resolves to:
- `54.149.79.189`
- `34.216.117.25`

## Required DNS records

At Spaceship, either switch nameservers to Vercel:

```text
ns1.vercel-dns.com
ns2.vercel-dns.com
```

Or keep Spaceship DNS and set these records:

```text
A      @    216.198.79.1
A      @    64.29.17.1
CNAME  www  6ae4d9d5121518cd.vercel-dns-017.com.
```

After DNS propagates, run:

```text
npx vercel domains verify joshua-hwang.com
npx vercel domains verify www.joshua-hwang.com
```

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
