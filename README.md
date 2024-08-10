# Diamond-Price-Prediction-

### Aim and Objective 

This project aims to develop a robust and informative model for predicting diamond
prices using machine learning algorithms.
By leveraging the power of data and statistical analysis, the project seeks to:
- Analyse key factors influencing diamond price: Explore the relationships between
various diamond characteristics (cut, clarity, color, carat weight, etc.) and their
impact on price.
- Compare the effectiveness of different machine learning algorithms: Train and
evaluate various algorithms (e.g., linear regression, random forest, decision tree) to
determine the most accurate approach for diamond price prediction.
- Provide a valuable tool for diamond stakeholders: Develop a model that can assist
individuals and businesses in the diamond industry, such as appraisers, buyers, and
sellers, by offering data-driven insights into diamond valuation.

This project will contribute to a more informed understanding of the diamond market by
harnessing the predictive power of machine learning.

### Data

| Column | Description |
|--------|-------------|
| **price**  | Price in US dollars ($326–$18,823) |
| **carat**  | Weight of the diamond (0.2–5.01) |
| **cut**    | Quality of the cut (Fair, Good, Very Good, Premium, Ideal) |
| **color**  | Diamond color, from J (worst) to D (best) |
| **clarity**| A measurement of how clear the diamond is (I1 (worst), SI2, SI1, VS2, VS1, VVS2, VVS1, IF (best)) |
| **x**      | Length in mm (0–10.74) |
| **y**      | Width in mm (0–58.9) |
| **z**      | Depth in mm (0–31.8) |
| **depth**  | Total depth percentage = z / mean(x, y) = 2 * z / (x + y) (43–79) |
| **table**  | Width of top of diamond relative to widest point (43–95) |

###  Exploratory Data Analysis

- Key Insights: EDA revealed important features impacting diamond prices, such as carat, cut, color, clarity, and depth. Carat had the strongest correlation with price, while categorical features like cut, color, and clarity also showed varying influences.
- A count plot for the cut feature would show the distribution of diamond cuts across the dataset. You would likely observe that certain cuts (like "Ideal" or "Premium") are more common, while others (like "Fair") are less frequent.
- The count plot for the color feature would indicate the frequency of each color grade. A common observation might be that middle-range colors (like "G", "H", and "I") are more prevalent compared to the extremes (like "D" or "J").
-  The count plot for the clarity feature would display how often each clarity grade appears in the dataset. It might reveal that certain clarity grades (like "SI1" or "VS2") are more common, while higher clarity grades (like "IF" or "VVS1") are rarer.
-   Pair plots and correlation heatmaps were used to visualize the relationships between numerical features, showing strong linear relationships between carat and price.
-   The pair plot often reveals a strong positive linear correlation between the carat and price features. As the carat weight increases, the price tends to increase significantly. This insight aligns with domain knowledge that larger diamonds (higher carat) are generally more expensive.
-   When comparing categorical variables like cut, color, and clarity against price, the pair plots help visualize the spread of prices within each category. For example, diamonds with a "Fair" cut might cluster at the lower end of the price spectrum, while those with "Ideal" cuts are distributed towards higher prices.

### Model Building and Evaluation

Modeling Approach: Multiple machine learning models were tested for predicting diamond prices, including Linear Regression, Decision Trees, and Random Forests etc.

#### Model Performance

| Algorithm                     | Training Score | Testing Score | MSE            |
|-------------------------------|----------------|---------------|----------------|
| **Linear Regression**         | 91.27%         | 91.26%        | 1,352,145      |
| **Random Forest Regressor**   | 99.74%         | 98.13%        | 289,988.8      |
| **Decision Tree Regressor**   | 99.99%         | 96.50%        | 540,933.3      |
| **XGBoost Regressor**         | 99.11%         | 98.14%        | 287,958.0      |
| **Gradient Boosting Regressor**| 97.77%        | 97.65%        | 363,904.4      |


- Random Forest: Outperformed the other models by combining multiple decision trees, reducing overfitting, and providing better generalization to unseen data.
- Linear Regression: Provided a baseline model but suffered from underfitting due to the complexity of relationships between features.
- Decision Trees: Improved performance by capturing non-linear relationships but was prone to overfitting.

Random Forest was selected as the best model based on its superior performance metrics like R-squared and Mean Absolute Error (MSE).The EDA and modeling results indicate that the Random Forest model is well-suited for predicting diamond prices, with key features like carat, cut, color, and clarity playing a significant role in the model's predictions.
