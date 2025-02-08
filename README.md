# Project Title: Student Performance Insights and Recommendations

## Overview
This project focuses on analyzing student performance data, identifying weak areas, improvement trends, and performance gaps, while estimating difficulty levels of quizzes based on student accuracy. It also offers actionable recommendations and defines student personas to support learning strategies.

## Workflow

### 1. **Data Loading and Preparation**
   - Mount Google Drive to access datasets.
   - Load three JSON datasets:
     - Quiz metadata (`quiz.json`)
     - Quiz questions (`Quizendpoint.json`)
     - User performance data (`apiendpoint.json`)
   - Normalize nested JSON structures into pandas DataFrames for easy analysis.

### 2. **Data Cleaning and Formatting**
   - Parse and clean relevant columns such as timestamps (`submitted_at`) and numerical data (`score`, `accuracy`).
   - Convert percentage values to numeric types.
   - Handle missing or corrupted data gracefully.

### 3. **Feature Engineering**
   - Estimate quiz difficulty levels using response accuracy:
     - **Easy:** Accuracy ≥ 90%
     - **Medium:** 70% ≤ Accuracy < 90%
     - **Hard:** Accuracy < 70%

### 4. **Data Analysis**
#### a. **Generating Insights**
   - Identify weak areas by calculating average scores per topic.
   - Analyze improvement trends based on chronological scores.
   - Detect performance gaps by counting missed questions.
   - Analyze performance by estimated difficulty levels.

#### b. **Defining Student Personas**
   - Categorize students based on performance patterns.
   - Highlight top-performing topics and areas with most mistakes.
   - Assign persona labels such as "Persistent Learner" or "Rising Star" based on score thresholds.

### 5. **Generating Recommendations**
   - Focus on weak topics for improvement.
   - Encourage sustained improvement or suggest reviewing prior topics.
   - Provide strategies for managing difficult questions and improving accuracy.

### 6. **Example Outputs**
   - **User Insights:** Key metrics on weak areas, improvement trends, and performance by difficulty.
   - **Recommendations:** Tailored suggestions to enhance learning.
   - **Student Persona:** A descriptive profile of student strengths and challenges.

## Key Functions
- `estimate_difficulty`: Estimates difficulty based on accuracy.
- `generate_user_insights(user_id)`: Provides insights for a specific user.
- `define_student_persona(user_id)`: Defines a persona for the student.
- `generate_recommendations(insights)`: Generates actionable recommendations.
- Bonus- NEET dataset is assumed statically and then prediction for NEET Rank is made.

## How to Run
1. Upload the required JSON files to Google Drive.
2. Execute the notebook in Google Colab.
3. Replace `user_id` in example code with a valid user ID from the dataset.
4. Review generated insights, recommendations, and personas.
