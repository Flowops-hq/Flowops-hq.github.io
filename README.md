# FlowOps site — for Google verification

Two pages. No build step, no framework. Drop them on GitHub Pages and they work.

## Put it online (free, ~5 minutes)

Host it under a GitHub **organization**, not a personal account — the URL then reads
`flowops.github.io` instead of carrying a personal username. Organizations are free.

1. GitHub → **+** → **New organization** → Free plan → name it `flowops`.
2. Inside that organization, create a **public** repo named exactly `flowops.github.io`.
3. Upload everything in this folder — `index.html`, `privacy.html`, and the `assets` folder.
4. Repo → **Settings** → **Pages** → Source: **Deploy from a branch** → Branch: `main`,
   folder `/ (root)` → Save.
5. Wait a minute. Pages are live at:
   - Homepage: `https://flowops.github.io/`
   - Privacy: `https://flowops.github.io/privacy.html`

If the `flowops` organization name is taken, pick the nearest free variant and use the matching
repo name — the repo must always be `<orgname>.github.io`.

If you buy a domain later (flowops.app or similar), point it here in the same Pages settings. The
Google submission is easier to get through with a real domain, but it is not required.

## Then fill in Google

Google Cloud Console → your project → **Google Auth Platform** → **Branding**:

| Field | Value |
|---|---|
| App name | `FlowOps` |
| User support email | your email |
| App logo | upload `assets/flowops-app-icon-512.png` |
| Application home page | the homepage URL above |
| Privacy policy link | the privacy URL above |
| Terms of service | leave blank — not required |
| Authorized domain | `github.io` (or your own domain) |

Then **Audience** → Publish app, and press **Verify branding**.

## Before you submit — three things to change

1. **The support email.** Both pages use `flowopssupport@gmail.com`. Google prefers an
   address on your own domain. A personal Gmail works, but swap it if you get a domain.
2. **Check the claims are still true.** The privacy policy says FlowOps requests only
   `openid`, `email` and `profile`. If that ever changes, the policy has to change with it —
   Google checks the policy against what the app actually asks for.
3. **Read it once yourself.** It is written to describe FlowOps honestly. If anything on it is
   wrong, fix it before it is published.

This is written to pass Google's review and to be honest with users. It is not legal advice, and
before real customer data goes in at scale you should have a lawyer look at it.

## Assets

- `assets/flowops-app-icon-512.png` — square icon for Google. Dark tile so it reads on both the
  light and dark consent screens.
- `assets/flowops-app-icon.svg` — same icon, vector.
- `assets/flowops-mark.svg` — the plain mark, used on the pages.
