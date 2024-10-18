# <span style="color: orange; font-weight: bold;">Maven Halloween Challenge 🎃<span> 

    
[![Challenge Link](https://img.shields.io/badge/🍬%20Challenge%20Link-brightgreen)](https://mavenanalytics.io/challenges/maven-halloween-challenge/701f06a2-a19b-41e9-95d3-37a0dcc5492f) 

### Objective
- For the Maven Halloween Challenge, you’ll need to take a data-driven approach for becoming the most popular trick-or-treating house on the block.

- Using online votes ranking 85 types of candy, **The task is to find the 3 treats you'll give out on Halloween to guarantee that trick-or-treaters of all tastes find something they'll love and present the data to back up your decision.**

#### Project Overview  
This project aims to identify the **Top 3 Halloween candies** across multiple consumer preferences. By leveraging data science techniques like **SHAP (SHapley Additive exPlanations)** value analysis and **Composite Scoring**, we analyzed various candy attributes (e.g., chocolate, fruity, sugar content, price, etc.) to rank candies that not only excel in popularity but also fit specific consumer needs. The final output is presented through a **data-driven approach** that helps optimize candy choices for Halloween.

---

### Key Steps:

#### 1. Data Preparation:  
- Preprocessed the candy dataset by cleaning unnecessary columns and normalizing key features such as **sugar percent** and **price percent**.
- Created **custom metrics** by analyzing candy attributes relevant to specific preferences.


#### 2. Composite Scoring Formula:  
- Developed a **Composite Score** to rank candies based on their attributes, using SHAP values to weigh each feature's importance.

  <p style="color:purple;"><b>Composite Score = ∑ ( Feature Value × Feature Weight )</b></p>

- Combined **winpercent** (popularity) with the composite score using a weighted formula to balance consumer popularity and theoretical best fit:

  <p style="color:purple;"><b>Final Score = (Normalized Winpercent × Winpercent Weight) + (Normalized Composite Score × Composite Score Weight)</b></p>


#### 3. Normalization and Ranking:  
- Normalized both **winpercent** and **Composite Score** to bring them onto a comparable scale.
- Calculated a **Final Score** using these normalized values and ranked the candies accordingly, identifying the **Top 3 candies** across various preferences.


#### 4. Custom Metrics for Sweet Tooth and Price Sensitivity:  
- Created specialized scores based on **sugarpercent** and **pricepercent** to identify the **Top 3 candies** for people with a **sweet tooth** and **price-sensitive consumers**.


### Tools and Libraries:  
- **Pandas & NumPy**: For data manipulation, cleaning, and feature engineering.
- **Scikit-learn**: Used for modeling, including SHAP value computation and composite scoring.
- **SHAP**: To understand and visualize feature importance and their impact on the target variable (*winpercent*).
- **Matplotlib & Seaborn**: For creating visually engaging plots and heatmaps to communicate insights.
- **PowerPoint Visualizations**: Results presented in an interactive, visually appealing PowerPoint-style format.
