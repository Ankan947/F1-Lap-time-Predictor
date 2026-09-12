F1 Lap Time Predictor

What is this project about?
This is a Machine Learning project I built to predict Formula 1 lap times by analyzing tire degradation. I wanted to see if an ML model can actually track how much a tire wears out during a race stint.

What data did I use?
I used the Kaggle Formula 1 dataset. To keep the weather and track conditions constant, I specifically looked at the 2019 Italian GP at Monza (dry track, no red flags) and selected the top finishing drivers.

The Models I Compared:
Baseline Model (Linear Regression) - This one just looks at the driver and guesses an average lap time. It completely ignores tire age.
Smart Model (Random Forest) - This one takes 'Tire Age' into account to predict the lap time.

Results:
Here is the visual comparison of the model predictions for Stint 2:
<img width="1600" height="655" alt="Code_Generated_Image" src="https://github.com/user-attachments/assets/e698f596-91cd-474a-95c1-d313ec274edc" />
My Random Forest model successfully tracked the real-world tire degradation curve! Even though the baseline model had a slightly lower raw RMSE (because it just drew a safe, flat average line ignoring the slow out-laps), my Random Forest model actually followed the real lap time trend perfectly in the stint-based testing.

How to run this locally:
1.Clone this repository.

2.Download the Kaggle F1 dataset (you will need lap_times.csv, pit_stops.csv, and results.csv).

3.Put those CSV files in the same folder as the python script.

4.Run pip install pandas scikit-learn matplotlib in your terminal.

5.Run the python file.
Tech Stack Used:
Python, Pandas for data cleaning, Scikit-Learn for ML models, and Matplotlib for graphing the degradation curve.


