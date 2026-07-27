# Milestone Optimization for Brand Campaigns

A data-driven project that recommends milestone targets and payout distributions for influencer marketing campaigns using historical campaign performance.

---

## Project Overview

Planning milestone ladders manually can be time-consuming and may lead to inconsistent targets across similar campaigns. This project provides a simple, data-driven approach to recommending milestone thresholds based on historical campaign data.

The recommendation considers:

- Campaign category
- Creator tier
- Campaign budget

The project also validates the recommendations through backtesting against historical campaign configurations.

---

## Features

- Recommends milestone view thresholds for new campaigns.
- Generates budget-aware payout distributions.
- Uses historical campaign performance to guide recommendations.
- Handles campaigns with limited historical data using a fallback strategy.
- Includes backtesting to evaluate recommendation quality.
- Interactive notebook for testing different campaign scenarios.

---

## Project Structure

```
.
├── data/
│   ├── campaigns.csv
│   ├── creators.csv
│   ├── posts.csv
│   └── historical_ladders.csv
│
├── Milestone_Optimization.ipynb
├── Report.pdf
├── README.md
└── requirements.txt (optional)
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
git clone https://github.com/<your-username>/<repository-name>.git
cd <repository-name>
```

### 2. Install the required libraries

```bash
pip install pandas numpy matplotlib seaborn
```

### 3. Open the notebook

Using Jupyter Notebook:

```bash
jupyter notebook
```

or upload the notebook to **Google Colab**.

### 4. Add the datasets

Place the following files inside the `data/` folder:

- campaigns.csv
- creators.csv
- posts.csv
- historical_ladders.csv

### 5. Run the notebook

Execute all cells from top to bottom.

---

## Methodology

The recommendation process follows these steps:

1. Load and combine campaign, creator, post, and historical milestone datasets.
2. Group historical campaigns by campaign category and creator tier.
3. Estimate expected campaign performance using historical final view distributions.
4. Generate milestone thresholds using historical percentiles.
5. Allocate the campaign budget across five milestone levels.
6. Validate the recommendations using historical campaign data.

---

## Try It Yourself

The notebook includes an interactive section that allows you to test the recommendation system using your own campaign inputs.

Simply enter:

- **Campaign Category**
- **Creator Tier**
- **Campaign Budget**

The notebook will automatically generate:

- Recommended milestone view thresholds
- Payout amount for each milestone
- Complete milestone ladder
- Total payout validation

This makes it easy to explore different campaign scenarios and understand how the recommendation strategy adapts to different inputs.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Google Colab / Jupyter Notebook

---

## Author

**Ahemed Sakeer Hussain**

B.Tech Computer Science (Data Science)

GitHub: https://github.com/ahemedsh
Portfolio: https://ahemedsh.github.io/portfolio/
