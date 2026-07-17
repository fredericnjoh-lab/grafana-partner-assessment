# Partner Business Case Simulator — Grafana Labs

Bilingual (FR/EN) single-file simulator that models the economic opportunity of a
Grafana Labs partnership for a services partner (GSI, SI, MSP, VAR, MSSP, Cloud
Provider, Consulting Firm).

## Run

Open `index.html` in any modern browser. No build step, no dependencies to install
(Chart.js is loaded from a CDN).

For local testing over HTTP:

```bash
python3 -m http.server 8791
# then open http://localhost:8791/index.html
```

## What it does

From partner profile + commercial assumptions, it computes across three scenarios
(Conservative / Realistic / Ambitious):

- Total generated revenue, revenue mix (License, Support, Prof. Services, Managed,
  Advisory, Training) and the **Services : License ratio** — the model's key lever.
- Gross margin, ROI, payback period, additional EBITDA.
- 5-year projection, CAGR, CLV, team-capacity / utilization.
- Sensitivity of total revenue to the Services : License ratio.
- Short / medium / long-term recommendations derived from the inputs.

## Features

- **Bilingual FR/EN** — auto-detects browser language on first visit, manual FR/EN
  toggle, all static and dynamic content (narratives, tables, charts, recommendations)
  translated. Currency and dates use the active locale.
- **Live recalculation** — the model updates as inputs change (debounced).
- **Persistence** — the last state and language are restored from `localStorage`.
- **Import / export** — export the full case (assumptions + computed results) as JSON,
  and re-import it later.
- **Print** — a print-friendly executive summary.
- **Accessibility** — visible keyboard focus, ARIA on tabs and the language switch,
  reduced-motion support.

## Structure

Everything lives in `index.html`:

- `<style>` — component-scoped, Grafana-branded dark theme.
- static markup with `data-i18n` keys.
- `<script>` — i18n dictionary + engine, computation model, renderers, charts.

—Fred
