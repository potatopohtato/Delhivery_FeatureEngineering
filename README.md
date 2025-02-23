# Delhivery Logistics Data Analysis

## Overview
This project focuses on analyzing delivery logistics data to optimize operations for Delhivery, a leading logistics company. The analysis aims to identify bottlenecks, compare actual delivery performance with OSRM (Open Source Routing Machine) predictions, and provide actionable insights to improve efficiency.

## Key Questions
1. What are the busiest delivery corridors?
2. How does actual delivery time compare to OSRM predictions?
3. Are there any outliers in delivery times or distances?
4. Which cities contribute the most to the order volume?
5. What are the most common route types (FTL vs. Carting)?

## Dataset Description
The dataset contains the following key columns:
- **trip_uuid**: Unique identifier for each trip.
- **source_name**: Name of the source location.
- **destination_name**: Name of the destination location.
- **actual_distance_to_destination**: Actual distance traveled for the trip.
- **actual_time**: Actual time taken for the trip.
- **osrm_time**: Predicted time by OSRM.
- **osrm_distance**: Predicted distance by OSRM.
- **route_type**: Type of route (FTL or Carting).
- **trip_creation_time**: Timestamp when the trip was created.
- **od_start_time**: Start time of the trip.
- **od_end_time**: End time of the trip.
- **start_scan_to_end_scan**: Time taken from the first scan to the last scan.

## Data Cleaning and Preprocessing
- **Handling Missing Values**: Missing values were identified and handled appropriately.
- **Merging and Aggregating Rows**: Rows were merged based on `trip_uuid`, and relevant fields were aggregated to summarize trip-level data.
- **Feature Engineering**: Useful features were extracted, such as city names from `source_name` and `destination_name`, and date features from `trip_creation_time`.

## Exploratory Data Analysis (EDA)
### Univariate Analysis:
- **Distribution of Actual Time**: Analyzed the distribution of actual delivery times.
- **Frequency of Route Types**: Examined the frequency of different route types (FTL vs. Carting).

### Bivariate Analysis:
- **Actual Time vs. OSRM Time**: Compared actual delivery times with OSRM predictions using scatter plots.
- **OD Duration vs. Start Scan to End Scan**: Analyzed the relationship between trip duration and scan times.

### Outlier Detection:
- **IQR Method**: Identified outliers in actual delivery times using the Interquartile Range (IQR) method.

## Feature Engineering
- **One-Hot Encoding**: The `route_type` column was converted into numerical format using one-hot encoding.
- **Normalization/Standardization**: Numerical features were standardized using `StandardScaler`.

## Business Insights
### Busiest Corridors:
- Identified the busiest delivery corridors, along with their average distances and delivery times.

### Route Type Analysis:
- **FTL (Full Truck Load)**: Typically used for longer distances with larger loads.
- **Carting**: Used for shorter distances with smaller loads.

### City Contribution:
- Analyzed which cities contribute the most to the order volume.

## Repository Structure
- **Delhivery_FeatureEngineering.ipynb**: Jupyter Notebook containing the detailed analysis and code.
- **Delhivery_FeatureEngineering.pdf**: PDF version of the analysis.
- **delhivery_data.csv**: Dataset used for the analysis.

## How to Use
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/delhivery-logistics-analysis.git
   ```
2. Navigate to the project directory:
   ```bash
   cd delhivery-logistics-analysis
   ```
3. Open the Jupyter Notebook to view the analysis:
   ```bash
   jupyter notebook Delhivery_FeatureEngineering.ipynb
   ```

## Dependencies
- Python 3.x
- Libraries: pandas, numpy, matplotlib, seaborn, scikit-learn

## Contributing
Contributions are welcome! Please fork the repository and create a pull request with your changes.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.


---

For any questions or feedback, please open an issue or contact pranavkiran74@gmail.com.
