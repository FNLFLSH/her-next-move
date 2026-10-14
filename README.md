# Her Next Move ♡
A mobile-friendly real-estate job finder. Search, filter, save jobs locally, and click through to legitimate job sources. No account needed for visitors.

## Put it online
1. Upload this folder to a new GitHub repository (or push its contents).
2. Visit https://vercel.com/new and import that repository. Framework preset: **Other**. Root directory: repository root.
3. Get Adzuna credentials at https://developer.adzuna.com/ and set these **Vercel Project → Settings → Environment Variables**:
   - `ADZUNA_APP_ID` (your App ID)
   - `ADZUNA_APP_KEY` (your API key)
4. Deploy (or Redeploy after adding credentials). Copy the public `.vercel.app` link and text it to her.
5. Test the site on a phone and verify several jobs/apply links before sharing.

If you deploy before adding credentials, the site still works and offers links to live Indeed, LinkedIn, and Google searches, but **does not pretend to display real postings**. Saves are stored in the visitor's browser only, not synced between devices. Results refresh on each search and have a short server-side cache. No automatic morning emails are included in this first version.

## Notes
- The backend uses Adzuna's job-search endpoint; your API key is never sent to visitors' browsers.
- API results can be imperfect. Labels are informational, not guarantees of eligibility, licensing, part-time hours, or pay.
- No scraping or bypassing job-board access controls. Respect API rate limits and terms.
- Default location is Atlanta, GA, but visitors may change it. Adjust `value="Atlanta, GA"` in `index.html` to change the default.
