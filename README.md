# Tesla vs GameStop: Share Price and Revenue Analysis

Python analysis of Tesla and GameStop share prices and quarterly revenue, covering return, risk and the link between revenue and price. Started as the final assignment of the IBM *Python Project for Data Science* course and extended with my own analysis.

## Business questions
1. How did each company's share price and revenue evolve?
2. Which stock returned more, and which was riskier?
3. Does quarterly revenue move together with the share price?

## Data
- **Share prices:** Yahoo Finance via the `yfinance` library (TSLA, GME), daily, up to 14 June 2021.
- **Revenue:** quarterly revenue scraped with `requests` and `BeautifulSoup` from static HTML pages provided in the IBM course.

## Approach
1. Extracted prices with `yfinance` and scraped revenue tables.
2. Cleaned the data: removed `$` and `,`, dropped empty rows, converted types, removed timezones from dates.
3. Built interactive Plotly charts of price and revenue.
4. Calculated total and annualised return, volatility and maximum drawdown.
5. Compared both stocks rebased to 100, and tested the correlation between quarterly revenue and quarter-end price.

## Key findings
- Tesla returned 12,828% from June 2010 to June 2021 (about 56% a year), against 3,291% for GameStop since 2002 (about 20% a year).
- GameStop was far riskier: 79% volatility and a 93% maximum drawdown, against 57% and 61% for Tesla.
- Tesla's revenue grew every year (from $116M in 2010 to $31.5B in 2020). GameStop's revenue fell from its 2011 peak of $9.7B to $7.3B in 2019.
- Tesla's price and revenue trended together (r = 0.81), but quarterly changes were unrelated (r = -0.07). For GameStop the link was weak throughout (r = 0.19).

## How to run
```bash
pip install -r requirements.txt
jupyter notebook tesla_gamestop_analysis.ipynb
```
Or upload the notebook to Google Colab and choose Runtime, then Run all.

## Limitations
- Revenue data ends in 2021, so the comparison stops at 14 June 2021.
- Correlation does not prove causation. Not financial advice.

## Credits
Based on the IBM Python Project for Data Science course. Analysis and extensions by Damaris Nafula Barasa.

## About me
Damaris | LinkedIn: [LinkedIn](https://www.linkedin.com/in/damaris-barasa-9b543223b/) | Portfolio: [Portfolio](https://damarisbarasa662.wixsite.com/data-analyst-portfol)
