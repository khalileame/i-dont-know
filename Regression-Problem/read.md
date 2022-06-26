To use the model whenever you want , just open a jupyter notebook, give the data that you have and then send it . Then you ll have the reply from the app deployed in heroku
vehicle_config = {
    'Cylinders': [4, 6, 8],
    'Displacement': [155.0, 160.0, 165.5],
    'Horsepower': [93.0, 130.0, 98.0],
    'Weight': [2500.0, 3150.0, 2600.0],
    'Acceleration': [15.0, 14.0, 16.0],
    'Model Year': [81, 80, 78],
    'Origin': [3, 2, 1]
}

import requests
url ="https://fuel-efficiency-predicti.herokuapp.com/"
r= requests.post(url,json =vehicle_config)
r.text.strip()
print(r)
