# AI-Prod

This project explores stock price data from Kaggle's **Massive Yahoo Finance Dataset**. The notebooks demonstrate simple data analysis using Python.

## Project Goal

The goal is to load the historical price information for hundreds of companies and inspect basic statistics such as the date ranges available, missing values and counts for each ticker. The provided notebooks show how to parse the CSV and perform a few summary operations.

## Environment Setup

1. Install Python 3. A version >=3.8 is recommended.
2. Create and activate a virtual environment:
   ```bash
   python -m venv .venv
   source .venv/bin/activate
   ```
3. Install the required packages:
   ```bash
   pip install pandas scikit-learn matplotlib
   ```

These packages are enough to execute the notebooks.

## Downloading the Data

The notebooks expect the CSV to live at:
```
./kaggle/input/massive-yahoo-finance-dataset/stock_details_5_years.csv
```

1. Install the Kaggle CLI if you haven't already: `pip install kaggle`.
2. Obtain a Kaggle API token from your Kaggle account page and place the credentials file in `~/.kaggle/kaggle.json`.
3. Download the dataset:
   ```bash
   kaggle datasets download -d gstoner/massive-yahoo-finance-dataset -p kaggle/input/massive-yahoo-finance-dataset --unzip
   ```
   This command puts `stock_details_5_years.csv` in the expected folder.

## Running the Notebook

Launch Jupyter and open `Stock.ipynb` (or `ai-prodject.ipynb`). Run the cells in order. The first cell reads the CSV and prints its shape. Subsequent cells show information about missing values and coverage per ticker.

The output tables help you understand how many records exist for each company and the overall time span of the dataset. You can modify the notebook to perform your own analyses using pandas, scikit-learn or matplotlib for plotting.

