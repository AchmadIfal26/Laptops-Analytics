# Laptop Data Analysis

This project involves analyzing a dataset of laptops to extract various insights. Below are the details of the analysis and the results.

## Data Analysis Steps

### 1. Filter laptops with a minimum price of 60000 and have a touchscreen

```python
import pandas as pd

# Filter DataFrame for laptops with a minimum price of 60000 and have a touchscreen
laptop_price = laptop_data[(laptop_data["Price"] >= 60000) & (laptop_data['Touch_Screen'] == True)]

print(laptop_price)
```

### 2. Display laptops with a Core i9 processor and price above 150000

```python
# Filter laptops with a Core i9 processor and price above 150000
filtered_laptops = laptop_data[(laptop_data["Price"] > 150000) & (laptop_data["Processor"] == "Core i9")].sort_values(by="Price", ascending=False)

print(filtered_laptops)
```

### 3. Count the number of laptops with Intel Core i7 processor

```python
# Count laptops with Intel Core i7 processor
jumlah_i7 = laptop_data[laptop_data['Processor'] == 'Core i7']

total_i7 = jumlah_i7.shape[0]
print(f"Total laptops with Intel Core i7 processor: {total_i7}")
```

### 4. Calculate the total price of laptops with a touchscreen

```python
# Calculate the total price of laptops with a touchscreen
touch_screen_laptop = laptop_data[laptop_data['Touch_Screen'] == True]

total_price_touch_screen = touch_screen_laptop["Price"].sum()
print(f"Total price of laptops with a touchscreen: {total_price_touch_screen}")
```

### 5. Count the number of laptops produced by the brand "Asus"

```python
# Count laptops produced by Asus
merk_asus = laptop_data[laptop_data["Brand"] == "ASUS"]

total_asus = merk_asus.shape[0]
print(f"Total laptops produced by Asus: {total_asus}")
```

### 6. List the models of Asus laptops using Intel Core i5 processor

```python
# List Asus laptops using Intel Core i5 processor
asus_i5_models = laptop_data[(laptop_data["Brand"] == "ASUS") & (laptop_data["Processor"] == "Core i5")]

print(asus_i5_models)
```

### 7. Count the total number of laptops with a touchscreen

```python
# Count total laptops with a touchscreen
laptop_layar_sentuh = laptop_data[laptop_data["Touch_Screen"] == True]

total_laptop_layar_sentuh = laptop_layar_sentuh.shape[0]
print(f"Total laptops with a touchscreen: {total_laptop_layar_sentuh}")
```

## Summary of Results

- Total laptops with a minimum price of 60000 and a touchscreen: [count]
- Total laptops with Core i9 processor and price above 150000: [count]
- Total laptops with Intel Core i7 processor: [count]
- Total price of laptops with a touchscreen: [total_price]
- Total laptops produced by Asus: [count]
- Models of Asus laptops using Intel Core i5 processor: [list of models]
- Total laptops with a touchscreen: 96

This analysis helps in understanding the distribution and specifications of laptops within different criteria. The results can be further used for making informed purchasing decisions or for market analysis.
