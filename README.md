# Kirana Store Demand Forecasting - Hackathon Project

## Project Overview
This project was developed as part of a Data Science Hackathon. The objective is to forecast daily product demand in local kirana stores using transactional data. Accurate demand forecasting helps store owners manage inventory efficiently, minimize wastage, and avoid stockouts.

## Dataset
- **Filename**: `kiranaRO_train.csv`
- # Dataset for the Project
The dataset for this project can be downloaded from the following Google Drive link:

[Download the Original Dataset](https://drive.google.com/file/d/1cwvnsBzCYTNkrhgFLDxObqHS8-jUPfPk/view?usp=sharing)

[Download the PreProcessed Dataset](https://drive.google.com/file/d/1tPga4yXe7ypA_-YlBGtdARPtttnbpwfj/view?usp=sharing)

- **Provided by**: Hackathon Organizers
- **Description**: Transaction-level sales data containing invoice information, product descriptions, quantity sold, unit price, and customer details.

## Steps Performed

### 1. Data Cleaning
- Removed rows with negative or zero quantities (returns/cancellations)
- Dropped rows with missing product descriptions
- Converted invoice dates to datetime format

### 2. Feature Engineering
- Extracted date-based features: day of week, month, hour, is weekend
- Created a new revenue column (quantity × unit price)
- Aggregated data to daily product-level demand

### 3. Exploratory Data Analysis
- Visualized overall demand trends over time
- Identified top-selling and highest-revenue products
- Analyzed product sales by hour of day and day of week

### 4. Modeling
- Model used: XGBoost Regressor
- Target variable: Daily quantity sold
- Feature set: Includes date-based features and product encoding
- Evaluation metrics: RMSE, R-squared (regression); F1-score, precision, recall (if binarized for demand classification)

### 5. Innovation Layer
- Conceptual restock alert system based on predicted demand and current stock
- Visual product-level insights for store owners to aid inventory planning

## Folder Structure
kirana-forecasting-hackathon/
├── data/
│   └── kiranaRO_train.csv
|   └── cleaned_kirana_data.csv
├── notebooks/
│   └── kirana_forecasting_colab.ipynb  ← Downloaded from Colab
├── presentation/
│   └── Hackathon_PPT.pptx
├── README.md

## How to Run
1. Open the notebook located in `notebooks/kirana_forecasting_colab.ipynb` using Google Colab or Jupyter.
2. Ensure the dataset `kiranaRO_train.csv` is located in the `data/` folder.
3. Run all code cells sequentially to replicate results and view visualizations.

## Team Members
- Aaradhya
- Anu
- Deepak Rawat
- Kunal Jain
