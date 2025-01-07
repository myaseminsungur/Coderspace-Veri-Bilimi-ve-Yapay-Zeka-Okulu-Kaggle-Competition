# Football Player Value Prediction Project

## Competition Overview
This project is part of the Coderspace Data Science and AI School (Veri Bilimi ve Yapay Zeka Okulu)'s final phase Kaggle competition. The goal is to predict which football players' market values will increase based on their attributes and characteristics.

### Definition of Value Increase:
A player is considered to have increased in value if:
- Market value at the start of 22/23 season (September 2022) was below $5M
- Market value at the start of 24/25 season (September 2024) is $10M or above
- Born on or after 2000-01-01

## Project Overview
The challenge is to predict whether a player's value will increase (True/False) using various player attributes, including physical characteristics, skills, and positions. The data combines player valuations from Transfermarkt and player attributes from Football Manager.

## Data Description
The dataset contains rich information about football players including:

### Key Features:
- **Basic Information:**
  - Player ID (unique identifier)
  - Current ability and potential
  - Positions played
  - Physical attributes (Height, Weight, Foot preference)
  - International caps and goals

### Technical Attributes:
1. **Goalkeeper-specific:**
   - Aerial Reach
   - Command of Area
   - Communication
   - Handling
   - One on Ones
   - Reflexes

2. **Outfield Players:**
   - Technical Skills (Dribbling, Finishing, Tackling, etc.)
   - Mental Attributes (Decisions, Leadership, Vision, etc.)
   - Physical Attributes (Acceleration, Stamina, Strength, etc.)

## Analysis Steps

### 1. Data Loading and Initial Exploration
- Imported necessary libraries (pandas, numpy, matplotlib, seaborn)
- Loaded the training dataset
- Performed initial data exploration using head(), info(), and describe()

### 2. Exploratory Data Analysis (EDA)
- Created correlation matrix visualization to understand feature relationships
- Analyzed the distribution of target variable (value_increased)

### 3. Data Cleaning and Preprocessing
- Handled missing values
- Processed categorical variables:
  - Split 'Caps / Goals' into separate columns
  - Converted Height and Weight to numeric values
  - Encoded 'Foot' column (Left/Right) to binary values
  - Performed one-hot encoding for player positions
- Created a preprocessing pipeline for consistent data transformation

### 4. Model Development
- Split data into training and test sets
- Addressed class imbalance
- Used PyCaret for automated machine learning:
  - Compared multiple classification models
  - Selected best performing model based on F1 score
  - Performed hyperparameter tuning
  - Finalized the model for predictions

## Technologies Used
- Python 3.9
- Key libraries: pandas, numpy, scikit-learn, PyCaret
- Visualization: matplotlib, seaborn

## Results
The analysis produced a classification model capable of predicting whether a player's value will increase, with evaluation metrics showing the model's performance on unseen data.

## Future Improvements
- Feature engineering to create more informative variables
- Deep learning approaches for better prediction accuracy
- Ensemble methods combining multiple models
- More extensive hyperparameter tuning
- Integration of additional external data sources 