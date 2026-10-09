# POP OS — Demo

A one-page demo of POP OS, POP Funding Inc.'s operating system for business funding. Every business, person and number in it is fictional.

The whole demo is one file, `index.html`. It has no build step, no server and no database.

## Signing in

The demo opens on the POP sign-in screen with the floating 3D Pop logo. Drag the logo to spin it.

Tap **Info** for the demo accounts, or type one in. The password for all of them is `demo123`.

| Account | Email |
| --- | --- |
| Sofia Alvarez, Sales | sofia@pop.demo |
| Jack Rivera, Admin | jack@pop.demo |
| Tyler Brooks, Sales | tyler@pop.demo |

When you sign in, the camera flies through the "o" of the logo into the Command center. You stay signed in until you close the tab. **Sign out** is in the yellow demo banner. These accounts only unlock the demo screens. Nothing is checked against a server.

## What's in it

- **Screens:** My work, Command center, Pipeline, Merchants, Funded deals, Providers, Offer workbench, Underwriting check, Team, New file, Status, plus sample application, deal and merchant pages.
- **Live calculators:** the Offer workbench (payment, payback, fees, APR estimate, all terms) and the Underwriting check (POP risk score, tier, payment capacity, max approvals, starting offers) calculate as you type.
- **Phone layout:** a slim top bar, and wide tables become cards.
- **Not live in this demo:** saving records, sign-in, and the other buttons. Those need the full app with its database.

## Put it on Vercel

1. Put `index.html` (and this README) at the **top level** of a GitHub repo, not in a folder. The file must be named exactly `index.html`, or the main address shows a 404.
2. In Vercel: **Add New → Project**, then import that repo.
3. Under **Build & Deployment**, set:
   - **Framework Preset:** Other
   - **Build Command:** leave empty
   - **Output Directory:** leave empty
   - **Root Directory:** leave as the repo root (`./`)
4. Click **Deploy**. When the deployment says **Ready**, the project address (for example `pop-os-11.vercel.app`) shows the demo.

If you see "404 NOT_FOUND" afterwards, check those four steps again. The usual cause is a misnamed file, a file inside a folder, or a framework preset other than Other.

## Open it without Vercel

Download `index.html` and open it in Safari or Chrome. The 3D logo loads from the internet (cdnjs). Offline, a flat version of the logo is used instead, and the rest works.

## Notes

- Pricing and risk scoring use POP's default tables: factor rates by term and tier, tier cutoffs A 740 / B 680 / C 620 / D 560, and a maximum daily payment of 8% of daily revenue plus 0.5% of average daily balance, capped at 12%.
- The APR shown is an estimate. Required state disclosures must come from the disclosure module, not from this demo.
