# Introduction to Data Science with Python

Completed on **6 October 2026**, using the examples in *Lab_Intro_to_data.pdf*. This lab covers data types, descriptive statistics and histogram plotting.

## Files

- [Completed notebook](intro_to_data.ipynb) - commented code, explanations and executed results.
- [Histogram](histogram.png) - the worksheet's five-bin histogram.
- [Return to the module repository](../../README.md)

## Running the exercise

Open the notebook in JupyterLab or VS Code, select **Python (University)**, and run the cells in order. The environment contains NumPy, pandas, Matplotlib and SciPy; SciPy was installed for this lab.

If these packages are missing from another notebook environment, run:

```python
%pip install numpy pandas matplotlib scipy
```

Restart that kernel after installation if required, then run the notebook from the top.

## Completed work

- Distinguished continuous measurements, discrete counts, nominal categories and ordinal ratings.
- Displayed the worksheet's examples in a pandas table, including an ordered categorical rating column.
- Calculated the mean, median, mode, variance and standard deviation.
- Updated the worksheet's mode calculation for current SciPy using `keepdims=False` and `.mode.item()`.
- Explained population statistics (`ddof=0`) and compared them with sample statistics (`ddof=1`).
- Plotted the five-bin histogram and saved the figure.

## Dataset and results

The statistics dataset is `[0, 2, 3, 2, 1, 0, 0, 2, 0]`.

| Statistic | Result |
| --- | ---: |
| Observations | 9 |
| Mean | 1.111111 |
| Median | 1 |
| Mode | 0 (4 occurrences) |
| Population variance | 1.209877 |
| Population standard deviation | 1.099944 |

Values 0, 1, 2 and 3 occur 4, 1, 3 and 1 times respectively. The histogram contains all nine observations. Its five equal-width bins produce one empty interval because the data contain only four distinct integer values.

The statistics describe the supplied example data; this lab does not train a predictive model.

## Reference

The worksheet is *Lab_Intro_to_data.pdf*. The mode calculation follows the [SciPy documentation](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.mode.html).
