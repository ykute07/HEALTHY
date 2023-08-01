# HEALTHY
LSTM-based Autoencoder Anomaly Detection (HEALTHY) is primarily developed to detect abnormal resting heart rate (RHR) during the Coronavirus (SARS-CoV-2) infectious period. It uses heart rate and physical activity data from smartwatches like Fitbit, Apple and Garmin. Further, it splits data into training (baseline) and test based on the participant's self-reported symptom date and COVID-19 infectious period. It learns the structure of the baseline data for each user by reconstructing the temporal sequences and calculates a reconstruction error. Using this error it builds an anomaly threshold and detects if the RHR sequences in the test data are anomalous (abnormal) or not.

Link to the research paper - https://www.medrxiv.org/content/10.1101/2021.01.08.21249474v1


### Installation 

``` 
git clone https://github.com/ykute07/HEALTHY.git
cd HEALTHY
pip install -r dependencies.txt
```

### Usage

```
python healthy.py  --heart_rate data/ASFODQR_hr.csv --steps data/ASFODQR_steps.csv --myphd_id ASFODQR --symptom_date 2024-08-14
```



### HEALTHY architecture

<p align="center">
<img width="800" alt="HEALTHY" src="https://user-images.githubusercontent.com/3885659/102735228-b4583600-42f6-11eb-9c2f-5af2ae614dab.png">
</p>

### Results

#### Reconstruction error (loss)

<p align="middle">
<img width="228" alt="s_training" src="https://user-images.githubusercontent.com/3885659/102735598-bf5f9600-42f7-11eb-925d-7eb6c411c95a.png">
<img width="258" alt="s_pred_loss" src="https://user-images.githubusercontent.com/3885659/102735600-c25a8680-42f7-11eb-82a9-b23cc06965b6.png">
</p>

#### Predictions

<p align="middle">
<img width="904" alt="s_results" src="https://user-images.githubusercontent.com/3885659/102735856-53316200-42f8-11eb-8cfa-40b4508d6d7c.png">
</p>

