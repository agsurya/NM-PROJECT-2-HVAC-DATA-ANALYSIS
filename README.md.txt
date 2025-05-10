

# HVAC Sensor Data Analysis

**A.SURYA**
2nd Year – Mechanical Engineering
ARM College of Engineering & Technology
**Course:** Data Analysis in Mechanical Engineering

---

## Introduction

As part of my learning in data analysis and its applications in mechanical systems, I worked on analyzing HVAC (Heating, Ventilation, and Air Conditioning) sensor data. The goal of this project is to understand how different environmental and system-related factors affect energy usage and indoor comfort.

By studying patterns in sensor readings like temperature, airflow, and CO2 levels, we can learn how to make HVAC systems more efficient and better suited to the needs of the building.

---

## Why This Project Matters

This analysis helps in:

* Finding out when and why HVAC systems consume the most energy.
* Detecting signs of inefficiency or unusual patterns in indoor conditions.
* Supporting smart building maintenance and automation systems.
* Understanding how human presence (occupancy) affects indoor air quality and system behavior.

---

## What’s in the Dataset?

The dataset is a time-based log of various sensor readings. Below is a brief overview of the key features:

| Feature Name              | What It Represents                           |
| ------------------------- | -------------------------------------------- |
| Date\_Logged              | Date and time when the data was recorded     |
| Temperature (C)           | Indoor temperature in Celsius                |
| Humidity (%)              | Relative humidity level inside the room      |
| Air\_Flow (CFM)           | How much air is moving, in cubic feet/minute |
| CO2\_Level (ppm)          | CO2 concentration inside the building        |
| Occupancy                 | Number of people present in the room         |
| Energy\_Consumption (kWh) | How much energy the HVAC system used         |

---

## How the Data Was Prepared

1. **Loading the Data**
   I used the pandas library to import and check the structure of the dataset.

2. **Fixing the Date Column**
   The `Date_Logged` column was converted into datetime format so we could analyze the data over time.

3. **Handling Missing Values**
   Some columns like `CO2_Level` and `Air_Flow` had missing entries. I filled them using the average value of each column.

4. **Creating New Features**
   I added two useful columns:

   * **Hour** of the day (from 0 to 23)
   * **DayOfWeek** (0 = Monday, 6 = Sunday)

These additions made it easier to spot patterns during different times and days.

---

## What I Discovered (EDA)

### Time-Based Trends

* Energy usage follows a routine daily cycle, rising during office hours.
* CO2 levels increase when more people are in the room.
* HVAC systems seem to respond by increasing airflow.

### Correlation Between Features

* Energy usage is influenced by both temperature and airflow.
* CO2 levels strongly relate to the number of people present.

### Feature Distributions

* Some readings, especially for energy and airflow, had extreme values or outliers.
* Boxplots and histograms helped me identify these unusual points.

---

## Key Takeaways

* **Occupancy directly affects CO2 levels**, which helps in planning ventilation strategies.
* **HVAC airflow adapts to room usage**, showing the effect of automation.
* **Most energy is consumed during working hours** (around 9 AM to 6 PM).
* **Temperature and humidity stay stable**, proving that the system maintains comfort well.

---

## What’s Next?

In future versions of this project, I plan to:

* Use statistical methods (like the IQR method) to remove outliers.
* Try building a simple prediction model to forecast energy usage.
* Explore whether machine learning can help detect unusual system behavior.

---

## Tools and Libraries Used

* **Python** with **Pandas** and **NumPy** for data handling
* **Plotly** and **Matplotlib** for data visualization
* **Jupyter Notebook** for writing and running the code

