# Ex-01: Plot a Time Series Data
## NAME : Hariharan S
## REG NO: 2305001009

## Aim
To develop a Python program to plot and visualize time-series data and identify trends such as increasing, decreasing, constant, and seasonal patterns.

## Objectives

To create time-series data for population, temperature, and commodity prices.
To store and manage data using Pandas DataFrames.
To plot time-series data using Matplotlib.
To identify trends and seasonal patterns from graphs.

## Program
```python
import pandas as pd
import matplotlib.pyplot as plt

# Step 1: Create annual population data (2015–2025)
year = list(range(2015, 2026))
population = [80, 83, 85, 88, 91, 94, 98, 102, 106, 111, 116]

# Step 2: Create monthly temperature data
months = ["Jan", "Feb", "Mar", "Apr", "May", "Jun",
          "Jul", "Aug", "Sep", "Oct", "Nov", "Dec"]
temperature = [24, 26, 29, 32, 35, 36, 34, 33, 32, 30, 27, 25]

# Step 3: Create monthly commodity price data
price = [4200, 4350, 4280, 4500, 4650, 4800,
         4750, 4900, 4850, 5000, 5100, 5250]

# Step 4: Create DataFrames
population_data = pd.DataFrame({
    "Year": year,
    "Population": population
})

temperature_data = pd.DataFrame({
    "Month": months,
    "Temperature": temperature
})

price_data = pd.DataFrame({
    "Month": months,
    "Price": price
})

# Step 5: Display the data
print("Annual Population Data:")
print(population_data)

print("\nMonthly Temperature Data:")
print(temperature_data)

print("\nMonthly Commodity Price Data:")
print(price_data)

# Step 6: Plot annual population
plt.figure(figsize=(8, 4))
plt.plot(population_data["Year"],
         population_data["Population"], marker="o")
plt.title("Annual Population Time Series")
plt.xlabel("Year")
plt.ylabel("Population (Assumed Units)")
plt.grid(True)
plt.show()

# Step 7: Plot monthly temperature
plt.figure(figsize=(8, 4))
plt.plot(temperature_data["Month"],
         temperature_data["Temperature"], marker="o")
plt.title("Monthly Temperature")
plt.xlabel("Month")
plt.ylabel("Temperature (°C)")
plt.grid(True)
plt.show()

# Step 8: Plot monthly commodity price
plt.figure(figsize=(8, 4))
plt.plot(price_data["Month"],
         price_data["Price"], marker="o")
plt.title("Monthly Commodity Price")
plt.xlabel("Month")
plt.ylabel("Price (Assumed Units)")
plt.grid(True)
plt.show()
```
## Output

<img width="484" height="630" alt="image" src="https://github.com/user-attachments/assets/00c4b1b8-5680-455d-88c7-82d4aadaccab" />
<img width="695" height="393" alt="image" src="https://github.com/user-attachments/assets/5afaa90f-909b-43c4-9c32-bb7b6ad39f7f" />
<img width="686" height="393" alt="image" src="https://github.com/user-attachments/assets/1442012b-8b2e-44d6-ba6a-984b8a15bcf7" />


## Result
Thus, time-series data for annual population, monthly temperature, and monthly commodity prices were successfully created, stored using Pandas, and visualized using Matplotlib. The population and commodity price graphs show an overall increasing trend, while the temperature graph shows a seasonal pattern, with temperatures increasing toward the middle of the year and decreasing afterward.
