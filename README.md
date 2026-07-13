# Offer Builder

A single-file, mobile-first offer intake tool for buyer's agents. Enter the listing, buyer, terms, and contingencies — get a clean one-page offer summary PDF, a document package, and a prefilled email draft to the listing agent.

Built to be **terms-only**: no buyer personal narrative, no demographic or protected-class detail enters any output.

---

## Use it

**Live:** `https://<username>.github.io/offer-builder/`

No install, no account, no server. Everything runs in your browser.

---

## How it works

**1. Set up your profile once.**
Name, license #, license state and type, brokerage, office address, contact. It saves to your device and prefills your agent details on every offer after that. Optional headshot and team logo appear as a secondary mark — brokerage branding stays dominant.

**2. Build the offer.**
Paste a listing link to prefill (beta), or enter fields manually. Financials calculate as you go:

- **Down payment** — enter % or $, the other fills in
- **Balance due at closing** — auto-calculated, overridable
- **Buyer's broker compensation** — you choose % or flat $ explicitly; nothing is assumed
- **Net to seller** — offer price − seller concession − any compensation asked of the seller. This is the number listing agents actually rank offers on, so it's the number the summary emphasizes.

A **±10% variance warning** fires if your offer price swings hard from list — a typo guard.

**3. Attach documents.**
Slots double as a checklist: Signed Offer, Pre-Approval Letter, Proof of Funds, Escalation Clause Authorization, Lead Paint Disclosure. Files are renamed `Address - Type` automatically. Merge into one PDF if you want.

**4. Send.**
Download the combined package, or open an email draft with the listing agent, subject, and body prefilled. Attach and send from your mail app.

---

## Your profile, three ways

Because this is client-side only, your profile lives with **you**, not on a server:

| Method | What it does |
|---|---|
| **Device** | Saves in this browser automatically. Most convenient. |
| **Copy my link** | Generates a personalized URL with your profile baked in. Bookmark it, or open it on another device. |
| **Export / Import** | Downloads a `profile.json` you can back up or move. |

> **Note on device storage:** iOS Safari clears local site storage after ~7 days without a visit. If you use this occasionally, keep your personalized link bookmarked or hang onto the exported `profile.json`.

---

## Privacy

- **Nothing leaves your browser.** No server, no database, no analytics, no tracking.
- Your profile and offer data stay on your device.
- PDFs are generated locally; the email draft opens in *your* mail client — this tool never sends anything.

---

## Compliance posture

- **Terms-only, agent-authored.** No buyer "love letters." Personal narrative about a buyer invites Fair Housing exposure by surfacing protected characteristics — so the output covers terms, and only terms.
- **Post-2024 NAR settlement language.** Buyer's broker compensation is not set by the listing or the MLS. It's paid to the **brokerage**, not the individual agent, and may be requested from the seller as a term of the offer. The tool words it that way throughout.
- Every output carries an Equal Housing Opportunity mark and a non-binding disclaimer.

The offer summary is a discussion document. It is not a binding offer or contract.

---

## Tech

Single `index.html`. No build step, no dependencies to install. Uses jsPDF and pdf-lib from CDN. Works offline once loaded.

To run locally: download the file and open it in a browser.
