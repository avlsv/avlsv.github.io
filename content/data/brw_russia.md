---
title: "Monetary Policy Surprises for Russia (BRW)"
date: 2026-11-15
tags: ["monetary policy", "Bank of Russia", "yield curve"]
author: ["Alexander Vlasov"]
description: "Monthly series of Bank of Russia monetary policy surprises identified with the Bu, Rogers and Wu (2021) method from the Russian government bond yield curve, February 2014 to November 2026."
summary: "Monthly series of Bank of Russia monetary policy surprises identified with the Bu, Rogers and Wu (2021) method from the Russian government bond yield curve, February 2014 to November 2026."
editPost:
    URL: "https://github.com/avlsv/BRWRussia"
    Text: "GitHub repository"
showToc: true
disableAnchoredHeadings: false

---

## Overview

This series measures monetary policy surprises of the Bank of Russia. It applies the method of [Bu, Rogers and Wu (2021), "A Unified Measure of Fed Monetary Policy Shocks", *Journal of Monetary Economics* 118: 331–349](https://doi.org/10.1016/j.jmoneco.2020.11.002) to Russian data.

The BRW approach uses the whole yield curve rather than a single short rate. It runs in two stages:

1. **Sensitivities.** For each maturity, it estimates how strongly the yield responds to the 2-year yield. Yield changes on key rate decision days are compared with changes one week earlier, and the higher variance on decision days serves as the instrument.
2. **Surprises.** On each decision day, the one-day yield changes across maturities are regressed on those sensitivities. The coefficient is the surprise.

The series is in percentage points, scaled to the 2-year yield: a surprise of 1 moves the curve as much as a 1 percentage point change in the 2-year yield.

---

## Download

**[CSV](/files/MonetaryShocksBuRogersWu.csv)** · **[Excel](/files/MonetaryShocksBuRogersWu.xlsx)**

| column | description |
| :-- | :-- |
| `date` | last day of the month |
| `year_month` | the same month, e.g. `2014 Feb` |
| `estimate_brw` | the surprise, in percentage points; summed if a month had two decisions |

The series is monthly from February 2014 to November 2026 and covers 104 months with a key rate decision. Months without a decision are 0. March 2022 is empty: its only decision fell while the Moscow Exchange bond market was closed. A positive value is a tightening surprise.

---

## Data

+ **Yield curve:** the Moscow Exchange zero-coupon yield curve for Russian government bonds (G-curve), daily from January 2014.
+ **Decision dates:** the Bank of Russia schedule of Board of Directors meetings on the key rate.

The R code that downloads the data and estimates the series is in the [GitHub repository](https://github.com/avlsv/BRWRussia).

---

## Citation

If you use the series, please cite Bu, Rogers and Wu (2021) for the method and this page for the Russian series.
