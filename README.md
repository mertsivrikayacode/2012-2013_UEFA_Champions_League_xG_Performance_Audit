# 2012-2013_UEFA_Champions_League_xG_Performance_Audit
This project delivers a comprehensive, data-driven tactical audit of the historic 2013 UEFA Champions League Final between Borussia Dortmund and Bayern Munich at Wembley. Moving beyond traditional box-score metrics, this analysis utilizes high-fidelity event data to dissect team momentum, spatial shot quality, and individual finishing efficiency.

# UEFA Champions League 2013 Final: Full-Match Expected Goals (xG) Performance Audit
**Author:** Mert Sivrikaya  
**Role Target:** Football Data Analyst / Technical Scout  
**Data Provider:** StatsBomb Open Data  

---

# Executive Summary
This project delivers a comprehensive, data-driven tactical audit of the historic 2013 UEFA Champions League Final between Borussia Dortmund and Bayern Munich at Wembley. Moving beyond traditional box-score metrics, this analysis utilizes high-fidelity event data to dissect team momentum, spatial shot quality, and individual finishing efficiency ($\Delta = \text{Goals} - \text{xG}$).

The entire pipeline is programmatically automated in Python, eliminating manual data entry and establishing an industry-standard workflow for modern sports analytics.

---

# Analytical Dimensions & Core Pillars

## 1. Spatial Shot Quality (Shot Maps)
Instead of looking at raw shot volumes, we audit the location and intrinsic probability of each attempt using StatsBomb's 120x80 coordinate matrix.
* **Bayern Munich Structure:** Evaluates how Heynckes' side penetrated the central corridors of the penalty box to generate high-value opportunities.
* **Borussia Dortmund Structure:** Visualized with a custom horizontal flip (attacking from right to LEFT) to isolate Jürgen Klopp’s offensive transitions, highlighted by İlkay Gündoğan’s 60th-minute penalty (0.76 xG).

## 2. Finishing Efficiency Audit
An institutional look at player-level productivity, calculating the delta between expected output and real conversion.
$$\text{Finishing Efficiency} = \text{Actual Goals} - \text{Accumulated xG}$$
This framework highlights elite shot-stopping performance from the goalkeepers (e.g., Manuel Neuer suppressing BVB's high xG threats) and rewards positional mastery.

## 3. Tactical Momentum (Cumulative xG Flow)
A chronological step-plot tracking the accumulated xG variance from the 1st to the 90th minute. This timeline mathematically validates:
* Dortmund’s aggressive structural dominance and *Gegenpressing* spikes during the opening 25 minutes.
* Bayern’s calculated resurgence, culminating in Arjen Robben’s decisive 89th-minute match-winning strike.

---

# Tech Stack & Open-Source Libraries
* **Colab Link:** https://colab.research.google.com/drive/1K4I5gB7EVR6mjWxEu4zoYys8gePr0esO?usp=sharing
* **Language:** Python 3
* **Data Ingestion:** `statsbombpy` (API client for corporate StatsBomb servers)
* **Spatial Pitch Modeling:** `mplsoccer` (Standardized engineering framework for pitch grids)
* **Data Engineering:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib`
