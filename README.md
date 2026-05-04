# Roland Tuboly

Social Data Science final-year MSc student at Corvinus University of Budapest, graduating June 2026. I work on **applied statistics, causal inference, and data analysis** — most recently using regression discontinuity methods to study how LLM training cutoffs shape software adoption.

Looking for entry-level **data scientist / data analyst** roles. Budapest local or remote EU.

📫 [tuboly.roland.levente@gmail.com](mailto:tuboly.roland.levente@gmail.com) · [LinkedIn](https://linkedin.com/in/rolandtuboly10)

---

## Highlighted work

### [Do LLMs Shape the Diffusion of New Software?](https://github.com/tubolyroli/thesis)
*MSc thesis · Python · Regression Discontinuity Design + Diff-in-Discontinuities*

Tests whether LLM training cutoffs distort the diffusion of newly released Python libraries. Estimated using RDD around the documented September 2021 GPT-3.5/GPT-4 cutoff, with 2018-2020 placebo cohorts isolating cutoff-specific effects from seasonal confounding.

**Result:** pre-cutoff Python libraries average roughly five times more weekly downloads than post-cutoff peers by early 2026, with no evidence of catch-up. Effect is absent at release and emerges only after ChatGPT launch (Nov 2022). Baseline-adjusted Diff-in-RDD p = 0.002 with year-by-week clustered standard errors.

### [UK Road Safety — Predicting Fatal Collisions](https://github.com/tubolyroli/aimlgroupproject)
*Course project · Python · scikit-learn*

End-to-end ML pipeline on UK STATS19 2024 road safety data, predicting whether a collision will be fatal. The dataset is severely imbalanced (~1.5% fatal), so the modeling problem is fundamentally one of *finding the rare positive class*, not maximizing accuracy.

**Methodological framing:** A majority-rule baseline scores 98.5% accuracy and 0% recall on fatal cases — useless despite the high accuracy. The right metric is **recall on the fatal class**, since false negatives (missed fatal collisions) are far costlier than false positives in a road-safety triage context.

**Approach:** leakage-safe preprocessing (no target-derived features). Class imbalance handled in-model via `class_weight="balanced"` (Lasso) and `"balanced_subsample"` (random forest), avoiding the artificial-sample artifacts of SMOTE-style resampling. Hyperparameters selected via **5-fold stratified cross-validation with `recall` as the scoring metric**, then final performance reported on a held-out test set.

**Result:** Lasso Logistic Regression outperformed Random Forest, achieving **0.78 recall and 0.83 ROC AUC** on the fatal class versus 0.64 / 0.80 for random forest. The simpler regularized linear model beating the tree ensemble is consistent with much of the predictive signal being approximately linear once categorical features are encoded.

### [Hungarian Counties — Industrial Network Analysis](https://github.com/KrisX03/Differences-between-Hungarian-counties)
*Course project · R · igraph, network analysis*

Network analysis of industrial structure differences between Győr-Moson-Sopron and Hajdú-Bihar counties, building a bipartite firm-industry network from national administrative data and comparing structural properties across the two regions.

**My contribution:** owned the **node-level analysis** component — building the per-node summaries (centrality measures, node attributes) that fed into the comparative analysis. Also handled the final cleanup pass before submission (naming conventions, repo structure). 

---

## Tools

**Core:** Python (pandas, numpy, scikit-learn, statsmodels) · R · LaTeX · Git
**Comfortable with:** RDD/DiD/IV (rdrobust, fixest), NetworkX, matplotlib/seaborn
**Currently building:** SQL fluency for industry data work, predictive ML workflows beyond coursework

---

## About

I came into data science from a business undergrad, and the path through Corvinus's Social Data Science MSc has shaped what I'm good at: **applied statistics with a causal lens, communicating findings clearly, and building reproducible analyses**. My thesis pushed me deepest on the first two — running an RDD on real ecosystem data, defending the identifying assumptions, and presenting the result to non-specialists.

SQL fluency at industry depth and end-to-end predictive ML are my current focus areas through summer 2026.

If you're hiring for entry-level data roles in Budapest or remote EU, I'd be glad to talk.
