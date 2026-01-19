# Data Science Assignment: Trader Behavior Insights

## Project Structure

```
ds_praneeth_reddy_bokka/
├── notebook_1.ipynb       # Main analysis notebook (Jupyter/Colab compatible)
├── csv_files/             # Raw and processed data files
│   ├── historical_data.csv
│   ├── fear_greed_index.csv
│   └── processed_daily_data.csv
├── outputs/               # Generated Visualizations
│   ├── Tradingvol_vs_Marketsentiment.png
│   |── Tradingvol_vs_FearGreedIndex.png
|   └──TotalPnL_by_MarketSentiment.png
├── ds_report.md           # Final Summary Report
└── README.md              # Project documentation
```

## How to Run
1.  **Open the Notebook**: Launch `notebook_1.ipynb` in Jupyter Notebook or Google Colab.
2.  **Dependencies**: Ensure the following Python libraries are installed:
    ```bash
    pip install pandas matplotlib seaborn
    ```
3.  **Execution**: Run all cells in the notebook.

## Analysis Overview
The code aligns daily trading metrics (Volume, PnL, Long/Short Ratio) with the Fear & Greed Index to visualize correlations between market sentiment and trader effectiveness.

