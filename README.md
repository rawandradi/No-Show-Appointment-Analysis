# No-Show Appointment Analysis

## Introduction
This project analyzes the **No-show Appointments** dataset, which contains information on 100,000 medical appointments in Brazil. The main focus is to understand whether patients attended their scheduled appointments or missed them. The goal of the analysis is to identify key factors that influence patient attendance and provide actionable insights for healthcare providers.

## Dataset Description
The dataset includes the following columns:

| Column Name     | Description                                                                                  |
|-----------------|----------------------------------------------------------------------------------------------|
| PatientId       | Unique identifier for each patient                                                           |
| AppointmentID   | Unique identifier for each appointment                                                       |
| Gender          | Patient's gender (M for male, F for female)                                                  |
| ScheduledDay    | The date and time when the appointment was scheduled                                        |
| AppointmentDay  | The date of the actual appointment                                                          |
| Age             | Age of the patient                                                                           |
| Neighbourhood   | The location of the hospital where the appointment was scheduled                             |
| Scholarship     | Indicates if the patient is enrolled in the Brazilian welfare program Bolsa Família (1 = Yes, 0 = No) |
| Hipertension    | Indicates if the patient has hypertension (1 = Yes, 0 = No)                                 |
| Diabetes        | Indicates if the patient has diabetes (1 = Yes, 0 = No)                                     |
| Alcoholism      | Indicates if the patient has a history of alcoholism (1 = Yes, 0 = No)                       |
| Handcap         | Indicates if the patient has a disability (values range from 0 to 4, mostly 0 or 1)          |
| SMS_received    | Whether the patient received an SMS reminder (1 = Yes, 0 = No)                              |
| No-show         | Indicates whether the patient missed their appointment (`No` = attended, `Yes` = missed)     |

**Note:** The `No-show` column is labeled "No" if the patient attended, and "Yes" if the patient missed the appointment.

## Analysis Questions
The project seeks to answer several key questions:

- Does receiving an SMS reminder reduce or increase the no-show rate?  
- Are patients with hypertension, diabetes, or alcoholism more or less likely to attend their appointments?  
- Are certain age groups more prone to missing appointments?  
- How do factors like gender, disability, and scholarship status affect attendance rates?

## Tools & Techniques
- Data cleaning and preprocessing using Python and Pandas  
- Exploratory Data Analysis (EDA) to identify patterns and correlations  
- Data visualization with Matplotlib and Seaborn to communicate findings  

## Conclusions

### 1. Does receiving an SMS reduce or increase the no-show rate?

- Among patients who **did not receive an SMS**:  
  - 56.56% attended  
  - 11.34% missed their appointments  

- Among patients who **received an SMS**:  
  - 23.25% attended  
  - 8.85% missed their appointments  

**Interpretation:**  
SMS reminders showed a slightly lower no-show rate (8.85%) compared to those without reminders (11.34%), but attendance was also lower among SMS recipients. This suggests SMS reminders may not be as effective as expected and could be influenced by factors like message timing or patient behavior.

---

### 2. Are patients with hypertension, diabetes, or alcoholism more or less likely to attend?

- Patients with **at least one** of these conditions had a show rate of **23.51%**.  
- Patients **without any** had a show rate of **20.08%**.  

**Interpretation:**  
Patients with chronic illnesses such as hypertension and diabetes tend to prioritize appointments more. Alcoholism showed no significant effect on attendance, possibly due to associated social and health challenges.

---

### 3. Are certain age groups more likely to miss appointments?

- Adults aged **18-60 years** had the highest number of no-shows (**12,966 missed appointments**).

**Interpretation:**  
This age group may face challenges balancing work and personal responsibilities, leading to missed appointments.

---

## Analysis Summary
This analysis highlights that SMS reminders alone may not significantly reduce no-shows. Chronic disease patients show higher attendance, while young and middle-aged adults miss appointments most frequently. These insights can help healthcare providers tailor interventions to improve patient attendance.

## How to Use This Project
- Explore the Jupyter Notebook (`no_show_appointments_analysis.ipynb`) for detailed steps and code  
- Review visualizations for a clearer understanding of the data patterns  
- Use findings to develop strategies to reduce missed appointments  

## License
This project is for educational purposes.

---

Feel free to update this README with additional results or visualizations as your project develops!
