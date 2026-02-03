# Nigeria CPI & Inflation Dynamics Pre-Covid to 2025
### **Detecting inflation shocks with Median Absolute Deviation (MAD), attributing causes, and evaluating policy efficacy (2019–2025)**

---

## Overview

This project presents a comprehensive, data-driven analysis of Nigeria’s *All Items Consumer Price Index (CPI)* and inflation dynamics from January 2019 to December 2025. The investigation moves beyond headline figures to provide a *context-aware interpretation* of CPI movements, with a particular focus on the interplay of *base effects*, volatility, and policy-induced structural shifts.

Using robust statistical methods, the analysis systematically:

- **Identifies and quantifies inflation shocks** (anomalous accelerations/decelerations in YoY rates) using the **Median Absolute Deviation (MAD)** method, moving beyond subjective thresholds.
- **Attributes drivers** across episodes, distinguishing between policy-driven actions (e.g., FX liberalization, fuel subsidy reform, monetary tightening), structural vulnerabilities (insecurity, supply shocks), global factors, and statistical effects (base effects, CPI rebasing).
- **Assesses the efficacy** of recent monetary and fiscal responses and distinguishes between cost-push versus demand-pull inflationary forces.
- **Provides policy-relevant insights** into Nigeria's structural vulnerabilities and the crucial role of base effects and seasonal factors in shaping observed headline inflation trends.

---

## Key Objectives

This project aims to systematically investigate Nigeria's inflation dynamics (2019–2025) by:

- **Distinguishing Real vs. Statistical Disinflation:** Decompose observed CPI deceleration to reliably separate base effects and temporary interventions from actual, structural improvements in price stability.
- **Quantifying and Attributing Shocks:** Systematically detect periods of anomalous acceleration (inflation shocks) using the Median Absolute Deviation (MAD) as a robust statistical threshold, and classify their primary drivers (e.g., policy-driven, structural, or statistical).
- **Evaluating Policy Efficacy:** Assess the impact of major structural policy shifts (FX liberalization, fuel subsidy removal, 2024 CPI rebasing) and monetary responses on the transition from hyper-acceleration to statistical disinflation in 2025.
- **Providing a Reproducible Framework:** Deliver a transparent and scalable methodology for robust inflation analysis applicable to other emerging economies facing similar volatility.

---

## Methodology

This analysis employs a multi-faceted approach to interpret Nigeria's inflation dynamics, focusing on robust identification of significant economic shifts and underlying drivers.
The core methodology integrates:

1. **Exploratory Data Analysis (EDA):** Initial visual and statistical analysis to understand the data structure, seasonality, and trends.
2. **Change-in-YoY Analysis:** A critical step to identify sharp accelerations and decelerations in the inflation rate, signaling potential shifts in the economic regime or policy impact.
3. **Contextual Interpretation:** Integrating findings with known macroeconomic events, major policy changes, and global commodity price movements for a holistic understanding.

#### Robust Outlier Detection using MAD

Given the high volatility and frequent extreme price swings characteristic of the Nigerian market, traditional statistical measures (like the Z-score) are unsuitable for identifying genuine turning points, as outliers tend to skew the mean and standard deviation.

To objectively establish a threshold for identifying `sharp increases` or `regime shifts,` we employ the **Median Absolute Deviation (MAD)**. As a robust statistic, MAD is significantly less sensitive to extreme outliers than standard deviation. This allows for a more accurate and reliable identification of genuine and economically significant shifts in the inflation trend, rather than mere statistical noise.

**Special attention is given to periods of sharp CPI movement**, particularly declines. We analyze whether these movements reflect genuine economic relief, effective policy intervention, or are primarily the result of statistical base effects.

---

## Key Findings: The Four Inflation Epochs and the Base Effect

This analysis identifies four distinct epochs in the recent inflation trajectory, culminating in a period where reported disinflation was largely statistical rather than fundamental.

#### The Four Epochs:

1. **2020–2021 (Supply-Side Shock):** Initial inflation driven by COVID-19-related disruptions and domestic supply constraints, notably land border closures.
2. **2022 (Global Commodity Spike):** Inflationary pressure amplified by global supply chain crises and escalating energy costs.
3. **2023–2024 (Policy-Induced Acceleration):** Sharp CPI increases following significant domestic policy shifts, specifically the removal of the fuel subsidy and the unification of exchange rate windows.
4. **2025 (The Base Effect & Rebasing):** A period where official figures indicated a statistical decline. The analysis reveals this deceleration was primarily a `Base Effect,` exacerbated by the 2024 CPI rebasing, rather than a sustained return to price stability.

#### Key Insights on Disinflation:

- **Statistical vs. Actual Stability:** Sharp CPI decelerations often coincide with **high-base comparison periods (base effects)**, which masks persistent underlying inflationary pressures.
- **Policy and Supply Relief:** Temporary policy interventions and supply reliefs tend to amplify these base effects rather than eliminate core inflation.
- **Sustained Disinflation:** A genuine and sustained return to price stability requires consistency across multiple macroeconomic indicators, not just isolated, statistically-driven slowdowns in the headline CPI.

---

## Project Structure
```text
.
├── data/
│   └── nigeria_monthly_cpi_2019_2025.csv
├── notebooks/
│   └── Nigeria CPI & Inflation Regime Shifts (2019-2025).ipynb
├── figures/
│   └── (generated charts and visuals)
├── README.md
└── LICENSE
```

---

## Data
- **Dataset:** Nigeria CPI & Inflation Data - Composite Index (2019–2025)
- **Frequency:** Monthly
- **Source:** [National Bureau of Statistics (NBS), Nigeria](https://microdata.nigerianstat.gov.ng/index.php/catalog/154)
- **Coverage:** Multiple years

The dataset includes computed inflation measures and derived indicators used to study volatility and sharp CPI movements.

> The dataset is also published on [Kaggle](https://www.kaggle.com/datasets/d0lheghend/nigeria-cpi-and-inflation-data-20192025) for wider access and discussion.
- [Dataset](https://www.kaggle.com/datasets/d0lheghend/nigeria-cpi-and-inflation-data-20192025) – Monthly NBS CPI series with derived metrics
- [Notebook on Kaggle](https://www.kaggle.com/code/d0lheghend/nigeria-cpi-inflation-regime-shifts-2019-2025) – Interactive version

---

## How to Reproduce the Analysis

1. **Clone the repository and navigate into the directory:**
```bash
git clone https://github.com/dlhegend/nigeria-cpi-inflation.git
cd nigeria-cpi-inflation
```
2. **Install dependencies:**
Run the following command in your terminal or a notebook cell:
```Bash
pip install numpy pandas matplotlib seaborn
```
3. **Open the notebook:**
  - **Recommended:** Upload the notebook to [Google Colab](https://colab.google/) (File → Upload notebook).
  - **Locally:** Open the notebook using jupyter notebook or an environment like VS Code + Jupyter extension.
4. **Run the analysis:**
  - Update file paths if necessary (the notebook uses relative paths or Kaggle-style /kaggle/input/).
  - Execute all cells in the notebook (e.g., Shift+Enter or Runtime → Run all) to view the full analysis and calculations.

---

## Use Cases

This project may be useful for:

- Data scientists analyzing inflation time series

- Economists studying emerging-market price dynamics

- Policy analysts interpreting CPI releases

- Students learning applied macroeconomic data analysis

---

## Limitations

- CPI data is subject to revisions and methodological changes by the statistical authority.

- This analysis does not attempt causal inference; interpretations are contextual and descriptive.

- External shocks (FX movements, fuel price changes) are discussed qualitatively, not modeled explicitly.

---

## Future Research Directions

Building on the current analysis, future work will focus on:

- **Inflation Decomposition and Modeling:** Decomposing the Month-on-Month (MoM) inflation shocks by sector (Food, Core, Energy) to refine the Mean Absolute Deviation (MAD) analysis. This will be complemented by employing advanced time-series models, such as Structural Vector Autoregression (SVAR) and regime-switching models, and LSTMs for forecasting.
- **External and Expectational Dynamics:** Fully integrating the interplay of MoM inflation dynamics and Foreign Exchange (FX) rates. We will also incorporate the modeling of inflation persistence and expectations to enhance predictive accuracy.
- **Early Warning and Cross-Country Analysis:** Developing an early-warning system to identify potential inflation turning points. Additionally, a cross-country comparison of the CPI base-effect will be conducted to benchmark findings and identify best practices.

---

## Feedback & Contact

**Author:** DOUGLAS, Unyime-Abasi (Victor)

**X / Twitter:** [@dz_unyimeabasi](https://x.com/dz_unyimeabasi)

**LinkedIn:** [Unyime-Abasi Douglas](https://www.linkedin.com/in/unyimeabasi-douglas/) 

**Data Source:** [National Bureau of Statistics (NBS) E-library](https://www.nigerianstat.gov.ng/elibrary)

> *Star ⭐ the repo if this analysis is useful for your work on Nigerian economics or time-series inflation studies!*
> 
> *Feedback, critiques, pull requests, forks, and collaborations are also welcome!*

---
