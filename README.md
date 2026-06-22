# 💸 TipClaw — Tip Calculator Web App

A clean, mobile-first tip calculator built as a single `index.html` file. No dependencies, no build step, no backend.

---

## 🌐 Domain Name Suggestions

| Domain | Notes |
|---|---|
| **quicktipcalc.com** | Memorable, descriptive, already in canonical tag. Checks all SEO boxes. |
| **splittip.app** | Short, modern `.app` TLD. Great for mobile-first audience. |
| **tipmate.io** | Friendly, brandable, dev-adjacent TLD. Easy to remember after a dinner out. |

---

## 🚀 Deploy to Vercel (Free, ~3 minutes)

### Prerequisites
- A [Vercel account](https://vercel.com) (free tier works perfectly)
- Git installed locally

### Step-by-Step

1. **Create a GitHub repo**
   ```bash
   cd utility-agents/tipclaw
   git init
   git add index.html README.md
   git commit -m "Initial TipClaw build"
   gh repo create tipclaw --public --push --source=.
   # (or use GitHub web UI to create a repo and push manually)
   ```

2. **Import to Vercel**
   - Go to [vercel.com/new](https://vercel.com/new)
   - Click **"Import Git Repository"**
   - Select your `tipclaw` repo
   - Framework Preset: **Other** (static)
   - Root Directory: leave as-is (or set to `utility-agents/tipclaw` if repo root is workspace)
   - Click **Deploy**

3. **Set your custom domain**
   - In the Vercel dashboard → Project → **Settings → Domains**
   - Add your domain (e.g. `quicktipcalc.com`)
   - Point your DNS to Vercel's nameservers or add the provided CNAME/A record
   - Vercel provisions a free TLS certificate automatically

4. **Update the canonical URL**
   - Edit `index.html`, find the `<link rel="canonical">` tag
   - Replace `https://quicktipcalc.com` with your actual domain
   - Commit and push — Vercel auto-deploys on every push

5. **Verify deployment**
   ```bash
   curl -I https://your-domain.com
   # Should return HTTP/2 200
   ```

### Vercel CLI (alternative)
```bash
npm i -g vercel
cd utility-agents/tipclaw
vercel --prod
```

---

## 💰 Monetization Notes

### Google AdSense

Two AdSense placeholder `<div>` blocks are included as HTML comments in `index.html`:

1. **Above the fold** — directly below `<body>`, before the header. High CPM placement.
2. **Below the calculator** — between the Reset button and the affiliate section.

**To activate:**
1. Apply at [adsense.google.com](https://adsense.google.com)
2. Wait for approval (usually 1–2 weeks for new sites)
3. Uncomment the `<ins class="adsbygoogle">` blocks in `index.html`
4. Replace `ca-pub-XXXXXXXXXXXXXXXXX` with your Publisher ID
5. Replace `data-ad-slot` values with your specific Ad Unit IDs
6. Add the AdSense script tag to `<head>`:
   ```html
   <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-XXXXXXXXXXXXXXXXX" crossorigin="anonymous"></script>
   ```

**Expected CPM:** Tip calculators in personal-finance adjacent niches typically earn $3–$8 CPM. Traffic from "tip calculator" searches converts well.

### Affiliate Cards Section

The bottom of the page includes a **"Best Credit Cards for Dining & Travel"** section with three placeholder affiliate links:

| Card | Replace `href` with |
|---|---|
| Chase Sapphire Preferred® | Your Chase affiliate link (via CreditCards.com, NerdWallet, or direct) |
| American Express® Gold Card | Your Amex affiliate link |
| Capital One Savor Cash Rewards | Your Capital One affiliate link |

**Affiliate networks to join:**
- [CreditCards.com Affiliate Program](https://www.creditcards.com/affiliates/)
- [NerdWallet Partner Program](https://www.nerdwallet.com/l/partner-affiliate)
- [FlexOffers](https://www.flexoffers.com) — aggregator with all major card issuers
- [Commission Junction (CJ)](https://www.cj.com) — Chase and Amex both use CJ

**Earnings:** Credit card affiliate commissions typically range from **$50–$200 per approved application**. Even modest traffic (1,000 visitors/month) can generate meaningful income.

### SEO Tips
- Submit `index.html` to Google Search Console after deploying
- Target keywords: "tip calculator", "restaurant tip calculator", "how much to tip"
- Build a few backlinks from Reddit (r/personalfinance) or resource pages
- Page loads instantly (no JS frameworks) — Core Web Vitals will be excellent

---

## 🛠 Tech Stack

- **HTML5** — semantic, accessible markup
- **Tailwind CSS** — via CDN, zero build step
- **Vanilla JavaScript** — no frameworks, no dependencies
- **Single file** — `index.html` is the entire app

## 📋 Features

- Bill amount input with `$` prefix
- Tip presets: 15%, 18%, 20%, 25%
- Custom tip % input field
- Tip % slider (0–50%)
- Split bill: 1–20 people with +/− buttons and direct input
- Real-time calculation on every keystroke
- Round Up / Round Down per-person total
- Reset button
- Mobile-first responsive design
- Emerald green accent color (#10B981)
- AdSense placeholder divs (commented out)
- Affiliate credit card section with disclaimer
- Full SEO meta tags + Open Graph + canonical URL
