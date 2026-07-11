# 🎮 Games Analytics Project

## Overview
An end-to-end data analytics project exploring game performance data using Python, exploratory data analysis (EDA), machine learning, and an interactive HTML dashboard. The project simulates a real-world Games Analyst workflow across five analytical domains: player retention, funnel drop-off, behavioural segmentation, A/B testing, and monetisation & LTV.

---

## 💡 Business Insights

The following insights are derived from the five analytical notebooks in this project. Each section translates data findings into actionable recommendations for product, user acquisition (UA), and LiveOps teams.

---

### 📈 1. Player Retention (Notebook 01)

**Key Metrics vs. Industry Benchmarks:**
- **D1 Retention:** ~42.9% ✅ (Benchmark: 35–45%)
- **D7 Retention:** ~18.8% ✅ (Benchmark: 15–20%)
- **D30 Retention:** ~8.0% ✅ (Benchmark: 5–8%, at upper bound)

**Channel & Platform Insights:**
- Organic and Influencer channels produce the stickiest players (D7 ~20%), outperforming all paid acquisition sources.
- TikTok Ads underperforms on both D7 (~17%) and D30 (~6.6%) retention — the weakest channel across all horizons.
- iOS users retain 1–2 percentage points better than Android users across all retention windows.

**Recommendations:**
- Prioritise UA budget toward Organic amplification (SEO/ASO) and Influencer partnerships.
- Flag TikTok Ads for a creative refresh and a CPI-vs-LTV audit before any Q4 budget scaling.
- Implement automated weekly cohort monitoring; trigger a product-side regression review if D1 retention dips below 38%.

---

### 🔻 2. Funnel & Drop-off Analysis (Notebook 02)

**Critical Drop-off Points:**
- ~31% of players drop off immediately after completing the tutorial — the first major engagement cliff.
- ~37% of players who attempt the first boss fail to proceed past it, representing the single largest drop-off event.
- A further ~47.8% of mid-campaign players are lost between Chapter 11 and Chapter 12.

**Side Content as a Retention Multiplier:**
- Players who adopt optional side content (Arena, Gauntlet, Raids) retain at **2–3× the rate** of non-adopters.
- Only ~18% of players currently discover the Arena mode, suggesting a significant missed retention opportunity.

**Recommendations:**
- Reduce boss difficulty or introduce a retry nudge/tip UI at the first boss defeat screen to reduce early churn.
- Surface the Arena mode earlier in the campaign via triggered push notifications or in-game popups after Chapter 2–3.
- The engagement cliff is concentrated on Day 0 — users who do not pass the first boss are highly unlikely to return.

---

### 👥 3. Player Segmentation & ML Clustering (Notebook 03)

**Identified Player Segments (K-Means, k=5):**
| Segment | Description |
|---|---|
| **Casual** | Low-intensity play, minimal spend |
| **Churned-early** | Very low activity, quick drop-off |
| **Grinder-F2W** | High sessions/playtime, high currency spend, low IAP |
| **Spender** | Moderate-to-high IAP and strong progression |
| **Whale** | High IAP, high character/legendary counts, long-term activity |

**ML Performance:**
- Unsupervised K-Means clustering successfully rediscovered all five studio-defined segments from raw behavioural telemetry alone.
- The model shows strong alignment for Spender and Grinder-F2W profiles; Casual and Churned-early segments show some overlap due to behavioural similarity in early lifecycle stages.
- Top differentiating features: `total_iap_usd`, `gems_spent_total`, and `characters_owned`.

**Recommendations:**
- Promote the most stable discovered clusters to canonical player personas for use across product and marketing teams.
- Transition the clustering model into production to enable dynamic, real-time player classification from incoming telemetry — eliminating dependency on manual labelling.
- Use segment outputs to drive LiveOps targeting, UA campaign optimisation, and adaptive difficulty tuning.

---

### 🧪 4. A/B Test — Legendary Chest Drop-Rate (Notebook 04)

**Test Overview:** Evaluated the impact of a higher legendary chest drop-rate on retention, payer conversion, and in-app purchase (IAP) revenue.

**Results:**
| Metric | Control | Variant | Lift | Significant? |
|---|---|---|---|---|
| **D7 Retention** | 17.82% | 19.74% | +10.77% | ✅ Yes (p < 0.0001) |
| **Payer Conversion** | 3.56% | 3.86% | +8.24% | ❌ No (p = 0.18) |
| **Avg IAP (USD)** | $3.36 | $3.67 | +$0.31 | ❌ No (p = 0.63) |
| **Chest Opens** | 2.66 | 2.89 | +8.6% | — |
| **Gems Spent** | 661.5 | 725.6 | +9.7% | — |

**Recommendations:**
- The statistically significant lift in D7 retention, combined with positive trends across all secondary engagement metrics, justifies moving toward a wider rollout of the variant.
- Monitor D30/D60 retention and long-term LTV before finalising a full global release.
- Conduct segment-level analysis (e.g., impact on Whales vs. Casual players) to check for heterogeneous treatment effects before scaling.

---

### 💰 5. Monetisation & LTV Analysis (Notebook 05)

**Segment Monetisation Breakdown:**
| Segment | Avg IAP (USD) | Payer Rate |
|---|---|---|
| **Whale** | £428.12 | 91.3% |
| **Spender** | £49.36 | 77.6% |
| **Grinder-F2W** | Low IAP | High currency spend |
| **Casual** | £0.07 | 0.8% |

**Acquisition Channel LTV Proxies:**
- **Highest LTV:** Apple Search Ads (£6.20 avg IAP), Meta Ads (£3.58 avg IAP)
- **Lowest LTV:** Influencer traffic (£2.38 avg IAP) — notable contrast to Influencer's strong retention performance
- TikTok Ads correlates with both the lowest retention and lowest monetisation metrics

**Recommendations:**
- Reallocate UA budget toward high-LTV acquisition sources (Organic, Apple Search Ads) and reduce spend on underperforming channels.
- Implement personalised LiveOps offers segmented by player type: tailored bundles for Whales and Spenders, engagement nudges for Grinders, and churn-prevention campaigns for Casual players.
- Use the combined retention and monetisation gains from the legendary chest experiment to inform future reward economy design changes.

---

## 📁 Project Structure

- `data/raw/` — Original datasets
- `data/processed/` — Cleaned and feature-engineered data
- `notebooks/` — Jupyter Notebooks for EDA and modelling
- `outputs/` — Charts and model output files
- `dashboard/` — Interactive analytics dashboard (HTML)

## 🛠️ Tools & Technologies

- Python (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn)
- Jupyter Lab
- HTML

## 🚀 How to Run

1. Clone the repository: `git clone <repo-url>`
2. Install dependencies: `pip install -r requirements.txt`
3. Open notebooks in Jupyter Lab
4. Open `dashboard/GamesAnalytics_Dashboard.html` in any browser

## 👤 Author

Emmanuel Mologe — [LinkedIn](https://linkedin.com/in/emmanuel-mologe) | [GitHub](https://github.com/MannyMols)
