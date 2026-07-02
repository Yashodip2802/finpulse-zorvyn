# ⚡ FinPulse — ProjFuel Market Intelligence Dashboard

> An interactive, real-time fintech analytics dashboard built with Python, Streamlit, and Plotly.

![Python](https://img.shields.io/badge/Python-3.10+-00d4ff?style=flat-square&logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-1.32+-ff3b6b?style=flat-square&logo=streamlit&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-5.18+-00ff88?style=flat-square&logo=plotly&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-f0c040?style=flat-square)

---

## 📌 About the Project

**FinPulse** is a high-performance market intelligence platform designed to track, analyze, and visualize global cryptocurrency market dynamics. Built with a modern, high-fidelity dark terminal aesthetic, FinPulse serves as a consolidated workspace for traders, analysts, and financial enthusiasts to monitor real-time pricing, macro market health metrics, and historical market sentiment indicators.

### Key Value Propositions
* **Consolidated Intelligence**: Integrates multiple data points—from real-time price feeds to global market capitalization KPIs and the crypto Fear & Greed sentiment index—into a single glassmorphic dashboard.
* **Interactive Financial Modeling**: Employs interactive Plotly charting, allowing users to drill down into 30-day historical trends, token-specific market share (dominance), and a multidimensional Risk vs. Return scatter plot.
* **Engineered for Efficiency**: Implements server-side data caching (`@st.cache_data`) with optimized Time-To-Live (TTL) cycles to provide fresh data while maintaining absolute rate-limit compliance with upstream REST APIs.

---

## 🔥 Live Demo

👉 **[View Live Dashboard →](your-streamlit-app-url-here)**

---

## 📊 Features

| Feature | Description |
|---|---|
| 📈 **Live Price Charts** | 30-day BTC & ETH price history with area charts |
| 🌍 **Global Market KPIs** | Total market cap, volume, BTC dominance, active assets |
| 📻 **Live Ticker Tape** | Auto-scrolling real-time price ticker for top 10 assets |
| 😨 **Fear & Greed Index** | 14-day sentiment bar chart with color-coded zones |
| 🍩 **Market Dominance** | Interactive donut chart of top asset market share |
| ⚡ **Sparklines** | 7-day mini trend charts for top 5 assets |
| 📋 **Top 10 Table** | Color-coded data table with 1h / 24h / 7d performance |
| 🎯 **Risk vs Return** | Scatter plot — volume vs 24h change, bubble-sized by market cap |

---

## 🛠️ Tech Stack

- **Frontend**: Streamlit + custom CSS (dark fintech aesthetic)
- **Charts**: Plotly (interactive, hover-enabled)
- **Data**: CoinGecko API + Alternative.me Fear & Greed API (both free, no API key needed)
- **Caching**: Streamlit `@st.cache_data` with 5-min TTL for rate limit safety

---

## 🚀 Run Locally

```bash
# Clone the repo
git clone https://github.com/Yashodip2802/finpulse-zorvyn.git
cd finpulse-zorvyn

# Install dependencies
pip install -r requirements.txt

# Run the dashboard
streamlit run app.py
```

---

## 📁 Project Structure

```
finpulse-zorvyn/
├── app.py              # Main Streamlit dashboard
├── requirements.txt    # Python dependencies
└── README.md           # You're here!
```

---

## 🔌 APIs Used

| API | Endpoint | Rate Limit |
|---|---|---|
| CoinGecko | `/coins/markets` | 30 req/min (free) |
| CoinGecko | `/coins/{id}/market_chart` | 30 req/min (free) |
| CoinGecko | `/global` | 30 req/min (free) |
| Alternative.me | `/fng/` | Unlimited (free) |

> No API keys required — all free public endpoints.

---

## 💡 Design Decisions

- **Dark fintech aesthetic** — inspired by Bloomberg Terminal & modern trading UIs
- **Space Mono + Syne** — technical monospace + modern sans pairing
- **5-minute cache TTL** — balances freshness vs API rate limits
- **Zero dependencies on paid APIs** — fully reproducible for anyone

---

## 👩‍💻 Built By

**Yashodip** — Intern @ ProjFuel  
*This project was built as a demonstration of real-world data analytics & dashboard engineering skills during the ProjFuel internship.*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=flat-square&logo=linkedin)](https://linkedin.com/in/yashodip2802)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=flat-square&logo=github)](https://github.com/Yashodip2802)

---

*Data refreshes every 5 minutes. Built with ❤️ and way too much caffeine.*
