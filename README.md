**Nutritional Advisor Project**
**Overview**
The Nutritional Advisor is a personalized health assistant designed to provide users with tailored dietary and exercise recommendations based on their personal information and goals. Using machine learning, it predicts the user’s daily caloric needs and suggests suitable foods and workouts aligned with their preferences and lifestyle.

**Features**
Calorie Needs Prediction:
Utilizes a trained Random Forest regression model to estimate the calories a user requires to maintain their current weight, based on age, weight, height, and activity level.

**Personalized Diet Plan:**
Recommends food items from a nutrition dataset filtered by the user’s dietary preference (vegetarian or non-vegetarian) and target caloric intake adjusted for weight goals (loss, gain, or maintenance).

**Exercise Recommendations:**
Suggests exercises tailored to the user’s activity level to help achieve their fitness goals.
**
**User-Friendly Interaction:****
Collects relevant user inputs interactively and provides clear, actionable recommendations.

**Dataset**
**Food Nutrition Dataset:**
Contains detailed nutrition facts for various food items, including calories, protein, carbs, fats, dietary preference labels, and allergens. The dietary preference labels are cleaned and normalized to two categories: vegetarian and non-vegetarian.
**
**Exercise Dataset:**
Includes exercises categorized by activity level, with information on duration and estimated calories burned.
**
**User Profile Dataset:**
Provides user data used to train the calorie prediction model, including age, weight, height, activity level, and caloric needs.

**Installation & Setup**
Clone the repository (or download the project files).

Install required Python libraries:

bash
Copy
pip install pandas numpy scikit-learn joblib
Prepare datasets:

Place the cleaned food dataset (cleaned_correct_food_data.csv), exercise dataset, and user profile dataset in appropriate folders.

Update file paths in the main script accordingly.

Usage
Run the main script:

bash
Copy
python nutritional_advisor.py
Enter the prompted personal details:

Name
Age
Weight (kg)
Height (cm)
Gender (male/female)
Goal (weight loss / weight gain / maintenance)
Dietary preference (vegetarian or non-vegetarian) — input is validated
Activity level (low, medium, high)

**Receives:**
Personalized daily caloric needs estimate
A diet plan with five recommended food items fitting the caloric and dietary preferences
A workout plan with three recommended exercises matching the activity level
General instructions tailored to the user’s goal

Code Structure
**Data Loading & Preprocessing:**
Loads datasets and processes user profile data by calculating BMI and encoding activity levels numerically.

**Model Training:**
Trains a Random Forest regression model on user profile data to predict caloric needs.

**Recommendation Functions:**
Functions to recommend foods and exercises based on filtered datasets and user-specific parameters.

**User Interaction:**
Input functions to gather user information and validation for dietary preferences.

Main Function:
Coordinates the entire flow — taking input, predicting calories, generating recommendations, and displaying results.

Notes & Considerations
The dietary preference input is strictly limited to "vegetarian" and "non-vegetarian" to ensure consistency with the dataset.

The calorie adjustment for goals is based on a standard +/- 500 kcal rule, which can be further customized.

The datasets must be cleaned and normalized (especially dietary preferences) for accurate filtering.

The model assumes the dataset is representative and that features like age, weight, height, and activity level strongly influence calorie needs.

Future Improvements
Add support for more nuanced dietary preferences (e.g., vegan, pescatarian, gluten-free) by enhancing the dataset and filtering logic.

Incorporate more personalized fitness goals and adjust exercise recommendations accordingly.

Enhance user interface with a web or mobile app for better usability.

Include nutrient-specific goals (protein intake, micronutrients) in dietary recommendations.

License
This project is provided for educational purposes and personal use.

Contact
For questions or collaboration, please contact:

Your Zishan Sher
Email: sherxeeshan00@gmail.com

