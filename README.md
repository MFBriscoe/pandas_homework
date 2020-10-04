# pandas_homework
Jupyter Notebook and ReadMe version

 #  A Whale off the Port(folio)

 In this assignment, you'll get to use what you've learned this week to evaluate the performance among various algorithmic, hedge, and mutual fund portfolios and compare them against the S&P 500.
 
```

import pandas as pd
import numpy as np
import datetime as dt
from pathlib import Path
%matplotlib inline

```

## Data Cleaning

In this section, you will need to read the CSV files into DataFrames and perform any necessary data cleaning steps. After cleaning, combine all DataFrames into a single DataFrame.

Files:

* whale_returns.csv
* algo_returns.csv
* sp500_history.csv

### Whale Returns
Read the Whale Portfolio daily returns and clean the data

```
####### Reading whale returns

`whale_returns_csv = Path("Resources/whale_returns.csv")`
###### YOUR CODE HERE
`whale_returns_df = pd.read_csv(whale_returns_csv, index_col=['Date'], parse_dates=True, infer_datetime_format=True)
whale_returns_df.head()`

`# Count nulls
###### YOUR CODE HERE
whale_returns_df.isnull().sum()`