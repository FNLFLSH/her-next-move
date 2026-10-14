# Her Next Move ♡
A mobile-friendly finder for internships and entry-level roles in marketing, business, client experience, HR and retail brands. Search, filter, save jobs locally, and click through to legitimate job sources. No account needed for visitors.

## Put it online
1. Upload this folder to a new GitHub repository (or push its contents).
2. Visit https://vercel.com/new and import that repository. Framework preset: **Other**. Root directory: repository root.
3. No credentials are needed: listings come from The Muse's free public API (https://www.themuse.com/developers/api/v2). Optionally set `MUSE_API_KEY` in **Vercel Project → Settings → Environment Variables** to raise the rate limit from 500 to 3600 requests/hour.
4. Deploy. Copy the public `.vercel.app` link and text it to her.
5. Test the site on a phone and verify several jobs/apply links before sharing.

Real estate has no live feed on The Muse, so that category links out to live Indeed, LinkedIn, and Google searches instead. Saves are stored in the visitor's browser only, not synced between devices. Results refresh on each search and have a short server-side cache. No automatic morning emails are included in this first version.

## Notes
- The backend proxies The Muse's jobs endpoint and caches results for 30 minutes. Searches cover the chosen city plus remote roles; locations must be written like `Atlanta, GA`.
- API results can be imperfect. Labels are informational, not guarantees of eligibility, licensing, part-time hours, or pay.
- No scraping or bypassing job-board access controls. Respect API rate limits and terms.
- Default location is Atlanta, GA, but visitors may change it. Adjust `value="Atlanta, GA"` in `index.html` to change the default.
