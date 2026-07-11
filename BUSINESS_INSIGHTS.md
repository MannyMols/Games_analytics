# 🎮 Games Analytics — Business Insights Report

**Prepared by:** Emmanuel Mologe
**Project:** Hutch Games Analytics (Portfolio Project)
**Date:** July 2026
**Audience:** Non-technical stakeholders — Product, Marketing, and Leadership teams

---

> **About this report**
> This document summarises what the data is telling us about our players — who they are, where we lose them, what drives them to spend, and where our biggest opportunities lie. No technical jargon. Just the story the numbers are telling.

---

## 📌 Executive Summary

We analysed player behaviour across five key areas: how long players stick around, where they drop out of the game, how different types of players behave, whether a recent game change worked, and how much revenue different player groups generate.

**The headline findings are:**

- Our player retention is **healthy and competitive** against industry standards — but we are leaving growth on the table.
- We are **losing a large portion of new players in the first few hours** of gameplay, and a simple fix could recover a significant share of them.
- Players who engage with optional game modes are **far more likely to stay** — but most players never discover them.
- A recent game change (increasing the chance of winning rare rewards) **meaningfully improved how long players stay**, and the data supports rolling it out more widely.
- A small group of high-spending players (**"Whales"**) generate a disproportionate share of revenue, and we know exactly how to identify and nurture them earlier.
- Some of our paid advertising channels are **not delivering good value** — we are spending money on users who leave quickly and spend little.

---

## 1. 📅 Are Players Sticking Around?

### What We Measured
We tracked how many players were still active 1 day, 7 days, and 30 days after downloading the game. These are known as **Day 1 (D1)**, **Day 7 (D7)**, and **Day 30 (D30)** retention rates.

### What the Data Shows

| Timeframe | Our Performance | Industry Benchmark | Status |
|---|---|---|---|
| After 1 day | 42.9% of players return | 35–45% | ✅ On target |
| After 7 days | 18.8% of players return | 15–20% | ✅ On target |
| After 30 days | 8.0% of players return | 5–8% | ✅ At the top of the range |

In plain terms: **roughly 1 in 5 players who download the game are still playing a week later**, and 1 in 12 are still playing a month later. This is in line with — and in some cases better than — what similar mobile games achieve.

### Where the Opportunity Is
- Players who came to us through **word of mouth or influencer recommendations** stick around the longest.
- Players acquired through **TikTok Ads leave faster** than any other channel — they are less engaged from day one.
- **iPhone users** retain slightly better than Android users (by 1–2 percentage points) across all timeframes.

### What We Recommend
- **Invest more in organic growth** (app store optimisation, community building) and influencer partnerships — these bring in players who stay.
- **Review our TikTok advertising** before spending more on it. We need to understand whether the ads are attracting the wrong type of player, or whether the creative messaging needs refreshing.
- Set up an **automatic alert** so the team knows immediately if new player retention dips below a warning threshold — this allows the product team to react quickly.

---

## 2. 🚪 Where Are We Losing Players?

### What We Measured
We mapped the full journey from the moment a player downloads the game through to the later stages of the campaign, identifying the exact points where players quit.

### What the Data Shows

Think of the player journey like a funnel. Players enter at the top and we want as many as possible to reach the bottom. Here is where the biggest leaks are:

```
100% ─ New players start the tutorial
 82% ─ Complete the tutorial                    ← 18% lost here
 56% ─ Attempt the first boss fight              ← 26% lost here
 35% ─ Defeat the first boss and continue        ← 21% lost here  ⚠️ BIGGEST DROP
  ...  Campaign continues with gradual drop-off
 ~18% ─ Reach the late campaign stages
```

**The first boss fight is our biggest problem.** More than a third of players who attempt it walk away and never come back. This single moment in the game is the largest driver of player loss.

### The Hidden Opportunity: Optional Game Modes

We also discovered something striking: players who try our optional side activities (Arena, Gauntlet, Raids) are **2 to 3 times more likely to still be playing a week later** compared to players who only follow the main story.

The problem? **Only 18% of players ever discover these modes.** The other 82% don’t even know they exist — or don’t feel prompted to try them.

### What We Recommend
- **Make the first boss fight more forgiving**, or introduce a helpful tip/nudge when a player fails — something that encourages them to try again rather than giving up.
- **Actively guide players to Arena mode** after they complete the first few chapters. A simple in-game notification or pop-up could dramatically increase the number of players who discover it — and in turn, dramatically improve retention.
- Recognise that **the critical window is Day 0** (the day of download). Players who do not pass the first boss are very unlikely to ever return.

---

## 3. 👥 Who Are Our Players?

### What We Did
Using data science techniques, we grouped players into five distinct types based purely on how they behave — how often they play, how long their sessions are, and how much they spend.

### The Five Player Types

#### 🐳 Whale
> **Who they are:** Our highest-value players. They play regularly, own many characters, and spend significantly on in-app purchases.
> **Revenue impact:** Average spend of **$428 per player**, with over 9 in 10 making at least one purchase.
> **What they need:** VIP treatment. Exclusive offers, early access, and personalised rewards.

#### 💳 Spender
> **Who they are:** Committed players who spend moderately but consistently.
> **Revenue impact:** Average spend of **$49 per player**, with nearly 8 in 10 making purchases.
> **What they need:** Value-for-money bundles and progression incentives to keep them engaged.

#### ⚔️ Grinder (Free-to-Win)
> **Who they are:** Highly dedicated players who invest significant time but avoid spending real money. They earn rewards through gameplay.
> **Revenue impact:** Minimal direct spend, but high engagement makes them valuable for community health and social proof.
> **What they need:** Meaningful in-game rewards for time invested. They could convert to Spenders with the right offer at the right moment.

#### 🎮 Casual
> **Who they are:** Light players who dip in occasionally but have low investment in the game.
> **Revenue impact:** Almost no spend (average $0.07).
> **What they need:** A reason to care more. Better onboarding and early engagement hooks.

#### 🚪 Churned-Early
> **Who they are:** Players who downloaded the game but stopped very quickly.
> **Revenue impact:** Negligible.
> **What they need:** Win-back campaigns, but the priority should be preventing this group from forming in the first place (see Section 2).

### Why This Matters
We can now **automatically identify which type of player someone is** based on their early behaviour — before they churn. This means we can deliver the right message to the right player at the right time, rather than treating everyone the same.

---

## 4. 🧪 Did Our Recent Game Change Work?

### What We Tested
We ran a controlled experiment where half of our players had a **higher chance of receiving rare (Legendary) rewards** from chests, while the other half continued with the standard drop rates. This type of test is called an **A/B test** — a standard method for making evidence-based product decisions.

### The Results

**What improved significantly (we are confident this is a real effect):**

| Metric | Before Change | After Change | Improvement |
|---|---|---|---|
| Players still active after 7 days | 17.8% | 19.7% | **+10.8% uplift** |
| Chest opens per player | 2.66 | 2.89 | +8.6% more engagement |
| In-game currency spent | 661 | 726 | +9.7% more activity |

**What showed positive trends but needs more data to confirm:**
- The share of players making a purchase went from 3.6% to 3.9% (+8.2%)
- Average spend per player went from $3.36 to $3.67 (+$0.31)

### In Plain English
Giving players a better chance at rare rewards made them **more engaged and more likely to still be playing a week later**. It also made them interact with the chest system more actively. The revenue indicators moved in the right direction, but we would need to run the test longer to be certain of the financial impact.

### What We Recommend
- **Roll out the higher drop-rate to all players.** The improvement in 7-day retention is statistically solid and meaningful.
- Before going fully global, monitor whether the effect holds over **30 and 60 days** — we want to make sure we are not just delaying churn.
- Check whether the change benefits all player types equally, or whether it is particularly impactful for certain groups.

---

## 5. 💰 Where Does Our Revenue Come From?

### What We Measured
We looked at how much different types of players spend and which advertising channels bring in the most financially valuable players.

### Revenue Is Heavily Concentrated

Our revenue does not come from the majority of players — it comes from a small, loyal group:

| Player Type | Average Spend | % Who Make a Purchase |
|---|---|---|
| Whale | $428 | 91% |
| Spender | $49 | 78% |
| Grinder | Very low | Low |
| Casual | $0.07 | Less than 1% |

This means **protecting and nurturing our Whale and Spender segments is a top business priority.** If we lose these players, the revenue impact is immediate and significant.

### Not All Advertising Channels Are Equal

| Channel | Avg. Spend per Player | Retention | Verdict |
|---|---|---|---|
| Apple Search Ads | $6.20 | Strong | ✅ High value |
| Meta (Facebook/Instagram) Ads | $3.58 | Good | ✅ Solid performer |
| Organic (word of mouth, ASO) | Strong | Strongest | ✅ Best overall |
| Influencer Partnerships | $2.38 | Strong | ⚠️ Good retention, lower spend |
| TikTok Ads | Lowest | Weakest | ❌ Underperforming |

### What We Recommend
- **Shift budget away from TikTok Ads** — the players it brings in are both the least likely to stay and the least likely to spend.
- **Invest more in Apple Search Ads and organic growth** — these deliver players with the highest long-term value.
- **Create tailored in-game offers for Whales and Spenders** — personalised, time-sensitive bundles that feel exclusive rather than generic.
- **Design a conversion pathway for Grinders** — these players are deeply engaged and represent untapped revenue potential. A well-timed, fair-value offer could convert a meaningful share of them.

---

## 📌 Summary: The Top 5 Actions

| Priority | Action | Expected Impact |
|---|---|---|
| 1 | Fix the first boss drop-off with a retry nudge or difficulty adjustment | Recover a significant share of Day 0 churners |
| 2 | Surface Arena mode to players after Chapter 2–3 | 2–3× improvement in 7-day retention for adopters |
| 3 | Roll out the higher Legendary chest drop-rate globally | +10.8% improvement in 7-day retention confirmed |
| 4 | Reallocate TikTok ad budget to Apple Search Ads and Organic | Higher LTV players at similar or lower acquisition cost |
| 5 | Launch personalised LiveOps offers for Whales and Spenders | Protect and grow the revenue base from high-value segments |

---

## 📝 A Note on the Data

All datasets used in this analysis are **synthetically generated**, calibrated against real-world mobile gaming industry benchmarks and distributions. They do not represent any real company, real players, or proprietary data. The patterns and metrics are modelled to reflect plausible, industry-consistent behaviour for educational and portfolio purposes.

---

*Report prepared by Emmanuel Mologe | [LinkedIn](https://linkedin.com/in/emmanuel-mologe) | [GitHub](https://github.com/MannyMols)*
