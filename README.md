# gdl_temperatures
# Temperature Data Analysis and Visualization Script

This script performs several tasks related to temperature data analysis and visualization for Guadalajara. It involves data scraping, data cleaning, trend analysis, and plotting of temperature trends over time.

## Script Breakdown

### 1. **Loading and Cleaning Data**
   - **File Loading**: The script loads a CSV file containing temperature data.
   - **Data Cleaning**: It replaces non-numeric values ('-') in the temperature column with `NaN` and converts the column to numeric.

### 2. **Calculating Yearly Averages and Trend**
   - **Group By Year and Month**: The script calculates the monthly average temperatures by grouping the data by `Year` and `Month`.
   - **5-Year Trend Calculation**: It computes a 5-year rolling mean to smooth the temperature data and observe trends over time.

### 3. **Visualization**
   - **Monthly Average Temperature Plot**:
     - Plots the monthly average temperatures.
     - Adds a 5-year trend line.
     - Saves the plot as `Montly average and 5y trend GDL.png`.

   - **5-Year Trend Focus Plot**:
     - Focuses on the 5-year trend line.
     - Calculates the slope of the trend line to indicate temperature change over time.
     - Saves the plot as `5y trend GDL.png`.

### 4. **Slope Calculation**
   - **Linear Regression**: Calculates the slope of the 5-year trend line using linear regression.
   - **Slope Interpretation**: The slope represents the rate of temperature change in degrees per month.

### 5. **Data Scraping**
   - **Web Scraping**:
     - Iterates over each year and month from 1992 to 2024.
     - Scrapes average daily temperatures from the specified website.
     - Uses a delay to prevent overloading the server.
   - **Data Storage**: Stores the scraped data in a CSV file named `guadalajara_temperatures_2024.csv`.

### 6. **Function Definition**
   - **scrape_temperatures(year, month)**:
     - **Parameters**: `year`, `month`.
     - **Functionality**: Scrapes average daily temperatures for the specified year and month.
     - **Output**: Returns a list of temperature records.


![5-Year Trend](5y%20trend%20GDL.png)
