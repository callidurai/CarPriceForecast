README 

DESCRIPTION

This application is designed to predict the best value of your car based on 5 different predictors. There are two components
to this program, a backend piece which is the ML models themselves and a Frontend component that lets the user interact with 
the model. The backend consists of a model that needs to be trained and pickled and this pickle file can then be passed into 
the code for the frontend. The frontend is a raw HTML, CSS form paired with a python Flask based API, with two endpoints. The
/predict endpoint is connected to the frontend to process the form data, while the /api endpoint is configured to be called from 
a direct POST request to test the model. 

## add to this description as you see fit for the model part of it.


INSTALLATION

FRONT END
- Make sure Python3 is installed. Frontend app.py is built on top of python3
- Install Fask 
    run following command in terminal: pip3 install flask

BACKEND MODEL
- Install and import the following libraries
    import numpy as np
    import pandas as pd
    from datetime import datetime
    import uszipcode
    from uszipcode import SearchEngine
    import gc
    import os

    import matplotlib.pyplot as plt
    import seaborn as sns
    from sklearn.tree import export_graphviz

    from sklearn.preprocessing import MinMaxScaler
    from sklearn.model_selection import train_test_split
    from sklearn.model_selection import cross_val_score
    from sklearn.metrics import mean_squared_error
    from sklearn.metrics import r2_score
    from sklearn.inspection import permutation_importance
    from sklearn.model_selection import KFold
    from sklearn.model_selection import cross_val_score

    from statsmodels.stats.outliers_influence import variance_inflation_factor
    from statsmodels.tools.tools import add_constant
    from scipy import stats

    from sklearn.linear_model import LinearRegression
    from sklearn.ensemble import RandomForestRegressor
    from sklearn.tree import DecisionTreeRegressor
    from sklearn.model_selection import GridSearchCV
    from sklearn import tree

    import fredapi as fa

EXECUTION

Backend
-------------------
    Run code in Jupyter Notebook
    Output will be a pickled model that can be interacted with through its predict function. The Front End's inputs correspond to the predict function,         which will create the prediction.


Frontend 
-------------------
1. Update line 20 of the app.py file with the name of the pickle file created in backend step
2. Start Python application 
    b. Run following command in terminal: python3 app.py 
3. Copy url from output of previous command. Ex: "http://127.0.0.1:5001"
4. Paste this url into your browser and you should see a form pop up
5. Enter vehicle information and click "Predict" to see the output.
6. Click "Reset Form" to reset the form and try a new prediction
