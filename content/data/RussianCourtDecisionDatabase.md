---
title: "Database of Russian Courts Decisions" 
date: 2023-03-07
tags: ["courts", "law"]
author: ["Alexander Vlasov"]
description: "This dataset contains all available records of decisions of Russian criminal courts from 2008 to 2022."
summary: "This dataset contains all available records of decisions of Russian criminal courts from 2008 to 2022."
editPost:
    URL: "https://github.com/avlsv/RussianCourtsProject"
    Text: "GitHub repository"
showToc: true
disableAnchoredHeadings: false

---

## Overview

Using [sudrfscraper](https://github.com/tochno-st/sudrfscraper), scrapper of Russian court system, I have collected big ($> 150$ gb) database of records of decisions, that criminal courts of Russia have reached, starting from January 2008 (the start of a unified electronic database was around that time, but the coverage is sparse) to September 2023. Most of the database is text. If you are interested in its entirety, contact me via mail [avlasov@nes.ru](mailto:avlasov@nes.ru). 

Since the database is large, I'm sharing a random samples of 30,000 records (if available) 2015-01-01 to 2022-01-01.  

---


## View dataset

You can find the samples in [this github folder](https://github.com/avlsv/RussianCourtsProject/tree/main/Courts/Datasets). 

It contains 5 csv files:

+ all_articles.csv : 30,000 random records 2015-01-01 to 2022-01-01.
+ all_articles1.csv : another random sample with the same restrictions as above.
+ article_105.csv : 30,000 random court cases of murders (105th article of Russian criminal code, Статья 105 УК РФ)
+ article_159.csv : 30,000 random court cases of fraud (159 article of Russian criminal code, Статья 159 УК РФ)
+ article_228.csv : 30,000 random court cases of drug related crimes (228th article of Russian criminal code, Статья 228 УК РФ)

---

## Source of data

Data was collected using [sudrfscraper](https://github.com/tochno-st/sudrfscraper) and **a lot** of time.

---
<!-- 
## Using data with Python

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

### Start Python:

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua.

```python
import numpy as np
import pandas as pd
```

### Open the file:

Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat `data.csv`.

```python
file_path = 'data.csv'
with open(file_path, 'r') as file:
```

### Read data:

Duis aute irure dolor in reprehenderit in voluptate velit esse
cillum dolore eu fugiat nulla pariatur.

```python
    lines = file.readlines()
```

### Parse and process data:

Duis aute `line_data` irure dolor in reprehenderit in voluptate velit esse
cillum dolore eu fugiat nulla pariatur `data.extend`.

```python
data = []
for line in lines:
    line_data = line.strip().split(',')  # Split the line into a list of values
    line_data = [float(value) for value in line_data]  # Convert values to floats
    data.extend(line_data)  # Extend the main list with values from the line
```

#### Compute summary statistics using NumPy:

Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum: `data_array`. 

```python
data_array = np.array(data)  # Convert the list to a NumPy array
mean = np.mean(data_array)
median = np.median(data_array)
std_dev = np.std(data_array)
min_value = np.min(data_array)
max_value = np.max(data_array)
```

#### Display summary statistics:

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
consequat `print`.

```python
print(f"Mean: {mean}")
print(f"Median: {median}")
print(f"Standard Deviation: {std_dev}")
print(f"Minimum Value: {min_value}")
print(f"Maximum Value: {max_value}")
```

---

## Description of simulation parameters

| Parameter |   Value   |  Language  | Time period |           Description            |
| :-------: | :-------: | ---------- | :---------: | :------------------------------: |
|  $\alpha$ |   $1/2$   | French     |  1930–1954  |         Tempor dolor in          |
| $\lambda$ |   $e/2$   | French     |  1930–1954  |       Fugiat sint occaecat       |
|  $\gamma$ |  $\ln(3)$ | Spanish    |  1833–1954  |      Duis officia deserunt       |
|  $\omega$ | $10^{-4}$ | Italian    |  1930–1994  | Excepteur et dolore magna aliqua |
|  $\sigma$ |   $1.5$   | Portuguese |  1990–2023  |         Lorem culpa qui          |
|  $\chi^2$ |  $\pi^2$  | Portuguese |  1990–2023  |         Labore et dolore         |  -->
