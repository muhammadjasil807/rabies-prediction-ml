Rabies Prediction in Humans using Machine Learning

An AI/ML powered Rabies Prediction System that uses XGBoost to estimate the risk of rabies infection in humans based on exposure details such as animal type, environment, and symptoms.
Deployed with Streamlit for an interactive and user-friendly web interface.

Overview
This project demonstrates an end to end Machine Learning pipeline from dataset creation to deployment — for predicting rabies risk in humans.

Users can input details like:

* Whether the animal is alive or not
* Animal type (Dog, Cat, Other)
* Visit and exposure information
* Multiple symptoms (like fever, aggression, paralysis, etc.)

The trained model then predicts whether the human is at high or low risk of rabies.

Features

* Interactive web interface (built with Streamlit)
* Multi-symptom input (choose up to 3 symptoms)
* Smart alerts for strong rabies symptoms
* End-to-end ML pipeline using scikit-learn and xgboost
* Deployed locally via Streamlit and Ngrok


Tech Stack
Programming Language: Python 3
ML Algorithm: XGBoost Classifier
Preprocessing: Scikit-learn Pipelines, OneHotEncoder, SimpleImputer
Frontend / UI: Streamlit
Deployment: Streamlit + Pyngrok
Model Saving: Joblib


Project Structure

rabies-prediction-ml
│
├── rabies_data.csv              (Sample dataset)
├── rabies_notebook.ipynb        (Model training notebook in Colab)
├── app.py                       (Streamlit web app)
├── xgb_rabies_pipeline.pkl      (Trained model file)
├── requirements.txt             (Dependencies)
└── README.md                    (Project documentation)


Installation and Running

Step 1 — Clone the Repository
git clone [https://github.com/YOUR-USERNAME/rabies-prediction-ml.git](https://github.com/YOUR-USERNAME/rabies-prediction-ml.git)
cd rabies-prediction-ml

Step 2 — Install Dependencies
pip install -r requirements.txt

Step 3 — Run the Streamlit App
streamlit run app.py

Step 4 — (Optional) Get a Public Link using Ngrok
from pyngrok import ngrok
ngrok.connect(8501)


Model Details
Model Used: XGBoost Classifier
Target Variable: rabies_status
Input Features: animal_alive, animal, PEP_RECOMMENDED, VISIT_STATUS, victim_environment, animal_environment, symptoms
Preprocessing: SimpleImputer + OneHotEncoder
Evaluation Metrics: Accuracy, Classification Report


Example Output

User Input:
Animal: Dog
Symptoms: Aggression, Hydrophobia

Output:
Strong rabies-related symptoms detected — high vigilance recommended.
High Risk of Rabies (Probability: 0.92)

User Input:
Symptoms: None

Output:
No rabies-related symptoms selected. Low risk likely.
Low Risk of Rabies (Probability: 0.10)

Future Improvements

* Add real-world medical dataset
* Include bite location and exposure type
* Deploy on Streamlit Cloud or Hugging Face Spaces
* Add doctor’s recommendation section

Author
Muhammad Jasil E.K.
LinkedIn: [https://linkedin.com/in/YOUR-LINKEDIN](https://linkedin.com/in/YOUR-LINKEDIN)
GitHub: [https://github.com/YOUR-USERNAME](https://github.com/YOUR-USERNAME)

Conclusion
This project demonstrates how Machine Learning can assist in healthcare risk assessment using structured data and intelligent modeling.
It’s a foundation for developing more advanced, real-world medical AI systems.


