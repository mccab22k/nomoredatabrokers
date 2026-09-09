# No More Data Brokers

**Take your data back. It's yours.**

No More Data Brokers is a free, open-source, local-only tool for systematically opting out of data brokers without paying for a removal subscription.

## What this does

- Tracks removal progress across 28+ data brokers, tiered by priority
- Links directly to broker opt-out, claim, and privacy-request routes
- Stores **multiple email addresses, phone numbers, and previous cities** in your local profile
- Keeps employer information optional
- Migrates older single-email / single-phone saved profiles automatically
- Provides a **form clipboard** so external privacy forms are faster to complete
- Provides an **email removal queue** for brokers with documented privacy addresses, generating a separate pre-filled request for each broker
- Flags removals that need to be rechecked after broker-specific intervals
- Includes B2B brokers such as ZoomInfo, Apollo, Lusha, Hunter, and Snov.io
- Includes the California DROP portal for registered data brokers

**No account. No server. No profile data leaves your browser.** Profile and progress state are stored only in browser `localStorage`.

## Current notable routes

- **Acxiom:** OneTrust privacy request portal
- **BeenVerified:** direct opt-out search; if verification fails, the app provides a pre-filled fallback request to `privacy@beenverified.com`
- **Hunter:** preferred Claim workflow, with `privacy@hunter.io` as an alternative privacy-rights contact
- **Snov.io:** privacy/deletion route plus documented `help@snov.io` and `snovio_dpo@snov.io` contacts

The app deliberately does not attempt to inject profile data into third-party sites. Cross-origin browser protections make that unreliable and unsafe for a static site. Instead, saved local values are exposed through one-click copy controls.

## Usage

Open `index.html` directly in a browser or use the hosted version:

https://mccab22k.github.io/nomoredatabrokers

No build step, dependencies, account, or backend are required.

```bash
git clone https://github.com/mccab22k/nomoredatabrokers
open nomoredatabrokers/index.html
```

## Broker tiers

| Tier | What they are | Why hit them first |
|---|---|---|
| **1** | Acxiom, LexisNexis, Spokeo, Whitepages, BeenVerified | Feeder / high-value consumer brokers |
| **2** | ZoomInfo, Apollo.io, Lusha, RocketReach, Hunter, Snov.io | B2B professional brokers selling work identity and contact data |
| **3** | Radaris, TruthFinder, Instant Checkmate, US Search | Consumer people-search sites |
| **4** | Epsilon, CoreLogic, Neustar, Datalogix | Advertising and data-enrichment networks |

## Privacy model

Profile data may include:

- Name and former name / alias
- Current city
- Any number of previous cities
- Any number of personal, work, or other email addresses
- Any number of phone numbers
- Optional current and previous employer

All of this stays in `localStorage`. The app contains a profile-only delete control and a full local-data delete control.

## Email requests

The Email Requests tab only lists brokers for which a privacy email is explicitly configured. Requests are generated separately for each broker rather than encouraging a single BCC blast, so each company receives a request addressed to its own privacy team with the locally stored identifying details needed to locate the record.

## California residents

The California DROP portal provides a centralized deletion mechanism for registered data brokers:

https://privacyportal.cppa.ca.gov/

## Important: removals can reappear

Data brokers continuously rebuild records from public and commercial sources. The tracker stores a broker-specific re-check date after a removal is confirmed so users can revisit it later.

## Contributing

PRs are welcome, especially for:

- Verified current opt-out URLs
- Documented privacy-request email addresses
- New brokers
- Changed verification or deletion workflows
- Additional state-level centralized deletion tools

Please verify broker routes before submitting changes. Third-party privacy portals change frequently.

## License

MIT. Use it, fork it, share it.
