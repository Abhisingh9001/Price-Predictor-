# Price-Predictor-
from sklearn.liinear_model import LinearRegression
import numpy as np

x = np.array([[1500,3,2],[2000,4,3],[1200,2,3],[1800,3,2],[2500,4,3]])
y = np.array([250000,350000,200000,400000])

model = LinearRegression()
model.fit(x,y)

x_new = np.array([[1600,3,2],[2200,4,2]])
predictions = model.predict(x_new)

for i, pred in enumerate(predictions):
     print(f"predicted price for house {i+1}: ${pred:.2f}")
