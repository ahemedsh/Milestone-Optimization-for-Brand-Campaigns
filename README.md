# Milestone Optimization for Brand Campaigns

A data-driven project that recommends milestone targets and payout distributions for influencer marketing campaigns using historical campaign performance.

---

## Project Overview

Planning milestone ladders manually can be time-consuming and may lead to inconsistent targets across similar campaigns. This project provides a simple, data-driven approach to recommending milestone thresholds based on historical campaign data.

The recommendation considers:

- **Campaign Category** (e.g., Gaming, Fashion, Tech, Beauty, FMCG, D2C)
- **Creator Tier** (Macro, Micro, Mid, Nano)
- **Campaign Budget**

The project also validates the recommendations through rigorous backtesting against historical campaign configurations and post performance.

---

## Features

- Recommends milestone view thresholds for new campaigns using historical distribution percentiles (20th to 90th).
- Generates budget-aware payout distributions (10%, 15%, 20%, 25%, 30%).
- Employs historical campaign performance to guide data-driven recommendations.
- Handles campaigns with limited historical data using a progressive fallback strategy.
- Includes backtesting to evaluate recommendation quality, budget safety (100% compliance), and creator completion rates.
- Interactive notebook interface for testing different campaign scenarios.

---

## Project Structure

```
.
├── campaigns.csv
├── creators.csv
├── posts.csv
├── historical_ladders.csv
├── Milestone_Optimization_for_Brand_Campaigns.ipynb
├── Report.pdf
└── README.md
```

---

## Requirements

- Python 3.10 or later
- Jupyter Notebook or Google Colab

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn
```

---

## Setup & Run

### 1. Clone the repository

```bash
git clone https://github.com/ahemedsh/Milestone-Optimization-for-Brand-Campaigns.git
cd Milestone-Optimization-for-Brand-Campaigns
```

### 2. Install the required libraries

```bash
pip install pandas numpy matplotlib seaborn
```

### 3. Open the notebook

Using Jupyter Notebook:

```bash
jupyter notebook Milestone_Optimization_for_Brand_Campaigns.ipynb
```

or upload `Milestone_Optimization_for_Brand_Campaigns.ipynb` to **Google Colab**.

### 4. Datasets

Ensure the following CSV dataset files are placed in the root directory (same folder as the notebook):

- `campaigns.csv`
- `creators.csv`
- `posts.csv`
- `historical_ladders.csv`

*(Note: If missing, the notebook will automatically generate clean sample datasets on first execution.)*

### 5. Run the notebook

Execute all cells from top to bottom (**Kernel $\rightarrow$ Restart & Run All**).

---

## Methodology

The recommendation process follows these steps:

1. **Data Ingestion & Cleaning**: Load and combine campaign, creator, post, and historical milestone datasets.
2. **Segmentation**: Group historical campaigns by campaign category and creator tier.
3. **Distribution Modeling**: Estimate expected campaign performance using historical final view distributions.
4. **Quantile Placement**: Generate milestone thresholds at the 20th, 40th, 60th, 80th, and 90th percentiles of expected views.
5. **Budget Allocation**: Allocate the campaign budget across five milestone levels ($10\%, 15\%, 20\%, 25\%, 30\%$).
6. **Backtesting & Validation**: Validate the recommendations against historical campaign performance and budget constraints.

---

## Try It Yourself

The notebook includes an interactive section that allows you to test the recommendation system using your own campaign inputs.

Simply enter:

1. **Select Category** (e.g., Gaming, Fashion, Tech)
2. **Select Creator Tier** (Macro, Micro, Mid, Nano)
3. **Enter Campaign Budget** (e.g., ₹400,000)

The notebook will automatically generate:

- Recommended milestone view thresholds
- Payout amount for each milestone
- Complete 5-stage milestone ladder
- Total budget validation

---

## Technologies Used

- **Python 3.10+**
- **Pandas** & **NumPy** (Data processing & statistical modeling)
- **Matplotlib** & **Seaborn** (Exploratory Data Analysis)
- **Jupyter Notebook / Google Colab** (Interactive environment)

---

## Author

**Ahemed Sakeer Hussain**  
*B.Tech Computer Science (Data Science)*  

- **GitHub**: [github.com/ahemedsh](https://github.com/ahemedsh)  
- **Portfolio**: [ahemedsh.github.io/portfolio](https://ahemedsh.github.io/portfolio/)
