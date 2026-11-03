# FINN — investor intelligence prototype

A mobile-first prototype for the ENAM AI Engineer Build Challenge. It focuses on two daily workflows: a prioritized push feed and an on-demand research desk.

## Run it

Open `index.html` in a current browser. There is no build step, account, API key, or install required. The layout adapts to phone and desktop widths.

## Product choices

- **Start with a daily briefing.** A short list of material changes appears before routine filings. The full feed supports company search, category filters, priority filters, and a routine-paperwork view.
- **Make alerts personal.** Price-move and unusual-volume thresholds can be edited and saved in local browser storage. Material categories and routine-paperwork controls are shown alongside them.
- **Give research an evidence trail.** The research desk lays out business, financial trajectory, cash quality, balance-sheet context, guidance versus delivery, and bull/bear views alongside source labels.
- **Keep it usable on a phone.** The dashboard compresses to a one-column feed, with persistent bottom navigation and touch-sized controls.

## Demo data and limits

This is a self-contained interaction prototype. Prices, portfolio values, events, financial figures, and excerpts are **illustrative demo content**, not current market data or verified company disclosures. The sample research profile is deliberately labeled; it must not be used for investment decisions. The research form accepts any NSE symbol, but only a small demo set has sample cards. An unknown ticker shows an awaiting-source state rather than inventing financial claims.

The brief asks for Yahoo Finance end-of-day data, NSE/BSE filings, and annual reports/concall transcripts. Those live ingestion services are not connected here. A production version should add server-side source adapters, retain original filing URLs and timestamps, extract primary-source passages with page/section references, then run classification and summarization over those passages. Alert rules should run against persisted end-of-day observations; the current browser controls only save preferences locally. No broker notes, news, or secondary research is used in the sample research narrative.

## Source layout

- `index.html` — responsive UI, demo fixtures, interactions, and local preference storage.
- `covering-note.md` — short submission note draft.

## Suggested next build steps

1. Add a small API service and a documented data contract for prices, announcements, and source documents.
2. Ingest and cache exchange announcements for a ticker universe; keep the original exchange URL and filing time on every record.
3. Add price/volume history and evaluate configurable triggers after market close.
4. Fetch annual reports and concall transcripts from company or Screener links, extract searchable sections, and show source anchors on each research claim.
5. Replace demo fixtures with validated records, add a deployment, and provide the submitted repository and AI build-history links.
