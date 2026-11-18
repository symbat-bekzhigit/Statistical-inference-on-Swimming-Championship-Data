# Statistical inference on Swimming Championship Data

### Project Overview

In this project, I performed exploratory data analysis (EDA), parameter estimation, and non-parametric hypothesis testing on results from the 2015 FINA World Swimming Championship to answer three questions:
1. **How are heat swim times distributed?** (Men's 200m freestyle)
2. **Do swimmers actually swim faster in the finals than in the semifinals?** (Women's 50m, 100m, and 200m across freestyle, breaststroke, butterfly, backstroke, and individual medley)
3. **How does swimmer performance decline over long events?** (Women's 800m freestyle heats)


#### Data Source
Official timing records from the **2015 FINA World Aquatics Championships** (`2015_FINA.csv`), originally collected by **OMEGA** (official competition timekeepers).


### Key Findings

* **Outliers Inflate Mean Race Benchmarks:**
  In preliminary heats, a small group of much slower qualifying swimmers skews the overall average. In the Men's 200m Freestyle heats, the average finish time was **111.63 seconds**, while the true middle-of-the-pack time (the median) was **110.04 seconds** showing why median benchmarks are far more accurate when evaluating skewed performance data.

* **Swimmers Do Not "Hold Back" in Semifinals:**
  Comparing the exact same swimmers across both rounds revealed that they improved by only **0.043%** in the finals, a tiny difference that falls well within normal random variation. This proves swimmers already race at peak effort in the semifinals rather than holding back.

* **Steady Mid-Race Fatigue in Distance Events:**
  By filtering out the fast dive start and the final sprint in the Women's 800m Freestyle, steady-state pacing was isolated to show that athletes slow down at a consistent rate of **0.065 seconds every 50 meters** as fatigue sets in.


### Tools & Methods Used

* **Tools:** Python, Pandas, NumPy, Matplotlib, Seaborn
* **Methods:** Empirical Cumulative Distribution Functions (ECDF) visualization, Bootstrap confidence intervals, Paired & correlation permutation hypothesis tests, Linear Regression, Pairs bootstrap resampling.


### Limitations & Next Steps
* **Single-Meet Scope:** Results reflect a single competition (2015 World Championships); expanding the analysis across multiple championship years (e.g., 2017–2024) would test whether these pacing and round-to-round trends hold consistently over time.
* **Survivorship Scope:** The semifinal-to-final comparison necessarily analyzes only the top 8 finalists per event; future work could examine heat-to-semifinal progression to capture a broader tier of competitors.
* **Athlete-Level Pacing:** Modeling fatigue at the individual swimmer level (rather than split averages) could identify distinct pacing profiles—such as front-runners versus negative-split closers.
