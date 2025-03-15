# Social Media Usage and Emotional Well-Being: Analysis and Predictions

## Overview
This project explores the relationship between social media usage patterns and emotional well-being. Using a dataset on social media engagement, we analyze factors such as time spent on platforms, user interactions, and dominant emotions to predict daily usage time and uncover key insights.

## Goals
- Understand how social media usage correlates with emotional well-being.
- Develop a **multiple regression model** to predict **daily social media usage time**.
- Identify which features contribute most to predicting usage behavior.
- Provide recommendations for healthier social media habits.

## Technologies Used
- **Python** for data analysis and machine learning
- **Key libraries:**
  - `pandas` - Data manipulation
  - `numpy` - Numerical computations
  - `scikit-learn` - Machine learning
  - `matplotlib` & `seaborn` - Data visualization

## Dataset
- **Files Used:** `train.csv`, `test.csv`, `val.csv`
- **Key Features:**
  - `User_ID` – Unique identifier
  - `Age` – Age of the user
  - `Gender` – Gender of the user (Female, Male, Non-binary)
  - `Platform` – Social media platform used
  - `Daily_Usage_Time (minutes)` – Time spent on the platform per day
  - `Posts_Per_Day`, `Likes_Received_Per_Day`, `Comments_Received_Per_Day`, `Messages_Sent_Per_Day`
  - `Dominant_Emotion` – User's dominant emotional state (Happiness, Sadness, Anger, Anxiety, Boredom, Neutral)

## Data Preprocessing
- **Cleaned dataset** by removing rows with missing values.
- **Fixed incorrect entries** (76 rows where “Age” and “Gender” were swapped).
- **Converted data types** (`Age` from string to integer).
- **Applied one-hot encoding** to categorical variables.
- **Mitigated multicollinearity** by creating a new feature:  
  - `Activity_Score` = *Sum of Posts per Day, Likes Received per Day, Comments Received per Day, Messages Sent per Day.*

## Exploratory Data Analysis (EDA)
- **Correlation heatmaps** to identify relationships between variables.
- **Descriptive statistics** for dataset distribution.
- **Visualizations:**
  - Histogram of daily social media usage time.
  - Scatter plot showing the relationship between **Activity Score** and **Daily Usage Time**.
  - Feature importance analysis for predicting usage time.

## Regression Model
- **Model Type:** Multiple Linear Regression
- **Data Split:** 80% Training, 20% Testing
- **Performance Metrics:**
  - **R² Score:** 0.92
  - **Root Mean Squared Error (RMSE):** 10.35  
    *(On average, predictions deviate by ~10.35 minutes from actual usage.)*
- **Residual Analysis:** Evaluated errors and variance in predictions.

## Key Findings
- **Average Social Media Usage:** Most users spend between **60 - 100 minutes per day**.
- **Strongest Predictor:** **Activity Score** has the highest correlation with daily usage time.
- **Platform Insights:** Some platforms encourage higher engagement and longer screen time.
- **Gender and Emotion Trends:**
  - Differences in usage time by **gender** across platforms.
  - Relationship between **dominant emotion** and social media consumption.

## Visualizations
### **How Long Do People Use Social Media?**
- Histogram of daily usage time distribution.

### **Which Features Are Most Important?**
- Bar graph showing feature importance in predicting social media usage.

### **Social Media Usage by Platform and Gender**
- Bar graph comparing average daily usage time across different platforms by gender.

### **Emotions and Social Media Consumption**
- Bar graph showing the relationship between dominant emotions and social media usage.

## Conclusion & Recommendations
### **Limitations**
- The dataset focuses **only on social media usage**, without accounting for **external factors** (e.g., lifestyle, work, sleep).
- The **average age** in the dataset is **27.5**, which may not fully represent younger college students.
- Each record **only captures one social media platform** per user.
- The dataset **does not include** popular platforms like **TikTok and YouTube**, which could impact findings.

### **Suggestions for Future Research**
- Conduct a **survey on college students** and include **multiple platforms per user**.
- Combine social media usage with **other lifestyle data** (e.g., sleep, exercise, academic performance).
- Develop a **predictive model** for users’ **dominant emotional state**.

### **Practical Takeaways for Social Media Users**
- **Curate Your Feed** – Follow content that supports emotional well-being.  
- **Take Breaks** – Periodic detoxing can improve mental clarity and reduce stress.  
- **Be Mindful of Engagement** – Excessive activity on some platforms correlates with negative emotions.

## Contributors
This project was conducted by:
- **Orlando Marin**
- **Tatiana Eng**
