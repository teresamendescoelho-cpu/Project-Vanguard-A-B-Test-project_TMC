# Sources

This document records the main data source, tools, documentation, and project-management resources used in the **Vanguard A/B Test — Project 2**.

## 1. Dataset

### Marketing A/B Testing Dataset

- **Dataset used:** `marketing_AB.csv`
- **Cleaned dataset:** `marketing_AB_clean.csv`
- The cleaned dataset was produced during the data-cleaning and preparation stage of the project and was used for the analysis and Tableau visualizations.
- The repository currently contains the dataset files used in the project.

> **Note:** The original external URL/provenance of `marketing_AB.csv` is not documented in the current project files. It is therefore intentionally not attributed here to a specific external website rather than guessing the source.

## 2. Analysis & Development Tools

### Python

Used for data preparation, exploration, analysis, calculations, and statistical testing.

- Python documentation: https://docs.python.org/3/

### Pandas

Used for loading, cleaning, transforming, and analysing the dataset.

- Pandas documentation: https://pandas.pydata.org/docs/

### NumPy

Used for numerical operations and calculations.

- NumPy documentation: https://numpy.org/doc/

### Matplotlib

Used for data visualisation during the analysis.

- Matplotlib documentation: https://matplotlib.org/stable/

### Seaborn

Used for statistical and exploratory visualisations.

- Seaborn documentation: https://seaborn.pydata.org/

### Jupyter Notebook

Used to document and execute the Python analysis.

- Jupyter documentation: https://docs.jupyter.org/

## 3. Tableau

Tableau was used to create the project's interactive visualisations and dashboards, including:

- **Marketing A/B Test Performance Dashboard**
- **A/B Test Group Performance**
- **Advertising Performance by Hour**

The Tableau workbook is included in the repository:

`Project-Vanguard-A-B-Test-project_TMC.twb`

- Tableau documentation: https://help.tableau.com/

## 4. Version Control

### Git

Used for version control and project development.

- Git documentation: https://git-scm.com/doc

### GitHub

Used to host the project repository, notebooks, datasets, documentation, and Tableau workbook.

- Project repository: https://github.com/teresamendescoelho-cpu/Project-Vanguard-A-B-Test-project_TMC
- GitHub documentation: https://docs.github.com/

## 5. Project Management

### Trello

Trello was used to organise the project workflow, hypotheses, Tableau work, documentation, and final deliverables.

- Project board: https://trello.com/b/UhyhqfFE/vanguard-a-b-test-project-2

## 6. Project Documentation

The main project documentation is available in:

- `README.md` — project overview, methodology, analysis, findings, and conclusions.
- `notebooks/Marketing_AB_Test_Analysis.ipynb` — Python analysis and data preparation.
- `Project-Vanguard-A-B-Test-project_TMC.twb` — Tableau workbook containing the project's visualisations and dashboards.

## 7. Reproducibility

The project uses the files and tools listed above to make the analysis reproducible. Python dependencies are documented in `requirements.txt`, while temporary files, virtual environments, and other local development files are excluded through `.gitignore`.
