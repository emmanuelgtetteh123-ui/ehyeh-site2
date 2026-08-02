# Ehyeh website

A handmade-crochet-bag showcase + WhatsApp shop, with a simple admin panel so the
owner can add, edit, and photograph new bags herself — no code.

## What's in here
- `index.html` — the website
- `admin/` — the content manager (where she edits bags & links)
- `data/` — the content the site reads (`products.json`, `settings.json`)
- `images/` — the logo and bag photos
- `netlify.toml` — tells Netlify to publish the folder as-is

---

## Part 1 — Put it online (one-time, ~10 min)

1. **GitHub** — create a free account at github.com, click **New repository**,
   name it `ehyeh-site`, keep it Public, and create it. On the repo page choose
   **uploading an existing file**, then drag in *everything inside this folder*
   (index.html, admin, data, images, netlify.toml). Commit.

2. **Netlify** — create a free account at netlify.com and sign in with GitHub.
   Click **Add new site → Import an existing project → GitHub**, pick `ehyeh-site`,
   and deploy. No build settings needed — just press deploy. Your site is now live
   at a random address like `random-name.netlify.app`.

3. **Catchy link** — in Netlify go to **Site configuration → Domain management
   → Options → Edit site name** and change it to `ehyeh`. Your link becomes
   **https://ehyeh.netlify.app** — short and clean. (For a `.shop`/`.com` domain,
   see Part 3.)

## Part 2 — Turn on her login (one-time)

4. In Netlify open **Integrations → Identity** (or the **Identity** tab) and click
   **Enable Identity**.
5. Under **Identity → Services**, click **Enable Git Gateway**.
6. Under **Identity → Registration preferences**, set it to **Invite only**.
7. Click **Invite users** and enter her email address.
8. She gets an email, clicks the link, sets a password — done. From then on she
   just visits **ehyeh.netlify.app/admin**, logs in, and edits.

> If your Netlify account doesn't show Identity, tell me and I'll switch the login
> to **DecapBridge** (a free drop-in) — it's a one-line change to `admin/config.yml`.

## Part 3 — A custom domain (optional, ~$12/yr)

Buy `ehyeh.shop` or `ehyeh.com` from Namecheap or Porkbun, then in Netlify go to
**Domain management → Add a domain** and follow the DNS steps. HTTPS is automatic.
Once it's set I can also make you a **QR code** for packaging and cards.

---

## How she adds a new bag (the everyday bit)
1. Go to **ehyeh.netlify.app/admin** and log in.
2. Open **Bags → All bags → add an item**.
3. Type the name, price, and a short description; upload the photo; tick
   **Show in slideshow** if she wants it featured; tick **Sold out** when it's gone.
4. Click **Publish**. The site updates itself in about a minute.

To change the WhatsApp number or add Instagram/TikTok/Facebook links, open
**Settings → Contact & links**.

## A note on previewing
Because the site now loads its photos and prices from the `data` and `images`
folders, opening `index.html` by double-clicking won't show them (browsers block
that for local files). It looks perfect once it's on Netlify. To preview on your
own computer, run `python3 -m http.server` inside this folder and open
`http://localhost:8000`.
