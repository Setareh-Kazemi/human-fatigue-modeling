# Raw IMU Signals Dataset

You can find the raw IMU signals at this link: 
[Figshare](https://figshare.com/s/c6c4dd74bdd29e4cb5a3)

This `.RData` file consists of three main components:

---

### 1. ActiGraph_IMU_Data
A list containing **204 dataframes**, each associated with a unique combination of subject, session, and body part. Each dataframe includes the following 10 columns:
* **Timestamp**: Captured in Unix time format.
* **Accelerometer**: `Accelerometer.X`, `Accelerometer.Y`, `Accelerometer.Z`
* **Gyroscope**: `Gyroscope.X`, `Gyroscope.Y`, `Gyroscope.Z`
* **Magnetometer**: `Magnetometer.X`, `Magnetometer.Y`, `Magnetometer.Z`

### 2. ActiGraph_IMU_DF
A mapping dataframe providing metadata for the 204 unique combinations found in `ActiGraph_IMU_Data`. The dataset tracks:
* **17 subjects**
* **4 sessions** * **3 body parts**: Trunk, wrist, and upper arm.

> **Note:** The mapping between session numbers and specific task conditions can be found in [NIOSH_Experiment_Settings.xlsx](data/NIOSH_Experiment_Settings.xlsx).

### 3. RPE_Data
A list of **68 dataframes** associated with unique subject-session combinations. Each dataframe contains three columns:
* **time**: Ranging from 0 to 45 with a step size of 5.
* **RPE**: Rate of Perceived Exertion; a value from `0` (minimum fatigue) to `10` (maximum fatigue).
* **type**: Categorized work/break periods with the following unique values:
  * `active1` (First work period)
  * `rest1` (First break period)
  * `active2` (Second work period)
  * `rest2` (Second break period)
  * `active3` (Third work period)

> **Note:** `NA` values indicate that no RPE values were reported for those specific time points.

---

### Missing Data Notice
* `NULL` list elements in both `ActiGraph_IMU_Data` and `RPE_Data` indicate that no experimental data was captured for that specific subject-session combination.
