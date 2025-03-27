
---

# **PowerCast: Germany Electricity Price Forecasting Model**  

## **Overview**  
PowerCast is a machine learning-based model designed to forecast electricity prices in Germany, benefiting traders, grid operators, and policymakers. It utilizes an ensemble of **XGBoost** and **Random Forest** models with energy price data, generation sources, and grid metrics. The model achieves **62.7% directional accuracy**, captures **40% of extreme price spikes**, and helps optimize trading strategies, ensure grid stability, and promote renewables.  

## **Key Findings**  
- **Price Trends**: Peak at **110–120 €/MWh** (morning & evening), drop to **70 €/MWh** at night. Weekends average **65–70 €/MWh**.  
- **Wind Impact**: High wind generation reduces prices by **32.41 €/MWh**, often dropping below **100 €/MWh** at **20,000+ MW** wind output.  
- **Correlations**: Prices rise with **fossil fuel usage (0.67)** and **unmet demand (0.82)**, but fall with **renewable adoption (-0.78)**.  
- **Model Performance**: **RMSE: 26.00, MAE: 16.40, R²: 0.8350**, capturing **40% of extreme events**.  
- **Feature Importance**: SHAP analysis highlights **renewable_demand_ratio**, **fossil_ratio**, and **conventional_vs_renewable** as key factors.  

## **Benefits for the Energy Sector**  
- **Traders**: Maximize profits by leveraging weekly price cycles (**Sunday 65 €/MWh, Tuesday 98 €/MWh**).  
- **Grid Operators**: Store energy during low-price periods (**32.41 €/MWh savings**) for peak demand management.  
- **Policymakers**: Encourage renewables to stabilize prices and reduce volatility.  

## **Repository Structure**  
- **data/**: Raw and processed datasets.  
- **models/**: Trained models (**XGBoost, Random Forest, Ensemble**).  
- **notebooks/**: Step-by-step Jupyter Notebooks for **EDA, training, SHAP analysis, and visualizations**.  
- **report/**: Final **PowerCast_Report.pdf** with findings.  
- **src/**: Python scripts for **data processing, model training, and interpretation**.  

## **Installation**  
1. Clone the repository:  
   ```bash
   git clone https://github.com/[YourUsername]/PowerCast-Germany-Electricity-Price-Forecasting.git  
   cd PowerCast-Germany-Electricity-Price-Forecasting  
   ```  
2. (Optional) Set up a virtual environment:  
   ```bash
   python -m venv venv  
   source venv/bin/activate  # Windows: venv\Scripts\activate  
   ```  
3. Install dependencies:  
   ```bash
   pip install -r requirements.txt  
   ```  
4. Launch Jupyter Notebook:  
   ```bash
   jupyter notebook  
   ```  

## **Usage**  
- **Data Exploration**: Run `notebooks/01_data_preprocessing.ipynb` and `notebooks/02_eda.ipynb` for insights.  
- **Model Training**: Train models via `notebooks/03_model_training.ipynb`.  
- **Feature Analysis**: Use `notebooks/04_model_interpretation.ipynb` for SHAP feature importance.  
- **Visualizations**: Generate report charts using `notebooks/05_report_visualizations.ipynb`.  
- **Automated Pipeline**: Run scripts in `src/` directory for end-to-end execution.  

## **Future Improvements**  
- Remove **leaky features** to improve model robustness.  
- Integrate **weather forecasts** for better accuracy.  
- Develop a **real-time API** for live electricity price forecasting.  

## **Contributing**  
Contributions are welcome! Focus areas include:  
- Enhancing model performance for **extreme price events**.  
- **Weather data integration** for improved accuracy.  
- **Better visualizations** for easier interpretability.  

## **License**  
This project is licensed under the **MIT License**.  

## **Contact**  
For questions or collaboration, contact **me** at **oluwatunmise1olaoluwa@gmail.com**.  

---
