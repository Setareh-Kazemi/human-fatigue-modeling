# Human Fatigue Dataset (Python Format)

## Overview

This folder contains a Python-compatible version of the human fatigue dataset collected during a controlled order-picking experiment. The data include wearable sensor measurements, participant anthropometric characteristics, subjective fatigue assessments, and experimental condition settings.

The complete dataset is maintained in R format (`.RData`). To facilitate use by the Python community, we additionally provide a Python pickle (`.pkl`) version of the dataset.

**Current release:** The Python dataset contains the first 45 minutes of each experimental session, corresponding to the work period. Recovery-period data are not included in the current release and will be added in a future update.

The dataset file can be downloaded from:

**[FIGSHARE LINK]**

---

## Dataset Structure

The pickle file contains a dictionary with three top-level entries:

* `ts_data`
* `anthro_clean`
* `experiment_settings`

### ts_data

`ts_data` is a dictionary indexed by `(Subject, Session)` tuples.

Examples:

* `('Sub01', 'Session1')`
* `('Sub01', 'Session2')`
* `('Sub02', 'Session1')`

Each entry contains a pandas DataFrame with timestamped observations from wearable sensors and subjective fatigue assessments.

Variables include:

* Subject identifier
* Session identifier
* Timestamp
* Trunk accelerometer, gyroscope, and magnetometer signals (X, Y, Z)
* Upper-arm accelerometer, gyroscope, and magnetometer signals (X, Y, Z)
* Wrist accelerometer, gyroscope, and magnetometer signals (X, Y, Z)
* `RPE_Val` (Rating of Perceived Exertion)
* `Activity_Type`

### anthro_clean

`anthro_clean` is a pandas DataFrame containing participant demographic and anthropometric information.

Variables include:

* Subject
* Gender
* Age
* Height (cm)
* Weight (kg)
* Waist circumference (cm)
* Hip circumference (cm)

### experiment_settings

`experiment_settings` is a dictionary indexed by subject identifier.

Each entry contains the workload conditions assigned to Sessions 1–4, including:

* `Weight` – load handled during the order-picking task
* `Pace` – prescribed work pace

---

## Loading the Dataset

```python
import pickle

with open("NIOSH_Combined_Dataset.pkl", "rb") as f:
    loaded_data = pickle.load(f)

ts_data = loaded_data["ts_data"]
anthro_clean = loaded_data["anthro_clean"]
experiment_settings = loaded_data["experiment_settings"]
```

---

## Example Data Access

### Time-Series Data

```python
ts_data[("Sub01", "Session1")].head()
```

### Anthropometric Data

```python
anthro_clean.head()
```

### Experimental Settings

```python
experiment_settings["Sub01"]
```

---

## Citation

If you use this dataset in research, publications, presentations, or derivative works, please cite the associated dataset and any related publications when available.

---

## Notes

* This release contains only the first work-period portion of the experiment (first 45 minutes).
* Recovery-period data will be included in a future release.
* The pickle file is intended for Python users and mirrors the structure of the original dataset as closely as possible.
* The complete dataset is maintained in R format (`.RData`) and is available in the `full_sensor_data` directory.

