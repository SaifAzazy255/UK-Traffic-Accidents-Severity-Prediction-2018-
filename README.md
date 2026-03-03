# 🚗 UK Traffic Accidents Severity Prediction (2018)
# 📌 Project Overview
This project aims to predict the severity of casualties in road accidents across the UK using the official 2018 dataset. By integrating multiple relational tables (Accidents, Vehicles, and Casualties), the model identifies key risk factors to help improve road safety and emergency response strategies.

# 🛠️ Tech Stack
Language: Python

Data Handling: Pandas, NumPy (Relational Data Joining & Merging)

Modeling: XGBoost, CatBoost, Scikit-learn

Visualization: Seaborn, Matplotlib

# 📊 Dataset Structure
The project involves a complex join of three main entities:

Accidents: Environmental factors (Weather, Light, Road Type).

Vehicles: Vehicle details (Type, Maneuvers, Skidding).

Casualties: Demographics and severity (The Target Variable).

# 🚀 The "95% Accuracy" Challenge (Data Leakage Fix)
One of the core technical achievements in this project was identifying Data Leakage.

Initial Result: The model achieved ~95% accuracy.

The Issue: Feature importance analysis revealed that Casualty_Severity (or related proxy features) was leaking information from the future into the training phase.

The Solution: Removed the leaking features and re-engineered the pipeline.

Final Result: A robust, reliable ~87% accuracy model that generalizes to real-world unseen data.

# 📈 Key Insights
Accident Severity Correlation: The overall Accident Severity is the strongest indicator of individual casualty outcomes, showing a direct link between high-impact crashes and severe injuries.

Infrastructure Hazards: Features like Carriageway Hazards (e.g., obstacles on the road or broken barriers) play a critical role in increasing the risk of high-severity accidents.

Vehicle Density: The Number of Vehicles involved in a single accident significantly scales the probability of multiple casualties, especially in urban areas.

Safety Implication: These findings suggest that improving road maintenance and rapid hazard removal could be more effective in reducing severe injuries than just focusing on speed limits.
