# Crop Recommendation and Analysis Dashboard

## Overview

This Python project utilizes Kaggle’s environment for analyzing and visualizing a crop recommendation dataset. The dataset includes various features related to soil and weather conditions (e.g., Nitrogen, Phosphorus, Potassium levels, temperature, humidity, pH value, and rainfall) along with the type of crop suitable for these conditions. The project includes data loading, cleaning, visualization, and a machine learning model to predict the best crop based on the given parameters.

### Dataset

The dataset used is the **Crop Recommendation Dataset**, which consists of 2,200 rows and 8 columns. The columns include:
- **Nitrogen** (int): Amount of Nitrogen in soil.
- **Phosphorus** (int): Amount of Phosphorus in soil.
- **Potassium** (int): Amount of Potassium in soil.
- **Temperature** (float): Ambient temperature in Celsius.
- **Humidity** (float): Percentage of humidity.
- **pH_Value** (float): pH value of the soil.
- **Rainfall** (float): Rainfall in mm.
- **Crop** (object): The recommended crop type.

### Libraries and Dependencies

The following Python libraries are required:
- `numpy`: For numerical operations.
- `pandas`: For data manipulation and analysis.
- `plotly`: For interactive data visualizations.
- `matplotlib` & `seaborn`: For generating static plots and heatmaps.
- `dash`: For creating interactive dashboards.
- `scikit-learn`: For machine learning model development.
- `pyngrok`: For exposing the local Dash app to the internet.

You can install these dependencies using:

```bash
pip install numpy pandas plotly dash scikit-learn pyngrok matplotlib seaborn
```

### Features

1. **Data Exploration and Cleaning**:
   - Inspecting data types, null values, and basic statistical analysis using `pandas`.
   - No missing values or NaNs are present in the dataset.

2. **Data Visualization**:
   - **Pie Chart**: Displays the crop distribution.
   - **Scatter Plot**: Shows the relationship between rainfall and temperature for different crops.
   - **Box Plot**: Compares nitrogen, phosphorus, and potassium levels across crops.
   - **Bar Plot**: Shows the mean levels of nutrients by crop.
   - **Sunburst Chart**: Visualizes nutrient levels per crop.
   - **3D Scatter Plot**: Represents temperature, humidity, and rainfall for different crops.
   - **Correlation Heatmap**: Shows relationships between the environmental features.

3. **Machine Learning Model**:
   - **Random Forest Classifier** is used to predict crop types based on environmental features.
   - Model achieves **97% accuracy**.
   - A **classification report** is plotted as a heatmap for further analysis.

4. **Interactive Crop Recommendation Dashboard**:
   - Built using `Dash`, the dashboard provides visual insights into crop distribution and nutrient data.
   - The dashboard is deployed via `ngrok`, making it accessible externally.

### Running the Dashboard

To run the dashboard, execute the notebook. The `ngrok` library is used to expose the dashboard, and the public URL is printed. 

Steps to run:
1. Install dependencies (if not already installed).
2. Run the notebook.
3. The app will be available at the printed `ngrok` URL.

### Machine Learning Workflow

1. **Data Split**: The dataset is split into training (80%) and testing (20%) sets.
2. **Training**: A Random Forest classifier is trained on the environmental features to predict crop types.
3. **Evaluation**: The model achieves high accuracy, and the performance is summarized using a classification report.

### How to Use

1. **Visualizations**: Explore various plots to understand the distribution of nutrients and environmental conditions for different crops.
2. **Modeling**: Check the machine learning section for model training and testing.
3. **Dashboard**: Access the interactive dashboard to visualize and explore data insights.

### Future Work

- Incorporate more advanced machine learning models.
- Implement real-time data updates for crop recommendations.
- Extend the dashboard with user inputs for on-the-fly recommendations.

---

### Files in the Repository

- **crop_recommendation.ipynb**: Main notebook containing the analysis, visualizations, model, and dashboard code.
- **Crop_Recommendation.csv**: The dataset used for crop recommendation.

---

### License

This project is licensed under the MIT License.

### Author

Maleke Chaker

For questions or issues, please contact melekchaker@gmail.com
