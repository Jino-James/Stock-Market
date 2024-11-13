# ANALYSIS
## Objective
Tracking the adjusted close prices of prominent stocks over time provides valuable insights into the trends and volatility of key companies. In this project, we focus on four major stocks: HDFC Bank (HDFCBANK.NS), Infosys (INFY.NS), Reliance (RELIANCE.NS), and TCS (TCS.NS), examining how their adjusted close prices have evolved. By visualizing these trends, we aim to understand the comparative stability and growth of each stock, which is crucial for investors and analysts.

### Code
```python
df['Date'] = pd.to_datetime(df['Date'])
df.set_index('Date', inplace = True)

plt.figure(figsize = (14,7))
sns.set(style = 'whitegrid')

sns.lineplot(data = df, x='Date', y='Adj Close', hue='Ticker', marker = 'o')

plt.title('Adjusted Close Price Over Time', fontsize=16)
plt.xlabel('Date', fontsize=14)
plt.ylabel('Adjusted Close Price', fontsize=14)
plt.legend(title='Ticker', title_fontsize='13', fontsize='11')
plt.grid(True)

plt.xticks(rotation=45)

plt.show()
```
### Results



### Key Insights

1) **TCS (TCS.NS)** maintains the highest adjusted close price among the four stocks throughout the observed period, indicating strong and stable performance in the market.
2) **Reliance (RELIANCE.NS)** shows considerable growth and is relatively stable, but experiences some fluctuations. The upward trend over the period reflects its strong market presence.
3) **Infosys (INFY.NS)**, represented in green, demonstrates less volatility and appears consistent with minor increases. Its performance suggests a steady growth trajectory.
4) **HDFC Bank (HDFCBANK.NS)** has the lowest adjusted close price among the stocks in this comparison. Its trend shows moderate stability, with a slight upward trend toward the end of the period, which may indicate future growth potential.