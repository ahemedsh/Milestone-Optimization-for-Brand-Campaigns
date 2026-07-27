# Milestone Optimization for Brand Campaigns

A data-driven approach for recommending milestone targets and payouts for influencer marketing campaigns using historical campaign performance.

## Overview

This project recommends milestone ladders for new influencer campaigns based on historical data. The recommendation considers campaign category, creator tier, and campaign budget to generate realistic milestone thresholds while keeping payouts within the allocated budget.

The project also includes backtesting to compare the recommended milestone ladders with historical configurations.

## Features

- Recommends milestone view thresholds for new campaigns.
- Generates budget-aware payout recommendations.
- Handles campaigns with limited historical data using fallback logic.
- Validates recommendations through backtesting.
- Interactive notebook for testing different campaign scenarios.

## Project Structure

```
.
├── data/
│   ├── campaigns.csv
│   ├── creators.csv
│   ├── posts.csv
│   └── historical_ladders.csv
├── Milestone_Optimization.ipynb
├── report.pdf
└── README.md
```

## Requirements

- Python 3.10+
- Jupyter Notebook or Google Colab

### Python Libraries

Install the required packages using:

```bash
pip install pandas numpy matplotlib seaborn
```

## Running the Project

1. Clone the repository.

```bash
git clone <repository-url>
cd <repository-folder>
```

2. Install the required libraries.

```bash
pip install pandas numpy matplotlib seaborn
```

3. Open the notebook.

```bash
jupyter notebook
```

or upload the notebook to **Google Colab**.

4. Place the datasets inside the `data/` folder.

5. Run the notebook from top to bottom.

6. At the end of the notebook, enter:

- Campaign Category
- Creator Tier
- Campaign Budget

The notebook will generate the recommended milestone thresholds and payout amounts.

## Methodology

The recommendation process:

- Combines historical campaign, creator, post, and milestone data.
- Groups similar campaigns using campaign category and creator tier.
- Uses historical view distributions to recommend milestone thresholds.
- Allocates the campaign budget across five milestones.
- Validates the recommendations using historical campaign data.

## Results

The notebook includes:

- Sample milestone recommendations
- Backtesting against historical milestone ladders
- Budget validation
- Summary evaluation metrics

## Author

**Ahemed Sakeer Hussain**
