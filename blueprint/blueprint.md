

# Unified Trading Blueprint: 8/20/50 EMA + Stochastic Scalping System
[![System Version](https://shields.io)](#)
[![Trading Style](https://shields.io)](#)
[![Execution Framework](https://shields.io)](#)

A high-velocity technical trading framework designed for scalping and intraday execution using multi-timeframe moving average alignments and momentum oscillators.
---## 📋 Table of Contents1. [System Specifications & Infrastructure](#1-system-specifications--infrastructure)
2. [⚙️ Core Indicators & Settings](#2-️-core-indicators--settings)
3. [🧠 Master Rulebook & Execution Checklist](#3-master-rulebook--execution-checklist)
4. [🛑 Risk Management Constraints & Controls](#4-risk-management-constraints--controls)
5. [🗺️ Step-by-Step Data Blueprint Mapping](#5-step-by-step-data-blueprint-mapping)
---## 1. System Specifications & Infrastructure### Trading Profile* **Trading Style:** High-Velocity Scalping and Intraday Day Trading.* **Target Assets:** High-Volatility Forex Pairs & Metals (e.g., GBP/JPY, EUR/USD, GBP/USD, XAU/USD).* **Risk-to-Reward (R:R) Profile:** Strict 0.5 R Target (Take Profit is exactly half of the Stop Loss distance).* **Stop Loss Mechanic:** 1-Hour Chart ATR (Average True Range) Volatility Buffer.
### Timeframe Matrix

┌─────────────────────────────────────────────────────────┐
│ ANCHOR TIMEFRAME: 1-HOUR (1H) │
│ [Macro Trend Filter] │
└────────────────────────────┬────────────────────────────┘
│
▼
┌─────────────────────────────────────────────────────────┐
│ EXECUTION GATEKEEPER: 15-MINUTE (15M) │
│ [Structural Synchronicity Check] │
└────────────────────────────┬────────────────────────────┘
│
▼
┌─────────────────────────────────────────────────────────┐
│ EXECUTION CHART: 5-MINUTE (5M) │
│ [Precise Scalp Triggers] │
└─────────────────────────────────────────────────────────┘


---

## 2. ⚙️ Core Indicators & Settings

### Exponential Moving Averages (EMA)
* **8 EMA:** Fast Momentum Trigger & Tape Filter.
* **20 EMA:** Short-Term Equilibrium Line & Primary Scalp Pullback Zone.
* **50 EMA:** Intermediate Structural Value & Master Trend Line.

### Stochastic Oscillator
* **Settings:** `14, 3, 3` (Smooth Momentum Lookback Filter).
* **Overbought (OB) Bound:** $\ge 80$
* **Oversold (OS) Bound:** $\le 20$

---

## 3. 🧠 Master Rulebook & Execution Checklist

### Rule 1: The Macro Filter (1-Hour Chart)
Before any lower-timeframe trade execution, establish the market bias on the 1-Hour Chart.

* **🟢 Long-Only Condition:** Price is above the 1H 50 EMA, **AND** the 1H 8 EMA is sloping upward above the 20 EMA.
* **🔴 Short-Only Condition:** Price is below the 1H 50 EMA, **AND** the 1H 8 EMA is sloping downward below the 20 EMA.
* **⚠️ No-Trade Zone (Flat Filter):** If the 1H EMAs are tangled, flat, or squeezing together, **do not trade**.

### Rule 2: The Timeframe Synchronicity Check (15-Minute Chart)
The 15-minute chart acts as the immediate structural gatekeeper to prevent buying into a heavy drop or shorting into a strong rally.

* **Alignment:** Price on the 15-minute chart must be sitting cleanly above or holding support at its own 20 or 50 EMA.
* **The "Fake Dip" Constraint:** If a 15-minute candle is currently a solid, aggressive red bar pushing down, **ignore all 5-minute buy signals**. Wait for the 15-minute candle to hit its EMA, stall, and leave a rejection wick before executing on the lower chart.

### Rule 3: The 5-Minute Execution Setup

#### 🟩 Buy Setup (Long Trades)
- [ ] **Trend:** Price on the 5-minute chart is trading above the 50 EMA.
- [ ] **Momentum:** The 5-minute 8 EMA is above the 20 EMA, and both are angling upward.
- [ ] **Deep Dip:** Price retraces downward into the 20 EMA or 50 EMA zone.
- [ ] **Oscillator Check:** The 14, 3, 3 Stochastic drops below 20 (Oversold).
- [ ] **🚀 The Trigger:** Enter the trade only when the Stochastic %K line crosses above the %D line **AND** a 5-minute candle closes firmly back above the fast 8 EMA.

#### 🟥 Sell Setup (Short Trades)
- [ ] **Trend:** Price on the 5-minute chart is trading below the 50 EMA.
- [ ] **Momentum:** The 5-minute 8 EMA is below the 20 EMA, and both are angling downward.
- [ ] **Deep Rally:** Price bounces upward into the 20 EMA or 50 EMA zone.
- [ ] **Oscillator Check:** The 14, 3, 3 Stochastic rises above 80 (Overbought).
- [ ] **🚀 The Trigger:** Enter the trade only when the Stochastic %K line crosses below the %D line **AND** a 5-minute candle closes firmly back below the fast 8 EMA.

---

## 4. 🛑 Risk Management Constraints & Controls

> [!IMPORTANT]
> **The High Win-Rate Mandate:** Because this is a 0.5 R target model, you must achieve a win rate **above 67%** to break even after factoring in broker spreads and commissions.

* **🎯 Volatility Buffer:** Place your Stop Loss exactly matching the current 1-Hour ATR value (e.g., if 1H ATR is 30 pips, SL is 30 pips). Your Take Profit must be exactly 15 pips.
* **🛡️ The "Pip-Buffer" Rule:** On high-volatility pairs (GBP/JPY or XAU/USD), add a 3 to 5 pip buffer beyond the 50 EMA or recent structural wick to prevent getting prematurely hunted by wide spreads.
* **🛑 The Entry-Chase Constraint:** If the 5-minute trigger candle is an explosive, oversized momentum bar that closes far away from the EMAs, **skip the trade**. Entering too late bloats your risk relative to the 0.5 R target.
* **🚨 Hard Structural Invalidation:** If you are in a 5-minute scalp and the 15-minute chart prints a full candle close on the wrong side of its own 20 EMA, **exit the trade manually immediately**. The institutional momentum has shifted, and holding for the 1-Hour ATR stop loss is statistically invalid.
* **⏰ The Timing Constraint:** Only trade during peak volume sessions. Turn the system off during quiet, mid-day, or bank holiday sessions when EMAs flatten out.
  * **London Open:** 7:00 AM – 10:00 AM GMT
  * **New York Overlap:** 12:00 PM – 4:00 PM GMT

---

## 5. 🗺️ Step-by-Step Data Blueprint Mapping

This markdown architecture aligns directly with the master system backend schemas as follows:

| System Section | YAML Component Block | Functional Value / Logic Target |
| :--- | :--- | :--- |
| **System Specs** | `system_overview` | Captures strategy title, target assets, and core trading style. |
| **Timeframe Matrix** | `timeframes` | Separates execution charts (5m/15m) from the anchor timeframe (1h). |
| **R:R Profile & Mandates** | `risk_reward_profile` | Defines R:R metrics (0.5), ATR SL calculation, and minimum win-rate requirements (> 67%). |
| **Indicators** | `core_indicators` | Stores technical settings for the 8/20/50 EMAs and Stochastic Oscillator (14, 3, 3). |
| **Rule 1** | `execution_rules.rule_1_macro_filter` | 1-Hour direction and flat filters. |
| **Rule 2** | `execution_rules.rule_2_timeframe_synchronicity` | 15-Minute structural gatekeeper and fake dip controls. |
| **Rule 3** | `execution_rules.rule_3_execution_setup` | 5-Minute precise entry triggers for buy and sell orders. |
| **Risk Controls** | `risk_management_and_controls` | Outlines execution filters, session times, pip buffers, and early invalidation rules. |

------------------------------
