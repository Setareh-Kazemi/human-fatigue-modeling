## Title

**Predictive Modeling of Human Fatigue and Recovery**

--- 

## Project Members:  
- **Setareh Kazemi Kheiri, Department of Industrial Engineering, University of Pittsburgh**, **skazemi@pitt.edu**
- **Sahand Hajifar, Robert W. Plaster School of Business, Park University**, **sahand.hajifar@park.edu**
- **Fadel M. Megahed, Farmer School of Business, Miami University**, **fmegahed@miamioh.edu**
- **Lora A. Cavuoto, Department of Industrial and Systems Engineering, University at Buffalo**, **loracavu@buffalo.edu**
- **Hongyue Sun, College of Engineering, University of Georgia**, **hongyuesun@uga.edu**

---
## Objective:

In this document all the data related to the associated paper entitled "Predictive Modeling of Human Fatigue and Recovery" are provided. The main objective of this research is gaining a better understanding of fatigue and recovery dynamics during manual material handling (MMH) operations in a simulated warehousing environment. 

---
## Introduction of the Experiment and Data:
Data used in this study is driven from an experiment conducted to assess the fatigue accumulation of **upper limb fatigue** in a repetitive overhead load lifting task. The experiment was conducted with four different conditions, with varying: (a) **task weights:** 1.5 and 2.5 kg, and (b) **task paces:** 5, 10, and 15 bpm. The four conditions are based on the following combinations of pace and weights: 

- 5 bpm -- 2.5 kg,   
- 10 bpm -- 2-5 kg,   
- 15 bpm -- 2.5 kg, and   
- 15 bpm -- 1.5 kg 

A total of 17 people participated in this experiment. Each session of the experiment consisted of three 45-minute periods, with two 15-minute breaks in between the work periods. The [Borg 0-10 Ratings of Perceived Exertion (RPE) Scale](https://my.clevelandclinic.org/health/articles/17450-rated-perceived-exertion-rpe-scale) were captured for each subject every 5 minutes of the experiment. A demonstration of the different stages of the experiment task is shown in the below figure.

![Image of workstation](Simulated%20workstation.png)

---
## Data Files: 

In the [**data**](data) folder, there is an [**input**](input) folder which includes the below files:
   1. [Anthropometric_data.RData](data/inputs/Anthropometric_data.RData): In this file the anthropometrics of participants are saved including their: gender, age, height(cm), weight(kg), waist circumference (cm), hip circumference (cm), and body mass index (BMI).
   2. [Experimental_Design.xlsx](data/inputs/Experimental_Design.xlsx): In the sheet "For analysis" of this file the random order of task conditions (combinations of load and pace) are assigned to different participants. This file is later used in the analysis to understand what task condition was performed in each session of the experiment. 
   3. [IMU_Raw.txt](data//inputs/IMU_Raw.txt): This file contains the link to access the large raw IMU data for download.
   4. [corrected_Changepoints.csv](data//inputs/corrected_Changepoints.csv): In this file the changepoints identifying the start and end of the first 45-minute of experiment are provided.

---
