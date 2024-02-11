![Header.jpg](https://github.com/ankysoemitro/Project2/blob/main/images/Header.jpg)

# House Price Prediction using Multiple Regression Analysis

**Authors:** Andrinny Soemitro
***

## Overview



The primary goal of this project is to develop a robust and accurate model for predicting house prices based on various features. By leveraging machine learning techniques, we aim to provide valuable insights to real estate stakeholders, enabling informed decision-making in a dynamic housing market.

## Business Problem

The central business challenge revolves around providing house sellers with a strategic edge in the real estate market, with a focus on achieving optimal pricing for their properties. House sellers grapple with the task of determining the right listing price to attract potential buyers while ensuring a profitable transaction. Accurate pricing is crucial for minimizing time on the market, reducing carrying costs, and maximizing return on investment. For house sellers, gaining insights into the nuanced factors influencing property prices, such as the number of bedrooms, bathrooms, square footage, and other relevant attributes, is paramount.

The primary stakeholder in this scenario is the house seller, and the objective is to empower them with data-driven insights through regression predictive analysis. By adopting this approach, sellers can make informed decisions when establishing competitive and realistic listing prices, thereby increasing the likelihood of attracting potential buyers and facilitating smoother transactions. The outcomes of this analysis directly benefit house sellers, providing them with the confidence to navigate the intricate real estate landscape and optimize returns on their property investments.

The analysis aims to address three key business questions:

1. **What are the significant factors influencing house prices in the real estate market?**

2. **How do different zipcode impact average property prices, and what factors contribute to these variations?**

3. **How can this knowledge be effectively utilized to establish an optimal price prediction for sellers?**


This analytical approach seeks to enhance the precision of pricing strategies, empower sellers with valuable insights, and ultimately contribute to their success in navigating the dynamic real estate landscape.

## Data Understanding

The dataset used in this project was sourced from 'House Sales in King County, USA' given in the beginning of the project. The dataset encompasses key variables that play a pivotal role in determining property values. The description of columns in the dataset is shown below:

![data_desc.png](data_desc.png)

The decision to exclude certain columns, namely 'id,' 'date,' 'sqft_above,' 'sqft_basement,' 'yr_renovated,' 'lat,' 'long,' 'sqft_living15,' and 'sqft_lot15,' from the predictive model was made with careful consideration of their relevance and redundancy to the task of predicting house prices.

## Data Preparation



For every data analytics process, it's essential to preprocess and prepare the dataset. This involves handling missing values, encoding categorical variables, and scaling numerical features to ensure optimal model performance. The data_preparation.ipynb notebook in the repository walks through these steps using the pandas library for data manipulation and scikit-learn for preprocessing. Key transformations include imputing missing values, applying logarithmic transformations to skewed continuous variables, and employing one-hot encoding for categorical features. Additionally, the notebook explores the importance of a train-test split using train_test_split from scikit-learn to evaluate the model's generalization performance.

## Data Modeling

The initial stage of the exploration involves creating scatterplot to visualize and identify categorical and continuous variables.

![cat_cont.png](cat_cont.png)

Scatterplot shown that bedrooms, bathrooms, sqft_living, sqft_lot appear to be continuous while floors, waterfront, condition, grade, yr_built and zipcode appear to be categorical. It also appears that bathroom and sqft_living have more positive relationship to the price.

### Significant Factors Influencing House Price

There are 3 significant factors positively correlated with price: sqft_living, grade and bathrooms. A positive correlation implies that as a particular feature or variable increases, the house prices also tend to rise. For instance, we observe that the highest positive correlation is between square footage and house prices, it suggests that larger living spaces are associated with higher property values.

![correlation.png](correlation.png)

### Effect of Zipcode on Average Property Price

The top 3 highest average property price are within the zipcode of 98039, 98004, 98040.

![avg_price.png](avg_price.png)

Upon further analysis, it has become evident that houses with comparable features exhibit variations in pricing across 3 zipcodes with the highest average price. Despite the similarities in key property attributes, such as bedrooms, bathrooms, and square footage, distinct pricing patterns emerge when considering the geographic location represented by zip codes. This nuanced insight underscores the influence of regional factors on housing prices, suggesting that location plays a pivotal role in shaping the market dynamics and influencing property valuations.

![features_by_zipcode.png](features_by_zipcode.png)

House price value also increases when the number of bathrooms and floors increases with addition of waterfront as evident in the row number 7.

### House Price Prediction

In our predictive model, we utilized a set of key features to estimate the price of a specific property. For a residence characterized by 7 bedrooms, 6 bathrooms, 9,500 square feet of living space, a 6,000 square feet lot, 2 floors, waterfront view, excellent condition (condition 5), a grade of 8, built in 2014, and situated in the 98004 zip code, our model generated a predicted price of US$2,607,762.39. This output is derived from the intricate relationships learned during the model training phase, which considered a myriad of factors influencing housing prices.

![price_predict.png](price_predict.png)

![predicted_price.png](predicted_price.png)

## Evaluation


To effectively guide sellers in predicting optimal prices, understanding the nuanced interplay of factors is key. Our analysis revealed that comparable houses can vary in pricing across high-average-price zip codes, emphasizing the impact of geographic location. Despite similar property attributes, such as bedrooms and bathrooms, distinct pricing patterns emerged, highlighting the influence of regional dynamics on property valuations. Notably, adding bathrooms and floors, along with waterfront views, contributes to increased house values. Our predictive model, informed by various factors, offers valuable insights. For instance, a property with 7 bedrooms, 6 bathrooms, 9,500 square feet, 2 floors, waterfront view, excellent condition, and located in the 98004 zip code is estimated at US$2,607,762.39. This prediction stems from a comprehensive consideration of diverse factors during the model training phase, empowering sellers with informed pricing strategies.

## Conclusions

**Answer to Business Questions**

1. **What are the significant factors influencing house prices in the real estate market?**

The analysis has identified several key factors that significantly influence house prices in the real estate market. Notably, variables such as square footage of living space (sqft_living), grade, and the number of bathrooms exhibit strong correlations with property prices. These findings suggest that the size, quality, and amenities of a property play crucial roles in determining its market value.

2. **How do different zipcode impact average property prices, and what factors contribute to these variations?**

Houses with similar features vary in price across the top 3 zip codes with higher average house price. Despite similar bedrooms, bathrooms, and square footage, pricing patterns differ. This highlights the impact of location on housing prices, emphasizing the key role of regional factors in shaping market dynamics and property values.

3. **How can this knowledge be effectively utilized to establish an optimal price prediction for sellers?**


To help sellers set the right prices, we found that where a home is located matters a lot. Even with similar features, like bedrooms and bathrooms, prices can differ. More bathrooms, floors, and a waterfront view increase a home's value. Our model predicts that a 7-bed, 6-bath, 9,500 sqft home in the 98004 zip code is worth around US$2,607,762.39. This helps sellers price homes accurately.

**Limitations:**
* **Data limitation.** 
    The analysis relies heavily on the given datasets, and the datasets' ability to represent the entire sale price within King County, USA is essential. Future efforts might involve obtaining more varied and comprehensive datasets to strengthen the reliability of the recommendations and conclusions.

* **External Factors.** 
    As with many industries, various external factors can influence house price. Factors such as but not limited to crime rate,  government policies, and economic factors can affect house price. Due to time constrains, analyses with external factor were not performed.

* **Dynamic Market.** 
    Real estate markets are dynamic, and house prices can be influenced by various factors that change over time. Predictions made by the model may become less accurate as market conditions evolve, and the model might need frequent updates to stay relevant.


**Future Steps:**

* **External Factors.**  Incorporate external factors like economic indicators, crime rates, and government policies into the analysis for a more accurate and robust predictive model.

* **Time Series Analysis.** Incorporate a time series analysis to understand how house prices change over time. This could involve analyzing seasonality, trends, and cyclic patterns in the real estate market. Time-related features or external factors like economic indicators over time 



# For More Information


See the full analysis in the <a href="https://github.com/ankysoemitro/Project2/blob/main/EDA_Notebook.ipynb">Jupyter Notebook</a> or review this 
<a href="https://github.com/ankysoemitro/Project2/blob/main/House_Presentation.pdf">presentation</a>.


# Repository Structure

```
├── data
│    └── column_names.md
│    └── kc_house_data.csv
├── images
├── .gitignore
├── Analysis.ipynb
├── EDA_Notebook.ipynb
├── House_Presentation.pdf
└── README.md
```


