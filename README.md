# Tech Employee Mental Health and Burnout: Exploratory Data Analysis

An exploratory data analysis (EDA) project studying workplace, demographic, and well-being measures for employees in the technology sector. The Jupyter notebook combines data inspection with a broad set of visualizations to explore burnout, stress, work patterns, and mental-health-related measures.

> **Important:** This is an exploratory visualization project, not a clinical assessment or a causal study. Charts show patterns in the supplied dataset; they do not establish that one factor causes another.

## Project Contents

| File | Description |
| --- | --- |
| `eda_tech_visualisation.ipynb` | Notebook containing data inspection, 32 implemented chart examples, interpretations, and a glossary of additional chart types. |
| `mental_health_burnout_tech_2026.csv` | Dataset loaded by the notebook. |

## Analysis Overview

The notebook begins with basic inspection, including sample rows, data types, descriptive statistics, and missing-value checks. It then explores distributions, group comparisons, relationships, and composition across employee and workplace attributes.

Implemented visualizations include:

- **Distributions:** histogram, density plot, box plot, violin plot, Q-Q plot, swarm plot, strip plot, and jitter plot.
- **Category comparisons and composition:** pie and donut charts, bar and column charts, stacked and grouped bars, heatmap, lollipop chart, and Pareto chart.
- **Relationships and trends:** line and multi-line charts, dual-axis and combo charts, area and stacked-area charts, scatter and bubble charts, correlation chart, parallel-coordinates plot, and slope chart.
- **Hierarchical views:** treemap and sunburst chart.

The notebook also includes definitions and intended uses for additional chart types. Those glossary entries are explanatory and are not implemented visualizations in this analysis.

## Dataset

The CSV contains employee-level records with fields covering:

- **Demographics and employment:** age, gender, country, job role, seniority, experience, tenure, company size, industry, and work mode.
- **Work conditions:** salary, weekly work hours, meetings per day, team size, deadline pressure, autonomy, manager support, and work-life balance.
- **Well-being:** sleep, exercise, vacation, job satisfaction, social support, stress, and burnout scores.
- **Mental-health-related measures:** PHQ-9 and GAD-7 scores and categories, therapy access and use, and whether support is sought.
- **Career intentions and tools:** job-change intention and daily AI-tool use.

The CSV's first column is `employee_id`. The notebook reads it as the DataFrame index (`index_col=0`), rather than as an analysis feature.

The dataset's origin, collection method, license, and representativeness are not documented in the files currently included in this repository. Verify that you have permission to redistribute it before making the repository public. If records are real or could identify individuals, remove or appropriately protect them before publishing.

## Requirements

- Python 3
- Jupyter Notebook support (for example, JupyterLab or the VS Code Jupyter extension)
- `pandas`, `matplotlib`, `seaborn`, `plotly`, and `scipy`

Install the Python packages with:

```bash
python -m pip install pandas matplotlib seaborn plotly scipy jupyter
```

## Getting Started

1. Clone the repository and enter its directory:

   ```bash
   git clone <your-repository-url>
   cd <repository-directory>
   ```

2. Install the requirements shown above.

3. Open `eda_tech_visualisation.ipynb` in JupyterLab or VS Code and select the Python environment where the packages were installed.

4. Before running the notebook, update its CSV-loading cell. It currently points to a machine-specific path; use the CSV's repository-relative path instead:

   ```python
   df = pd.read_csv("mental_health_burnout_tech_2026.csv", header=0, index_col=0)
   ```

5. Run the notebook from top to bottom. Plotly charts are interactive when rendered in a compatible notebook environment.

## Reproducibility Notes

- Keep the notebook and CSV in the same directory, or adjust the CSV path to match your repository layout.
- The notebook samples rows with a fixed `random_state` in selected plots so those samples are repeatable.
- Dependency versions are not pinned in this project. For a reproducible environment, record the package versions you use in a `requirements.txt` file.
- Some plots summarize groups by experience, job role, industry, work mode, or seniority; results depend on the supplied data and its category coverage.

## Responsible Interpretation

Mental-health measures are sensitive and should be handled with care. Avoid drawing conclusions about individuals or groups from these visual summaries alone. Consider sample size, missing data, how scores were collected, and possible confounding factors before interpreting apparent differences. Do not use this notebook as a diagnostic or employment decision-making tool.

## License

No project or dataset license is included in the current files. Add an appropriate license only after confirming that you have the rights to license both the code and any data you publish.