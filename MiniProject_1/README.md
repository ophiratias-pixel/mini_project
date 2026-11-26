# Mini-Project 1: Neural Spikes and Laptop Data Analysis

This repository contains the two parts of **Neuroscience Data Analysis with Python – Mini-Project #1**.

## Files

- `Q1_neural_spikes.ipynb` — simulation and analysis of regular, irregular and bursting neural spike trains, including spike plots, inter-spike intervals, validation and new stochastic realizations.
- `Q2_laptop_analysis.ipynb` — audit, cleaning and exploratory analysis of a laptop dataset; comparisons of RAM, price, screen size, weight and manufacturers; and an investigation of unusual observations.
- `laptop_price_dataset.csv` — input data for Question 2 (1,275 laptops).
- `figures/` — selected figures exported from the notebooks.
- `requirements.txt` — Python packages needed to run the notebooks.
- `AI_USAGE.md` — description of AI assistance and how its suggestions were checked.

## How to run

Use Python 3. Open a terminal **inside this `MiniProject_1` directory** and install the dependencies:

```bash
python -m pip install -r requirements.txt
```

Then start Jupyter:

```bash
jupyter notebook
```

Open and run each notebook from top to bottom, in order. The Question 2 notebook reads `laptop_price_dataset.csv` from the same directory; no absolute path is required.

For a reproducibility check, use **Restart Kernel and Run All Cells** in each notebook. Question 1 uses explicit random number generator seeds for its stochastic examples. Question 2 analyses the supplied dataset without downloading data from the internet.

## Key results from Question 2

- RAM and price have a positive sample correlation of approximately 0.74.
- Screen size and weight have a positive sample correlation of approximately 0.83.
- The full dataset has 28 high-price observations flagged by the 1.5 × IQR rule.
- The RAM analysis flags 21 observations above a Z-score of 3; 12 of these are also high-price outliers.
- Removing price outliers changes summary statistics and the comparison of average prices across manufacturers. This is a sensitivity analysis, not an assertion that excluded prices are incorrect.

The notebook includes the interpretation and limitations of these findings. Correlations do not establish causation, and some manufacturer samples are small.
