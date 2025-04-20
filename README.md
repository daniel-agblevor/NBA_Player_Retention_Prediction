# NBA Player Retention Prediction

This project focuses on feature engineering and predictive modelling using NBA player data. The goal is to predict whether a player will remain in the league for 5 years (`target_5yrs`) based on various performance metrics.

## Project Structure

```
data/
    extracted_nba_players_data.csv  # Processed NBA player data
    nba-players.csv                # Raw NBA player data
models/
    logistic_model.pkl             # Logistic Regression model trained on all features
    logistic_model1.pkl            # Logistic Regression model trained on selected features
Notebooks/
    predictive_modelling.ipynb     # Notebook for predictive modelling
    Preparing NBA dataset for Modelling..ipynb  # Notebook for data preparation
```

## Key Steps

1. **Data Preparation**:
   - Data is loaded and cleaned from `data/extracted_nba_players_data.csv`.
   - Correlation heatmaps and boxplots are used for exploratory data analysis.

2. **Feature Engineering**:
   - Feature importance is calculated using Logistic Regression coefficients.
   - A subset of important features is selected for a second round of modelling.

3. **Predictive Modelling**:
   - Logistic Regression is used to predict `target_5yrs`.
   - Models are evaluated using metrics like accuracy, precision, recall, and F1 score.

4. **Model Saving**:
   - Trained models are saved in the `models/` directory for future use.

## How to Run

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd NBA_Player_Retention_Prediction
   ```

2. Install required libraries:
   ```bash
   pip install -r requirements.txt
   ```

3. Open the Jupyter Notebooks in the `Notebooks/` directory to explore the analysis and modelling steps.

4. Run the notebooks to reproduce the results.

## Results

- The first Logistic Regression model achieved the following metrics:
  - Accuracy: 71%
  - Precision: 75%
  - Recall: 80%
  - F1 Score: 78%

- The second Logistic Regression model (with selected features) achieved:
  - Accuracy: 68%
  - Precision: 71%
  - Recall: 81%
  - F1 Score: 76%

## Future Work

- Experiment with other machine learning algorithms (e.g., Random Forest, XGBoost).
- Perform hyperparameter tuning to optimize model performance.
- Explore additional feature engineering techniques.

## License

This project is licensed under the MIT License. See the LICENSE file for details.
