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

- Make sure Python3 is intalled. Frontend app.py is built on top of python3
- Install Fask 
    run following command in terminal: pip3 install flask

## add any packages you used in your code here 


EXECUTION

Backend
--------------------
1. Train Model 
2 Pickle Model 


Frontend 
-------------------
1. Update line 20 of the app.py file with the name of the pickle file created in backend step
2. Start Python application 
    b. Run following command in terminal: python3 app.py 
3. Copy url from output of previous command. Ex: "http://127.0.0.1:5001"
4. Paste this url into your browser and you should see a form pop up
5. Enter vehicle information and click predict to see the output.
