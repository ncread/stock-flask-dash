# Stock Information Project

A web application written in Python, leveraging the Flask framework.


## Overview

This web application receives user-inputted market tickers (AAPL, NVDA, etc.) and timeframe (6 months, 1 year, etc.) and displays the following:

* Correlation matrix including asset return correlations for provided tickers over the provided timeframe
* Table with current share price, 5-year beta value, market cap, trailing & forward price-to-earnings ratios, and upcoming earnings date (if applicable)
* time-series price graphs with share price, 10, 50 and 200-day simple and exponential moving average prices, and upper and lower Bollinger bands.

Graphics on the webapp are plotly express images, so they are able to be downloaded at the click of a button to share or use elsewhere. The time-series charts are interactive, allowing users to toggle whatever metrics they would like to see and to hover over each chart for specific prices.

## Project Structure
```
stock-flask-dash/
├── get_data.py
├── main.py
├── Procfile #necessary for Render deployment
├── pyproject.toml
├── README.md
├── requirements.txt
├── static
│   └── styles.css
├── templates
│   └── index.html
└── uv.lock
```

## Other

The initial plan was to try out Vercel for the first time to host this project, yet I came across a few pitfalls related to the storage size of the entire application (including dependencies). I wasn't able to reduce the storage size of the app enough to fit within the 250 MB requirements, so Render was utilized instead of Vercel. Along with UptimeRobot to avoid cold starts by the Render server, the free tier of Render is suitable, however I have run into fairly frequent issues pinging the Yahoo Finance servers through Render's IP address. Knowing a little more about what Vercel expects will be helpful for future projects down the line.

Thanks for reading, and enjoy the web app! I hope it will be useful to others. Please feel free to reach out with thoughts or improvements.
