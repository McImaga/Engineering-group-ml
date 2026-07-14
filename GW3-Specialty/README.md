# California Housing Price Prediction

Predicting median house values in California using the California Housing dataset. 
Built as part of a team project to compare Linear, Lasso, Ridge, and Polynomial Regression models.

## **Dataset**
- **Source**: [California Housing Dataset - Scikit-learn](https://www.scikit-learn.org/stable/modules/generated/sklearn.datasets.fetch_california_housing.html)
- **Target**: `MedHouseVal` - Median house value in $100,000s
- **Features**: 8 features including `MedInc`, `HouseAge`, `AveRooms`, `Latitude`, `Longitude`, etc.
- **Rows**: 20,640

## **Project Structure**

├── data/                     # Raw dataset  
├── notebooks/  
│  └── mult_col_polyreg.ipynb  # Main analysis notebook    
├── src/                    # Helper functions  
├── models/                 # Saved models  
└── http://README.md

**Approaches Tested**
1.  **Linear Regression** - Baseline model
2.  **Polynomial Regression** - Degree 2 features with scaling
3.  **Lasso Regression** - L1 regularization with GridSearchCV
4.  **Ridge Regression** - L2 regularization with GridSearchCV

Best model: `Ridge with alpha=0.0001` → R2 = 0.61, RMSE = 0.72

**Key Findings**
- Scaling was critical. Without `StandardScaler`, Ridge/Lasso performed poorly
- `MedInc` and `Latitude/Longitude` were the most important features
- Polynomial features improved performance but risked overfitting


### Team Members
1.  Ifeanyichukwu Imaga Agwu
2.	Victor Chinedu Ezebuiro
3.	Isaac Godspower C.
4.	Nduka, Chukwuemeka J.
5.	Nnokwe Franklin Okechukwu
6.	Anosike Joy Ogechi
7.	Prosper Chukwuemeka Nwankwo
8.	Henry Ajunwa Chibuike
9.	Udi Anita Nzubechukwu
10.	Okafor Enyinnaya Udeh
11.	Chukwuemeka Chimbuchi


*Results Summary*
Model	R2 Score	RMSE
Linear Regression	0.59	0.74
Lasso	0.60	0.73
Ridge	0.61	0.72
Polynomial	0.63	0.70


