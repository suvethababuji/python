import yfinance as yf
import pandas as pd
apple = yf.Ticker("AAPL")
import json
with open('apple.json') as json_file:
    apple_info = json.load(json_file)
    # Print the type of data variable    
    print("Type:", type(apple_info))
apple_info
apple_share_price_data = apple.history(period="max")
apple_share_price_data = apple.history(period="max")
apple_share_price_data.head()
apple_share_price_data.plot(x="Date", y="Open")
