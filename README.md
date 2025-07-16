
# Room Occupancy Estimation 

This project predicts room occupancy counts using various environmental sensor data such as temperature, light, CO2, sound, and motion. It implements and compares multiple regression models to find the most accurate prediction technique.

---

## 📁 Dataset Description

- **Source:** UCI Machine Learning Repository
- **Total Records:** 10,129
- **Features:**
  - Environmental Sensors: Temperature, Light, CO₂, Sound
  - Motion Detection: PIR Sensors
  - Temporal Info: Datetime, Hour, Day
- **Target Variable:** `Room_Occupancy_Count`

---
## 🧪 Experimental Setup (From UCI Source)

- The data was collected in a 6m × 4.6m room using a wireless sensor network (WSN) with 7 sensor nodes and 1 edge node.
- Sensor nodes transmitted data every 30 seconds in a star configuration.
- No HVAC systems were used during data collection.
- Data was collected over 4 days with occupancy ranging from 0 to 3 people (manually recorded).

### 🧠 Sensors Used

- **Temperature, Light, Sound, CO₂, PIR (Passive Infrared)**

### 🧰 Sensor Placement

- **S1–S4:** Temperature, Light, Sound
- **S5:** CO₂
- **S6–S7:** PIR (placed on ceiling ledges to maximize motion coverage)

## ⚙️ Technologies Used

- Python, Pandas, NumPy
- Scikit-learn
- Seaborn & Matplotlib for visualization

---

## 🧪 Models Implemented

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor
- Support Vector Regressor (SVR)
- Gradient Boosting Regressor

---

## 📈 Model Performance

| Model                    | R² Score | MAE    | MSE    | RMSE   |
|--------------------------|----------|--------|--------|--------|
| Linear Regression        | 0.7149   | 0.3239 | 0.2338 | 0.4836 |
| Decision Tree Regressor | 0.9664   | 0.0208 | 0.0276 | 0.1660 |
| Random Forest Regressor | 0.9765   | 0.0202 | 0.0193 | 0.1389 |
| Support Vector Regressor| 0.9225   | 0.0994 | 0.0635 | 0.2520 |
| Gradient Boosting       | 0.9682   | 0.0509 | 0.0261 | 0.1614 |

📊 *Random Forest* outperformed all models with the highest R² and lowest error metrics.

---

## 📊 Visualization

*Figure: Comparison of R² Scores across all regression models*
<img width="831" height="538" alt="image" src="https://github.com/user-attachments/assets/55321819-b751-4491-949d-3ad7b47d539c" />


---

## 📌 Key Findings

- Temperature, Light, CO₂,and PIR sensors were strong predictors of occupancy.
- Ensemble models performed best, especially **Random Forest** and **Gradient Boosting**.
- Simple models like Linear Regression struggled with non-linearity in the data.
---

## 🚀 Future Work

- Deploy the best model using Flask/Django for real-time prediction
- Integrate with IoT devices for live room monitoring
- Explore deep learning models for sequential data (e.g., LSTM)
---

## 🙋‍♀️ Author

**Mufeeda Saleem V**

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).
