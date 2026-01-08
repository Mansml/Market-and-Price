# Simple Guide: Analyzing Food Prices in Ghana

## What You'll Discover
You'll explore how Ghana's economy affects food prices from 2015-2024. Think of it like detective work, finding clues in the data about what makes food more expensive.

## Your Data Files
1. **Food prices** - Prices of rice, maize, yam, tomatoes, etc. across Ghana
2. **Economic indicators** - Things like inflation (how fast prices rise), exchange rates (how strong the Ghana Cedi is), interest rates, debt levels, etc.

## Steps to Follow in Google Colab

### Step 1: Upload Your Files
Click the folder icon on the left sidebar in Colab, then upload all 5 CSV files.

### Step 2: Ask Gemini to Load the Data
Copy this into Colab and run it:

```
Load these CSV files:
- bog_fx_selenium_2015_to_2024.csv (economic indicators)
- wfp_food_prices_gha.csv (food prices)

Show me the first few rows of each to understand what's inside.
```

### Step 3: Prepare the Data
The economic data is organized by months/years in columns. You need it reorganized so each row is one month. Ask Gemini:

```
The bog_fx_selenium file has months as columns. Reshape it so each row represents one month with columns: Date, Variable, Value. Then merge it with the food prices data by matching dates.
```

### Step 4: Pick Your Foods to Study
You have 20+ foods. Start with the most important ones. Ask Gemini:

```
Show me which food commodities have the most price data. Then create a dataset focusing on these 5 foods: Maize, Rice (imported), Rice (local), Tomatoes (local), and Yam. Calculate the average national price for each food by month.
```

**Why?** These are staple foods Ghanaians eat regularly.

### Step 5: Visualize Food Price Trends
Ask Gemini:

```
Create a line graph showing how prices changed over time (2015-2024) for each of the 5 foods. Use different colors for each food.
```

**What to look for:** Which foods got much more expensive? When did big price jumps happen?

### Step 6: Compare with Key Economic Indicators
Now the interesting part! Ask Gemini:

```
Create 4 separate graphs, each showing:
1. Food prices vs Headline Inflation
2. Food prices vs USD/GHS Exchange Rate  
3. Food prices vs Food Inflation
4. Food prices vs Fuel Prices (diesel/petrol)

For each graph, put the food prices on one axis and the economic indicator on another axis. Use different colored lines.
```

**Economic terms explained:**
- **Headline Inflation** = How fast prices rise overall (%)
- **Exchange Rate** = How many Cedis you need to buy 1 US Dollar (higher = Cedi is weaker)
- **Food Inflation** = How fast just food prices rise (%)
- **Fuel Prices** = Cost of petrol/diesel (affects transportation costs)

### Step 7: Find Relationships (Correlation)
Ask Gemini:

```
Calculate correlation coefficients between each food's price and these indicators:
- Headline Inflation
- Food Inflation
- USD/GHS Exchange Rate
- Diesel Price
- Gross International Reserves
- Public Debt/GDP

Show me the results in a table sorted by correlation strength. Create a heatmap to visualize which relationships are strongest.
```

**What correlation means:** A number from -1 to +1 showing how closely two things move together:
- Close to +1 = when one goes up, the other goes up too (strong positive relationship)
- Close to -1 = when one goes up, the other goes down (strong negative relationship)
- Close to 0 = no clear relationship

**What to look for:** Which indicator has correlations closest to +1 or -1? That's your best predictor!

### Step 8: Test Predictions
For your best predictor, ask Gemini:

```
Using [the best indicator from step 7], create a scatter plot for each food showing the relationship. Add a trend line (linear regression). Calculate the R-squared value to see how well it predicts prices.
```

**R-squared explained:** A score from 0-100% showing how much of the price changes your indicator can explain. Higher = better predictor.

### Step 9: Deep Dive on One Food
Pick the food with the strongest relationships. Ask Gemini:

```
Focus on [food name]. Create:
1. A time series showing major price spikes and what economic events happened then
2. A multi-indicator comparison showing the top 3 predictors together
3. A simple forecast: if the exchange rate increases by 10%, how much would this food's price change?
```

### Step 10: Summary Table
Ask Gemini:

```
Create a final summary table showing:
- Each food
- Its best predictor indicator
- The correlation strength
- The R-squared value
- A one-sentence interpretation

Then write 3-5 bullet points of key findings in plain language.
```

## What You'll Learn

You'll discover things like:
- Does rice get more expensive when the Cedi weakens?
- Do tomato prices follow fuel costs (transport)?
- Is the exchange rate or inflation better at predicting maize prices?
- Which foods are most sensitive to economic changes?

## Tips for Using Gemini
1. If you get an error, copy the error message and ask Gemini to fix it
2. Ask Gemini to "explain this graph" if you're unsure what it shows
3. Request "make the graph prettier with better labels" anytime
4. Save your best graphs: right-click → Save image

## Expected Results
The **exchange rate** (USD/GHS) typically predicts food prices best because Ghana imports a lot, and a weaker Cedi makes everything more expensive. But you might find surprises, some local foods like yam might not follow the same pattern!

Good luck! Remember: you're learning to tell a data story about how Ghana's economy affects what people pay for food.
