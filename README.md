## E-Commerce Ecosystem Analysis

This project, "E-Commerce Ecosystem," focuses on analyzing e-commerce transactional data to uncover key insights related to product performance, seller profitability, and sales trends. The analysis covers various aspects of an e-commerce ecosystem, providing a comprehensive understanding of purchasing patterns and operational metrics.

### Dataset

The dataset used in this project is sourced from Data.GOV and can be viewed at the following link: [State Agency Amazon Spend Fiscal Year 25](https://catalog.data.gov/dataset/state-agency-amazon-spend-fiscal-year-25).

The dataset includes the following columns:
* **Order Date**: The date on which the order was placed.
* **Agency Name**: The name of the agency handling or processing the order.
* **Payment Date**: The date when the payment was made.
* **Payment Amount**: The total amount paid for the order.
* **Shipment Date**: The date when the order was shipped.
* **Product Category**: The category or type of product purchased.
* **ASIN**: Amazon Standard Identification Number, a unique identifier for each product.
* **Title**: The name or description of the product.
* **UNSPSC**: United Nations Standard Products and Services Code, a global classification system for products and services.
* **Brand Code**: A code representing the brand of the product.
* **Brand**: The name of the brand.
* **Manufacturer**: The entity that manufactures the product.
* **Item Model Number**: The model number of the item.
* **Part Number**: A unique number assigned to each part of a product.
* **Product Condition**: The condition of the product (e.g., new, used).
* **Listed PPU**: The price per unit as listed.
* **Purchase PPU**: The price per unit at purchase.
* **Item Quantity**: The number of units purchased.
* **Item Subtotal**: The subtotal amount for the items purchased before any additional charges.
* **Item Shipping & Handling**: The cost associated with shipping and handling.
* **Item Promotion**: Any promotional discount applied to the item.
* **Item Tax**: The tax amount applied to the item.
* **Item Net Total**: The total amount for the item after discounts, shipping, and taxes.
* **Discount Program**: Information about any discount programs applied.
* **Pricing Discount Applied ($ off)**: The discount amount applied in dollars.
* **Pricing Discount Applied (% off)**: The discount percentage applied.
* **Seller Name**: The name of the seller.
* **Order Day**: The day of the week when the order was placed (extracted).
* **Order Delivery Time**: The time taken for the order to be delivered (extracted).
* **Time to Purchase**: The time elapsed from when the product was listed to when it was purchased (extracted).
* **Seller Profit**: Seller's earnings after deducting all costs from a sale (extracted).

### Project Structure

*   `Mid Project - E-Commerce Ecosystem.ipynb`: The main Jupyter Notebook containing the data analysis, visualization, and potentially model training.
*   `Mid Project - E-Commerce Ecosystem.pptx`: PowerPoint presentation, likely containing a project overview, objectives, and findings (cannot be directly processed by this agent).
*   `data/`: Directory containing the raw and supporting data files.
    *   `State_Agency_Amazon_Spend_Fiscal_Year_25.csv`: The primary dataset for the analysis.
    *   `link dataset.txt`: A text file, possibly containing a link to the dataset source or related information.
*   `cleaned_data/`: Directory containing cleaned or preprocessed data.
    *   `X_test_scaled.csv`: Scaled features for the test set.
    *   `X_train_scaled.csv`: Scaled features for the training set.
    *   `y_test.csv`: Target variable for the test set.
    *   `y_train.csv`: Target variable for the training set.
*   `README.md`: This file, providing an overview and documentation for the project.


### Project Objectives (Questions Addressed)

This project aims to answer the following key questions:

1.  What are the best-selling product categories and brands?
2.  How does seller profit vary across different product categories?
3.  How does purchase PPU (Price Per Unit) influence seller profit across different product categories?
4.  How does item tax vary across different product categories?
5.  How do item shipping & handling costs vary across different manufacturers?
6.  What is the relationship between item tax and payment amount across different product categories?
7.  How does order delivery time vary across different product categories and brands?
8.  How do sales trends vary by day of the week?
9.  How does the total number of items sold vary across different days of the week over time?
10. How does total seller profit vary across different days of the week over time?
11. How does the time to purchase (`time_to_purchase`) vary across product categories?
12. What is the trend of shipping and handling costs over time?

### Methodology

The project follows a standard data analysis pipeline involving data understanding, exploratory data analysis (EDA), and data preprocessing.

#### 1. Understanding Data
* **Understand Columns**: Identify and understand the significance of each column in the dataset.
* **Check Data Types**: Review and ensure the data types of each column are appropriate.
* **Describe Numerical Columns**: Summarize numerical columns using descriptive statistics.
* **Describe Categorical Columns**: Analyze categorical columns by examining unique values and their frequencies.

#### 2. Exploratory Data Analysis (EDA)

* **Uni-variate Analysis**:
    * Histograms: Plot histograms to understand the distribution of numerical features.
    * Distribution Plots: Assess the shape and spread of numerical distributions.
    * Categorical Analysis: Visualize the frequency of categorical values using bar plots or count plots.
* **Bi-Variate Analysis**:
    * **Numerical vs Numerical**: Scatter plots and line plots to explore relationships and trends.
    * **Numerical vs Categorical**: Box plots and violin plots to compare distributions across categories.
    * **Categorical vs Categorical**: Bar plots and count plots to aggregate and compare values across categories.
* **Multi-Variate Analysis**: Pair plots to visualize relationships and distributions among multiple numerical features simultaneously.

#### 3. Pre-Processing

* **Detect & Handle Duplicates**: Identify and remove any duplicate rows to ensure data uniqueness.
* **Train-Test Split**: Divide the dataset into training and testing subsets for model evaluation.
* **Detect & Handle NaNs**: Identify missing values and address them through imputation or removal.
* **Detect & Handle Outliers**:
    * Identify Outliers: Use statistical methods like Interquartile Range (IQR).
    * Handle Outliers: Apply capping to extreme values based on upper and lower bounds.
* **Encoding**:
    * Nominal Encoding: Use OneHotEncoding for limited unique values and BinaryEncoding for high-cardinality categorical features.
* **Scaling**: Standardize numerical features using StandardScaler.
* **Save Processed Data**: Save the processed training and testing datasets for future use.

### Libraries Used

The following Python libraries are imported and used in this project:

* `numpy` (np): For numerical operations.
* `pandas` (pd): For data manipulation and analysis.
* `seaborn` (sns): For statistical data visualization.
* `matplotlib.pyplot` (plt): For creating static, animated, and interactive visualizations.
* `sklearn.model_selection.train_test_split`: For splitting data into training and test sets.
* `sklearn.preprocessing.OneHotEncoder`: For one-hot encoding categorical features.
* `category_encoders.BinaryEncoder`: For binary encoding high-cardinality categorical features.
* `sklearn.preprocessing.StandardScaler`: For standardizing features.
