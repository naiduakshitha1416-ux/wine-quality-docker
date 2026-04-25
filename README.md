# Wine Quality Prediction using Docker

## About the Project

This project predicts whether a wine is good or bad based on its chemical properties.
I trained a machine learning model using the Wine Quality dataset and deployed it with Flask inside a Docker container.

---

## Tools Used

* Python
* Flask
* Scikit-learn
* Pandas / NumPy
* Docker

---

## Project Files

```text id="ihg99l"
app.py           → Flask API code  
train.py         → Model training script  
model.pkl        → Saved trained model  
Dockerfile       → Docker setup  
requirements.txt → Python libraries  
winequality.csv  → Dataset  
```

---

## How It Works

1. Train the model using the dataset
2. Save the trained model
3. Load model in Flask API
4. Run everything inside Docker

---

## Run the Project

### Build Docker Image

```bash id="bdiyiv"
docker build -t wine-quality-app .
```

### Run Docker Container

```bash id="59g91t"
docker run -p 5000:5000 wine-quality-app
```

---

## API Testing

### Home URL

```text id="fwjlwm"
http://localhost:5000/
```

### Prediction API

```text id="hykcfw"
POST /predict
```

Sample Input:

```json id="kk0p5t"
{
  "features":[7.4,0.7,0,1.9,0.076,11,34,0.9978,3.51,0.56,9.4]
}
```

Sample Output:

```json id="kzn1y1"
{
  "prediction": 0
}
```

---

## Future Improvements

* Add frontend UI
* Deploy on Azure
* Improve model accuracy

---

## Created By

Akshitha Naidu
