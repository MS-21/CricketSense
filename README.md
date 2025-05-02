# CricketSense
IPL Match Outcome Predictor
## Project Objective
To build a robust machine learning model that can accurately predict:
- Match winner
- Team scores
- Key player performance (optional)
- Match outcome probabilities
## Tech Stack

| Layer            | Tools Used                                                                 |
|------------------|----------------------------------------------------------------------------|
| **Language**     | Python 3.9+                                                                |
| **Data Handling**| pandas, numpy                                                              |
| **ML Models**    | scikit-learn (Logistic Regression, Gradient Boosting)                      |
| **Visualization**| seaborn, matplotlib                                                        |
| **LLM Reasoning**| Ollama with custom prompts for match outcome explanation                   |
| **Backend APIs** | FastAPI / Django (for future deployment)                                   |
| **Environment**  | Jupyter Notebook, VS Code                                                  |
## Algorithms Used
- Logistic Regression
- Used as a baseline classifier to predict the match winner (a binary/multiclass classification problem).
- Good for interpretability and performs well on linearly separable features.
- Gradient Boosting / Ensemble Models
## Features Used for Prediction
The model was trained using structured IPL data. Key features (columns) used include:
- Feature	Description
- team1	First team (categorical)
- team2	Second team (categorical)
- toss_winner	Team that won the toss
- toss_decision	Whether the toss-winning team chose to bat or field
- venue	Stadium where the match was played
- season	Year of the IPL season
## LLM Integration
We used **Ollama LLM** to:
- Generate natural language reasoning for match predictions
- Convert structured features into match summaries
- Provide interpretable insights like:
> _"Given that CSK is batting first at Chepauk and won the toss, their win probability increases by 18% historically. Predicted winner: CSK"_
- LLM prompts included contextual match history, toss logic, and venue performance.
## ML Model Details
- Feature encoding using LabelEncoder
- Logistic Regression (Baseline)
- Gradient Boosting Classifier
- Test Accuracy: **83%**
- Evaluation: Accuracy, Confusion Matrix, Precision/Recall (future work)
## Future Enhancements
- Add LSTM/Transformer models for time series prediction
- Include live updates from IPL feeds
- Build full-stack web interface using FastAPI + React
- Provide match explanations through LLM responses
- Add retraining pipeline and model monitoring
