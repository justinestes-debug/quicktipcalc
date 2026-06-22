# Mission: Tip Calculator Web App
Your job is to build a standalone Tip Calculator that captures a portion of the 3M+ monthly searches for this keyword.

## Phase 1: Build & Design
1. Generate a brand name and register an available domain (via Namecheap API or prompt owner to buy).
2. Write `index.html`, `style.css`, and `app.js`.
3. Features: Instant calculation, split bill by N people, custom tip %, round up/down buttons, mobile-first UI.
4. Integrate Google AdSense placeholders and an affiliate link section (e.g., "Best Travel Credit Cards").

## Phase 2: Deployment
1. Initialize a Git repository.
2. Push code to a private GitHub repo.
3. Deploy to Vercel using the Vercel CLI (`vercel --prod`).

## Phase 3: Ongoing Maintenance (Cron Jobs)
- **Weekly (Monday 9am):** Run Google Lighthouse API. If performance drops below 95, optimize the code and push a fix.
- **Monthly (1st of month):** Use web search to analyze top 3 competitors for "tip calculator". If they added a new feature, write the code to add it to our site, create a PR, and notify the owner.
- **Daily:** Check Vercel deployment status. Alert owner if down.
