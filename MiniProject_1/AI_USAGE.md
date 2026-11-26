# AI Usage Documentation

## AI tools used

I used **ChatGPT (OpenAI)** while working on this mini-project.

## Tasks where I used AI assistance

- Understanding Python, NumPy, Pandas and Matplotlib commands and their arguments.
- Discussing possible analysis strategies, visualizations, validation checks and scientific interpretation.
- Debugging and checking code examples, including Pandas selection, `groupby()`, `mean()`, `quantile()`, Z-scores and plotting.
- Reviewing and correcting English spelling and grammar in Markdown explanations.
- Organizing the submission files and testing the notebooks in a clean execution order.

## Examples of suggestions or code explained by AI

The following are examples of AI-suggested or AI-explained techniques that I used or adapted:

```python
average_prices = laptops.groupby("Company")["Price (Euro)"].mean()
```

This groups laptop observations by manufacturer and calculates the mean price within each group.

```python
q1 = laptops["Price (Euro)"].quantile(0.25)
q3 = laptops["Price (Euro)"].quantile(0.75)
iqr = q3 - q1
upper_limit = q3 + 1.5 * iqr
lower_limit = q1 - 1.5 * iqr
```

These lines calculate the interquartile range and its lower and upper fences, used to flag potential price outliers.

```python
ram_z = (laptops["RAM (GB)"] - ram_mean) / ram_std
high_ram_z = ram_z[ram_z > 3]
```

This calculates Z-scores for RAM values and selects the values more than three sample standard deviations above the mean.

## How I checked AI suggestions

- Compared Pandas transformations with `value_counts()`, looked at unique pairs of source `Memory` values and derived storage types, and checked that every relevant storage combination was classified.
- Checked the operating-system grouping and that Windows versions were grouped consistently, not just Mac OS names.
- Ran the notebooks in order, checked the actual outputs and plots, and compared the numbers in the text with computed correlations, counts, means and medians.
- Considered whether conclusions were supported by the data and made clear that outliers are not necessarily errors and that correlation is not causation.

## Example of an AI suggestion that I challenged or corrected

During the operating-system cleaning, an early AI suggestion focused on combining Mac operating-system labels but did not consistently group the Windows versions. I noticed this, challenged the suggestion, and updated the mapping before validating it. A separate storage classification check also revealed that mixed Flash Storage + HDD entries needed explicit handling. I checked the resulting mappings against the dataset rather than assuming that working code was necessarily correct.

## Responsibility for submission

I reviewed and checked the methods and interpretations used in this work. AI assistance is documented here rather than presented as entirely unaided work.
