# Certainty Classifier: Analyzing Speculative Language in Scientific Abstracts

## Overview

This project aims to analyze the **degree of certainty or speculation** expressed in the **abstracts of scientific papers**. Abstracts summarize a paper’s findings and often signal how confident the authors are in their conclusions. Measuring this tone can provide valuable insights, especially in **fields like environmental science**, where research findings may be nuanced, controversial, or evolving.

## Problem Motivation

Scientific communication doesn't always express findings with the same degree of confidence. By quantifying how speculative or definitive a paper’s abstract is, we can help readers better interpret the certainty of scientific claims—whether they are **exploratory observations** or **definitive conclusions**. This is particularly important for complex domains such as **climate change, sustainability, and environmental policy**, where interpretation can influence public perception and decision-making.

## Certainty Categories

We defined four certainty levels based on the **strength of claims** in each abstract:

* **Exploratory** – tentative observations, early-stage ideas
* **Hypothetical** – includes assumptions or models that are not yet tested
* **Evidential** – supported by data but framed with some caution
* **Definitive** – strong, confident claims backed by clear evidence

## Data Collection

We curated our dataset from [EarthArXiv](https://eartharxiv.org/), a preprint server for Earth and environmental sciences. Our filtering criteria:

* Keyword: “Environmental Science”
* Year: Papers published after 2015
* Max 5 papers per author to increase diversity
* Only included open-access papers with clear licensing

## Modeling Approach

We trained an **ordinal regression classifier** to predict the certainty level of an abstract based on its text. The model reflects the **ordered nature** of the labels (i.e., Exploratory < Hypothetical < Evidential < Definitive).

Input features:

* **Bag-of-Words** (presence and count of terms)
* **Certainty Keywords** (e.g., "might," "suggests," "demonstrates")
* **Pretrained Embeddings** using models like TinyBERT

## Contributors

* **Stephanie Yew**
* **Raina Park**
* **Hanen Su**
* * **Melody Miao**

