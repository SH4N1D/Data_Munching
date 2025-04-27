# Airbnb NYC 2019 Dataset — Outlier Removal

## Project Overview
This project focuses on cleaning the **Airbnb NYC 2019** dataset by removing outliers to improve the quality and reliability of data analysis.  
The key task performed was outlier detection and removal based on the **price** feature, ensuring the dataset represents a more realistic distribution of Airbnb listings.

## Dataset
The dataset initially contained the following features:
- `id`, `name`, `host_id`, `host_name`
- `neighbourhood_group`, `neighbourhood`
- `latitude`, `longitude`
- `room_type`, `price`
- `minimum_nights`, `number_of_reviews`
- `last_review`, `reviews_per_month`
- `calculated_host_listings_count`, `availability_365`

For the purpose of this project, only the following columns were retained:
- `neighbourhood_group`
- `neighbourhood`
- `room_type`
- `price`
- `minimum_nights`

## Process

1. **Initial Data Exploration**  
   Basic statistics and structure of the dataset were explored using `describe()` and `head()` functions.

2. **Outlier Detection**  
   Outliers in the `price` feature were identified using the 1st and 99.9th percentile values:
   - 1st percentile (`0.01`): ~30 USD
   - 99.9th percentile (`0.999`): ~3000 USD

3. **Outlier Removal**  
   Listings with `price` values **below 30 USD** or **above 3000 USD** were removed.

4. **Post-cleaning Analysis**  
   After outlier removal:
   - Dataset size reduced from **48,895** rows to **48,183** rows.
   - A slight decrease in mean and standard deviation of the price feature was observed.

## Technologies Used
- Python 3.x
- Pandas
- Numpy



