# real_estate_metrics_analysis

## Data Collection

Data was collected from realtor.com's Hotness Inventory Metrics, Federal Reserve Economic Data's (FRED) API, and Zillow's Price Index through the Nasdaq Data Link API. For each of the three metrics analyzed, different steps were taken to collect the metric data. Price data was collected from Zillow's All Homes Price Index. The exact procedure and code can be found in the processData notebook.

## Cleansing Data

Multiple cleaning procedures were carried out in order to analyze the data such as:
- Removing null and infinite values
- Formatting location strings to only include city and state abbreviations separated by comma
- Skipping locations which don't have sufficient price data for backtesting
- And more

## Analyzing Data

Each metric was analyzed by calculating the compound annual growth rate(CAGR) of housing prices for each region. A backtest period of 5 years was used for each metric. Regions were ranked by metric score and compared against CAGR using a correlation coefficent- np.corrcoef.
