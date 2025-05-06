
# Weather Data Visualization 

This project demonstrates how to perform exploratory data analysis (EDA) on a weather dataset using Python, pandas, and seaborn. The analysis includes data loading, inspection, and a variety of visualizations to understand relationships and distributions within the data.

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Requirements](#requirements)
- [Usage](#usage)
- [Visualizations](#visualizations)
- [License](#license)

## Overview

The script loads a weather dataset (`Test.csv`), inspects its structure, and uses seaborn to create multiple plots for visualizing relationships between features such as humidity, temperature, air pollution index, and weather types.

## Dataset

The dataset should be a CSV file named `Test.csv` with the following columns:

- `date_time`
- `is_holiday`
- `air_pollution_index`
- `humidity`
- `wind_speed`
- `wind_direction`
- `visibility_in_miles`
- `dew_point`
- `temperature`
- `rain_p_h`
- `snow_p_h`
- `clouds_all`
- `weather_type`
- `weather_description`

Example row:

| date_time         | is_holiday | air_pollution_index | humidity | wind_speed | wind_direction | visibility_in_miles | dew_point | temperature | rain_p_h | snow_p_h | clouds_all | weather_type | weather_description      |
|-------------------|------------|---------------------|----------|------------|----------------|---------------------|-----------|-------------|----------|----------|------------|--------------|-------------------------|
| 18-05-2017 00:00  | None       | 73.0                | 63.0     | 1.0        | 27.0           | 4.0                 | 4.0       | 285.15      | 0.0      | 0.0      | 90.0       | Rain         | moderate rain           |

## Requirements

- Python 3.x
- pandas
- seaborn
- matplotlib

Install dependencies with:

```bash
pip install pandas seaborn matplotlib
```

## Usage

1. Place your `Test.csv` file in the project directory.
2. Run the script:

```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Set seaborn style
sns.set(color_codes=True)

# Load the dataset
weather = pd.read_csv('Test.csv')

# Inspect the data
print(weather.head())
print(weather.info())

# Example visualizations
sns.barplot(x=weather['humidity'], y=weather['temperature'])
plt.show()

sns.distplot(weather['humidity'])
plt.show()

sns.jointplot(x=weather['humidity'], y=weather['temperature'])
plt.show()

# ... (add more plots as needed)
```

> **Note:** The script above shows only a subset of the visualizations. You can add or modify plots as needed for your analysis.

## Visualizations

The script demonstrates the following seaborn plots:

- Bar plots
- Distribution plots (histograms, KDE)
- Joint plots (scatter, hex, KDE)
- Pair plots
- Strip plots
- Swarm plots
- Box plots
- Count plots
- Point plots
- Linear model plots (lmplot)

These visualizations help in understanding the distribution and relationships between weather features.

## License

This project is open-source and available under the [MIT License](LICENSE).

---

