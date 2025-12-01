# QQQ Forecasting Using Options-Market Signals

This project builds a machine-learning model to forecast the **next-day directional movement** of the Invesco QQQ ETF using features engineered from its **end-of-day options data**. The model translates information embedded in the options market—such as volatility and sentiment—into a predictive exposure signal.

All processing, feature engineering, and modeling are implemented in a **single Jupyter Notebook**.

---

## Project Workflow

### Data Preprocessing
- Handling and cleaning large QQQ options datasets (millions of rows).  
- Aggregating daily option-level data into summary features.  
- Aligning options features with underlying QQQ price movements.

### Feature Engineering
Examples of features created from options data:
- Put–call volume ratios  
- Implied volatility metrics (ATM IV, term structure)  
- Realized vs implied volatility spreads  
- Aggregated volume and open interest statistics  

### Modeling
- Transforming daily features into next-day exposure predictions.  
- Models tested: Ridge Regression, PCA-based approaches.  
- Predicted exposure constrained to a custom range (e.g., –1.0 to +1.5).  
- Train/validation split used for evaluation and robustness checks.

### Evaluation
- **Calmar Ratio** on training and validation sets.  
- Directional accuracy and feature importance for interpretability.  
- Results reflect full 5-year dataset; metrics provide insight into model performance.

### Limitations
- Full challenge dataset is proprietary and **not included**.  
- No full walk-forward backtesting or trading simulation.  
- Metrics are based on train/validation sets; results may differ on other data.  

### Reproducibility
- Two **small sample datasets** (`sample_options_QQQ.csv`, `sample_options_SPY.csv`) are included for demonstration purposes.  
- Full results reflect the proprietary data and cannot be reproduced publicly.

### Future Improvements
- Add walk-forward validation and backtesting.  
- Test additional models (XGBoost, LightGBM, CatBoost).  
- Include macro and cross-asset features for richer predictions.  

---

## Repository Structure

