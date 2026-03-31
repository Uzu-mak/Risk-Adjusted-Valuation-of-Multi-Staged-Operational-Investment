# Risk-Adjusted-Valuation-of-Multi-Staged-Operational-Investment Using Decision Analysis
# Risk-Aware Decision Analysis of Asset Retention vs Sale Under Uncertainty

## Overview

This project develops a multi-stage decision analysis model to evaluate whether a decision maker should **sell a business for a guaranteed value** or **continue operating under uncertainty**.

The analysis demonstrates how decisions change when moving from **expected monetary value (EMV)** to **risk-adjusted utility-based evaluation**, which is critical in real-world engineering, manufacturing, and capital investment decisions (e.g., Boeing, Ford).

---

## Decision Problem

The decision maker must choose between:

- **Sell the business** for a certain payoff of **20 billion credits**
- **Continue operating**, facing multiple layers of uncertainty:
  - Production cost variability
  - Settlement outcomes
  - Technical success or failure

---

## Model Structure

The decision is modeled as a **multi-stage stochastic decision tree**:

### Stage 1: Production Cost
- Inexpensive (18.5%)
- Moderate (63%)
- Costly (18.5%)

### Stage 2: Settlement Outcome
- Agreement (68%)
- Dispute (32%)

### Stage 3: Technical Outcome
- Success (85%)
- Failure (15%)

Each path leads to different payoffs, capturing operational and financial uncertainty.

---

## Methodology

The analysis combines classical and advanced decision analysis techniques:

- Decision Tree Modeling (PrecisionTree)
- Expected Monetary Value (EMV)
- Exponential Utility Function
- Certainty Equivalent (CE)
- Risk Premium Analysis
- Goal Seek for Risk Tolerance Estimation

---

## Mathematical Framework

### Expected Value

\[
EV = \sum p_i x_i
\]

### Exponential Utility Function

\[
U(x) = 1 - e^{-x/R}
\]

### Certainty Equivalent

\[
CE = -R \cdot \ln(1 - EU)
\]

### Risk Premium

\[
RP = EV - CE
\]

---

## Key Results

- **Expected Monetary Value (Do Not Sell):** ~50.05 billion credits  
- **Sell Option (Certain):** 20 billion credits  

Despite the higher EMV, the decision maker is willing to sell due to risk aversion.

### Risk Tolerance Calibration

Using Goal Seek:

- CE = 15 → **Risk Tolerance ≈ 43.29**
- CE = 20 → **Risk Tolerance ≈ 53.55**

---

## Insights

- The EMV-optimal decision is to **not sell**, but this ignores risk preferences.
- The decision maker exhibits **strong risk aversion**, accepting a significantly lower certain value.
- The difference between EMV and CE represents a large **risk premium**, indicating substantial sensitivity to uncertainty.
- As certainty equivalent increases, **risk tolerance increases**, implying reduced risk aversion.
- Decision outcomes are **preference-dependent**, highlighting the importance of utility-based analysis in real-world decision-making.

---

## Business Interpretation

This framework reflects real industry scenarios such as:

- Asset divestment vs continued operation
- Capital investment under uncertainty
- Manufacturing and production risk decisions
- Engineering reliability and performance tradeoffs

It demonstrates why **expected value alone is insufficient** and why organizations must incorporate **risk-adjusted decision metrics**.

---

## Tools Used

- Excel
- PrecisionTree (Decision Analysis Add-in)

---

## Project Structure
