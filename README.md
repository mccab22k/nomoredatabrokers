# No More Data Brokers

**Take your data back. It's yours.**

Data brokers collect your personal information — name, address, phone, employer, relatives, income estimates — without your consent, compile it into profiles, and sell it to anyone willing to pay. Then they offer to "protect" you if you subscribe to their removal service. The same people selling your data are selling the fix.

This is a free, open-source tool to systematically opt out yourself.

## What this does

- Tracks your removal progress across 28+ data brokers, tiered by priority
- Links directly to each broker's opt-out portal
- Flags when removals have expired and need to be resubmitted (brokers re-scrape every 3–6 months)
- Includes B2B brokers (ZoomInfo, Apollo, Lusha) that sell your professional identity to sales teams
- Covers the Google visibility tools that de-index your info from search results
- Exports your progress as JSON so you can back it up

**No account. No server. No data leaves your browser.** All state is stored in your browser's localStorage.

## Usage

Open `index.html` directly in any browser. No build step, no dependencies, no install.

```bash
git clone https://github.com/mccab22k/nomoredatabrokers
open nomoredatabrokers/index.html
```

Or use the hosted version at: https://mccab22k.github.io/nomoredatabrokers

## Why this is free

Data brokers make money two ways: selling your data, and charging you to keep it off their platforms. That's extortion with extra steps. Privacy shouldn't cost a subscription. This tool exists because opting out is your legal right under CCPA, GDPR, and an increasing number of state laws — you just need to know where to go and when to go back.

## Broker tiers

| Tier | What they are | Why hit them first |
|---|---|---|
| **1** | Acxiom, LexisNexis, Spokeo, Whitepages, BeenVerified | Feeder brokers — they supply data to hundreds of downstream sites. Removal here has a multiplier effect. |
| **2** | ZoomInfo, Apollo.io, Lusha, RocketReach, Clearbit | B2B professional brokers — sell your work email, direct dial, job title, and org chart to sales teams. |
| **3** | Radaris, TruthFinder, Instant Checkmate, US Search | Consumer people-search — home address, relatives, criminal/civil records. |
| **4** | Epsilon, CoreLogic, Neustar, Datalogix | Ad and data enrichment networks — power the targeted advertising ecosystem. |

## California residents

The DELETE Act (SB 362) created the DROP portal — a single authenticated request that directs all registered California data brokers to delete your data. As of August 2026, brokers are required to process these requests within 45 days.

→ [California DROP portal](https://privacyportal.cppa.ca.gov/)

## Important: removals expire

Brokers continuously re-scrape public records, company websites, LinkedIn, and each other. Even after a confirmed removal, your profile can reappear within 3–6 months. This tool tracks re-check due dates and surfaces expired removals automatically.

Set a calendar reminder to re-open this every 3 months.

## Contributing

PRs welcome — especially:
- New brokers with verified opt-out URLs
- Updated URLs when portals change
- Additional state-level callouts (Texas, Virginia, Colorado DROP equivalents)

Please verify opt-out URLs are live before submitting. Broker portals change frequently.

## Opt-out links

All opt-out links in this tool are direct URLs to each company's privacy portal. They are not affiliate links and this project is not affiliated with any data broker, removal service, or privacy company.

## License

MIT. Use it, fork it, share it.
