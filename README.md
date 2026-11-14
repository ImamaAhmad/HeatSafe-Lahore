# HeatSafe Lahore
### AI-Powered Heat-Risk Forecasting for Lahore Schools

**Veritas AI International High School Hackathon 2026**  
**Track:** AI + Climate  
**Project Status:** Experimental AI Prototype

---

## About the Project

HeatSafe is an AI-powered heat-risk forecasting prototype designed to help schools in Lahore anticipate potentially dangerous outdoor heat conditions.

Using historical weather observations and machine learning, HeatSafe predicts the next day's heat-risk category. It aims to support school administrators, principals, and sports coordinators in making informed decisions about outdoor activities such as sports, assemblies, and school events.

## The Problem

Lahore experiences extremely high temperatures, particularly during summer. Students participating in outdoor school activities may be exposed to potentially dangerous heat conditions.

Schools need better ways to anticipate high-risk weather days and plan outdoor activities accordingly.

## The Solution

HeatSafe analyses historical weather conditions and uses machine learning models to predict the following day's heat-risk category.

The system includes:
- Next-day heat-risk prediction.
- Interactive prediction dashboard.
- Live weather integration using Open-Meteo.
- Monthly and seasonal heat-pattern analysis.
- Dangerous-day detection and false-negative analysis.
- Prediction history and visualizations.

## Dataset

**Historical weather source:** Open-Meteo Historical Weather Data.

**Location:** Lahore, Pakistan  
**Period used:** 2016–2024  
**Observations:** 3,288 daily records

An initial dataset was also examined from [Pakistan Major Cities Daily Weather on Kaggle](https://www.kaggle.com/datasets/devmarwat/pakistan-major-cities-daily-weather). The 2024–25 dataset was excluded because of issues with the provided data.

## Heat-Risk Categories

HeatSafe uses four experimental temperature-based categories:

| Category | Temperature |
|---|---|
| Low | Below 30°C |
| Moderate | 30°C to below 35°C |
| High | 35°C to below 40°C |
| Extreme | 40°C or above |

These are experimental project classifications, not official health or government warning thresholds.

## Machine Learning Models

The project explores and compares:

- Random Forest Classifier
- Decision Tree Classifier
- Logistic Regression

The models are evaluated using:
- Accuracy
- Macro F1-score
- Balanced accuracy
- Dangerous-day precision and recall
- False negatives

## Reported Model Results

| Model | Accuracy | Macro F1 | Balanced Accuracy |
|---|---:|---:|---:|
| Random Forest | 85.34% | 82.72% | 83.78% |
| Decision Tree | 80.82% | 77.75% | 80.13% |
| Logistic Regression | 86.03% | 83.03% | 84.17% |

Random Forest's reported dangerous-day detection results:

- Dangerous-day recall: 87.28%
- Dangerous-day precision: 79.89%
- False negatives: 22

These are experimental results and require verification using a chronological target-date split and further independent testing.

## Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- IPyWidgets
- Open-Meteo API

## How to Run

1. Open `HeatSafe.ipynb` in Google Colab.
2. Ensure the required historical Lahore weather CSV is available.
3. Select **Runtime → Run all**.
4. Allow the notebook to process the dataset and train the models.
5. Open the interactive HeatSafe dashboard.
6. Enter weather information or use the live-weather integration.
7. Click **Predict Heat Risk** to view the result.

**Note:** The notebook may require internet access for Open-Meteo integration and the relevant dataset files to be available in the Colab environment.

## Project Development Phases

**Phase 1: Data Collection and Exploration**

**Phase 2: Heat-Risk Classification and Data Preparation**

**Phase 3: Machine Learning Development and Evaluation**

**Phase 4: HeatSafe Prediction System and Visualization**

## Future Improvements

- Validate predictions using additional independent weather observations.
- Improve model reliability and confidence calibration.
- Investigate missed dangerous heat days.
- Improve explanations of prediction factors.
- Explore integration with official weather alerts.
- Develop a more comprehensive school-focused dashboard.

## Safety Disclaimer

HeatSafe is an experimental decision-support prototype, not an official heat-warning system or medical assessment. Its predictions are not guarantees of safe conditions.

Schools should follow official weather alerts and established heat-safety guidance when planning outdoor activities.

## Acknowledgements

- Open-Meteo for historical and weather forecast data.
- Kaggle for the initial Pakistan weather dataset.
- Scikit-learn and the Python data science ecosystem.
- ChatGPT for development assistance and debugging.

