# Analysis of Trader Behavior and Bitcoin Market Sentiment

This project explores the relationship between historical trader behavior data from Hyperliquid and Bitcoin market sentiment using the Fear & Greed Index. The objective is to analyze how trading behavior aligns or diverges from overall market sentiment and identify potential trends or signals for trading strategies.

## Project Structure

The project follows the specified directory structure:

ds_Krishnamurthi/

├── notebook_1.ipynb  # All work is to be done in Google Colab

├── outputs/          # Store all visual outputs, graphs, or charts here.

│   └── *.png / *.jpg # Image results of EDA, charts, etc.

├── ds_report.pdf     # Final summarized insights and explanations.

└── README.md         # This file

## Data Sources

1.  **Historical Trader Data from Hyperliquid:** Provided via a Google Drive link, containing detailed information on individual trades (account, coin, execution price, size, side, timestamp, PnL, etc.).
2.  **Bitcoin Market Sentiment Dataset:** Provided via a Google Drive link, containing daily sentiment classification (Fear/Greed) and a corresponding sentiment value (Fear & Greed Index).

## Analysis Steps

The analysis was conducted in Google Colab following these steps:

1.  **Data Preprocessing:** Cleaned and prepared both datasets, including converting timestamp columns to datetime objects and handling any missing values.
2.  **Feature Engineering:** Created new features such as the date component from timestamps, trade types (combining side and direction), daily aggregated trade volume and average PnL per account, and a numerical sentiment score.
3.  **Data Merging:** Combined the trader data and sentiment data based on the date to create a unified dataset for analysis.
4.  **Exploratory Data Analysis (EDA):** Explored the distributions of key variables (trade size, PnL, sentiment) and visualized initial patterns and correlations using summary statistics, histograms, box plots, and scatter plots.
5.  **Relationship Analysis:** Analyzed the relationship between sentiment metrics and trading behavior metrics using correlation analysis and ANOVA tests to determine the statistical significance of observed differences across sentiment classifications.
6.  **Identifying Hidden Trends/Signals:** Investigated potential lag effects of sentiment on trading behavior and explored distinct trading patterns of individual accounts under different sentiment conditions.

## Key Findings

*   Market sentiment has a statistically significant impact on both daily trading volume and average daily profitability.
*   Higher average daily total trade sizes were observed during 'Fear' and 'Neutral' sentiment periods, counter to the intuition that high greed would correlate with high volume.
*   'Extreme Greed' sentiment correlated with the highest average daily closed PnL, suggesting potential profit opportunities during periods of high market optimism.
*   Specific trade types exhibited varying profitability across different sentiment classifications, highlighting the importance of tailoring trading strategies to market sentiment.
*   Simple lagged sentiment did not show a strong correlation with subsequent daily trading volume or profitability.
*   Analysis of individual accounts revealed that some traders consistently achieved higher profitability during specific sentiment conditions, such as 'Extreme Fear'.

For a more detailed explanation of the findings, please refer to the `ds_report.pdf`.

## Setup and Running the Notebook

1.  **Clone the Repository:** Clone this GitHub repository to your local machine.
2.  **Open in Google Colab:** Open the `notebook_1.ipynb` file in Google Colab.
3.  **Run the Cells:** Execute the cells in the notebook sequentially. The notebook contains all the code used for data loading, preprocessing, analysis, and visualization.
4.  **Generated Outputs:** Running the notebook will generate plot images and save them to the `outputs/` directory within the repository structure.

## Report

The `ds_report.pdf` file provides a summarized overview of the analysis, key findings, and potential implications for trading strategies.

---

**Note:** The datasets used in this analysis were provided via Google Drive links as part of the assignment. Ensure you have access to these links when running the notebook.

