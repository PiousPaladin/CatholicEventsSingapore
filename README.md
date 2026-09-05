# Catholic Events Singapore

An unofficial community calendar of Catholic events in Singapore.

The whole site is one file: `index.html`. It loads nothing from anywhere — no scripts,
stylesheets, fonts or images from other servers — so it works offline, and it works on any
static host without configuration.

## Putting it online with a free GitHub account

1. Sign in at **github.com** and click **New repository** (the **+** at the top right).
2. Name it whatever you like — for example `catholic-events`. Set it to **Public**.
   GitHub Pages is only free on public repositories. Do not tick "Add a README".
   Click **Create repository**.
3. On the empty repository page, click **uploading an existing file**.
4. Drag in **`index.html`** and **`.nojekyll`** (this README is optional).
   `.nojekyll` is an empty file that tells GitHub not to run its blog engine over the site —
   harmless here, but it avoids surprises later.
   If your computer hides files beginning with a dot, press **Cmd+Shift+.** on a Mac or turn on
   **Hidden items** in the Windows Explorer View menu.
5. Click **Commit changes**.
6. Go to **Settings → Pages** (left-hand menu). Under **Build and deployment**, set
   **Source** to *Deploy from a branch*, **Branch** to `main` and the folder to `/ (root)`.
   Click **Save**.
7. Wait a minute or two, then reload that page. It will show:
   **`https://<your-username>.github.io/catholic-events/`**
   That is your website. Anyone with the link can open it.

The first publish sometimes takes up to ten minutes. If you get a 404, wait and reload before
changing anything.

## Updating it each week

Open the repository, click `index.html`, then the **pencil** icon → **Delete this file** →
commit, and upload the new one. Or simpler: on the repository's main page use
**Add file → Upload files**, drop in the new `index.html`, and GitHub will replace it.
The live site updates a minute or so later.

Nothing else needs doing. There is no build step and no server.

## A few things worth knowing

- **It is free, permanently.** GitHub Pages on a public repository costs nothing and has no
  traffic limit that a site like this would ever approach.
- **The countdown badges keep working.** "Today" and "In 3 days" are worked out in each
  reader's own browser from their device's clock, not baked into the file, so they never go
  stale and they cost nothing to host.
- **The link preview.** When the address is shared on WhatsApp, Telegram or Slack it shows
  *Catholic Events Singapore* and a one-line description. There is deliberately no preview
  image: an image would have to be a separate file at a fixed web address, and that would break
  the promise that this page depends on nothing. If you later decide you want a picture in the
  preview, add an image to the repository and I will point the page at it.
- **Your own domain, if you ever want one.** Buy a domain, add a `CNAME` file to the repository
  containing just the domain name, and point the domain's DNS at GitHub. The site itself does
  not change.
- **Everything is public**, including the repository's history. There is nothing private in
  this file, but do not commit anything you would not publish.

## Turning on visitor counting

The page ships with counting **off** — it requests nothing from anywhere until you configure it.
Open `index.html`, find `const ANALYTICS` (search for "counting visits"), and fill in one line.

**Cloudflare** — free, no cookies, no consent banner. Visits, when, country, device, referrer.

1. Sign in at dash.cloudflare.com → **Analytics & Logs → Web Analytics → Add a site**.
2. Enter your GitHub Pages address. It gives you a **token**.
3. Paste it: `provider: "cloudflare"`, `token: "your-token-here"`.

**Umami** — free tier, also cookieless, and additionally measures how long people stay and which
organisers draw interest.

1. Create an account at umami.is, add the site, copy the **website id**.
2. Paste it: `provider: "umami"`, `websiteId: "your-id-here"`.

Set `provider: ""` to switch counting off again.

The footer's privacy note rewrites itself to match whichever provider is on, so it never claims
more than is actually counted. Nothing about a listing is ever sent — interest is recorded at the
level of the organiser only, and searches are never recorded.

**Keeping history.** Both dashboards discard old data eventually. If you want a permanent record,
export the monthly summary as CSV and commit it to this repository — that costs nothing and the
history is then yours regardless of which tool you use.

## Feedback

The page carries **catholiceventssg@gmail.com** in its footer and in the "Where this comes
from" panel, for readers to send corrections and events.
