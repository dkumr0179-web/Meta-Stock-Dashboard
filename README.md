# 📊 META Stock — Performance & Risk Dashboard

An executive-level, single-file interactive dashboard that transforms raw daily stock price data into boardroom-ready financial risk intelligence — built for investment leadership reporting.

![Status](https://img.shields.io/badge/status-complete-brightgreen)
![HTML](https://img.shields.io/badge/HTML-single--file-orange)
![Chart.js](https://img.shields.io/badge/Chart.js-4.4.4-blue)
![License](https://img.shields.io/badge/license-MIT-lightgrey)

## 🔗 Live Demo
https://metastockdashboard.oneapp.dev/

## 🎯 Overview

Built as a decision-support tool for leadership who need to understand trend direction, volatility, drawdowns, return consistency, and downside risk without digging through raw data or spreadsheets. Every chart, KPI, and insight responds live to a global filter panel.

## ✨ Features

- 5 live KPI cards — latest price, total return, annualized volatility, max drawdown, Sharpe ratio
- 12 interactive charts — price trend, returns distribution, rolling volatility, drawdown, OHLC candlestick, monthly return heatmap, volume/price scatter, YoY comparison, benchmark relative performance, event impact analysis, risk-return quadrant, support/resistance range
- Global filter panel — period, year, price type, frequency (daily/weekly/monthly), benchmark, event marker — all charts update together
- Automated insights panel — plain-language takeaways generated dynamically from the filtered data
- Zero backend, zero build step — one HTML file, CDN-loaded dependencies only

## 🖼️ Preview

![Dashboard Preview](https://raw.githubusercontent.com/dkumr0179-web/Meta-Stock-Dashboard/6da07bf41edff91eaa447d5d606b0f92207f97f7/Meta%20Dashboard%20Preview.png)

## 🛠️ Tech Stack

- Vanilla JavaScript (ES6+) — no framework, no build tooling
- Chart.js + chartjs-chart-financial (candlesticks) + chartjs-plugin-annotation (event markers, quadrant lines)
- Hand-rolled financial math: rolling volatility, drawdown, Sharpe ratio, resampling, event detection — no external analytics library

## 📐 Data Handling & Transparency

The source dataset (daily OHLCV) does not include adjusted close, benchmark, dividend, split, or earnings data. Rather than fabricate these:

| Field | Approach |
|---|---|
| Adjusted Close | Falls back to Close (no corporate-action data available) |
| Benchmark | Clearly labeled simulated sector index, off by default |
| Earnings events | Algorithmically detected from volume/price anomalies, not sourced |
| Dividend markers | Modeled quarterly cadence, labeled "illustrative" |
| Stock splits | None detected — explicitly stated, not guessed |

This distinction is surfaced directly in the UI so no one mistakes a model output for a confirmed fact.

## 🚀 Getting Started

git clone https://github.com/dkumr0179-web/Meta-Stock-Dashboard.git
cd Meta-Stock-Dashboard
open index.html   # or just double-click the file

No install, no dependencies to manage — it runs entirely in the browser.

## 📁 Project Structure

├── index.html          # Full dashboard (self-contained)
├── README.md
└── /assets             # Screenshots / demo GIF (optional)

## 🌐 Deployment

Live at: https://metastockdashboard.oneapp.dev/

To also host via GitHub Pages:
1. Settings → Pages → Deploy from branch → main / root
2. Your dashboard will be live at https://dkumr0179-web.github.io/Meta-Stock-Dashboard/

## 📄 License

MIT — free to use, modify, and build on.

## 🙋 About

Built as a demonstration of executive dashboard design: turning raw financial time-series data into a clean, filterable, insight-driven interface — with an explicit focus on not overstating what the data actually supports.

Author: dkumr0179
