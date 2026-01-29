# Learning Platform Product Analytics Dashboard (Tableau)

## Project Overview
This project analyzes user behavior across a digital learning platform, focusing on the **product lifecycle from onboarding to engagement, retention, and certification outcomes**.

The goal is to understand:
- How effectively users activate after registration
- How engagement evolves over time
- Where users drop off in learning and exam funnels
- How learning depth and outcomes differ across user segments

This project was developed as part of a **guided Tableau analytics course on Udemy** and extended into a **portfolio-ready product analytics case study** with clear metrics, insights, and recommendations.

---

## Product Questions Answered
- How many registered users become **actively engaged learners**?
- How does **user retention decay** across cohorts over time?
- Are engagement trends driven by **volume or depth** of learning?
- Where do users drop off in the **career track funnel**?
- How effective are exams and certifications as learning outcomes?
- How does behavior differ between **free and paid users**?

---

## Key Product Metrics
- **Activation Rate**: % of registered users who onboard successfully
- **Engaged Users**: active learners over time (daily/monthly trends)
- **Retention**: cohort engagement by registration month and period
- **Learning Depth**: minutes watched per student
- **Outcome Conversion**: exam → certificate funnel progression
- **Course Performance**: minutes watched, completion rate, ratings

---

## Dashboards (Screenshots)

### 1) Overview
![Overview](images/Overview_db.png) 

### 2) Engagement Trends
![Engagement Daily](images/engagement_daily.png)
![Engagement Month](images/engagement_month.png)
![Engagement Year](images/engagement_year.png)

### 3) Cohort Retention
![Cohort Retention](images/cohort_retention.png)

### 4) Exams & Certificates
![Exams & Certificates](images/exams_certificates.png)

### 5) Career Track Funnel
![Funnel](images/funnel.png)

### 6) Learning Behavior
![Learning](images/learning.png)

---

## Key Insights
- Retention shows a **sharp drop after the first engagement period**, suggesting onboarding friction.
- Engagement growth appears driven more by **user volume than depth of learning**.
- A relatively small fraction of enrolled users complete the **full career track funnel**.
- Paid users show **more stable and sustained engagement patterns** vs free users.
- A visible **engagement spike in August** suggests seasonality or campaign-driven behavior.

---

## Product Recommendations
- Improve onboarding nudges during the **first engagement period** to reduce early churn.
- Add progress reminders and clearer learning milestones before exams.
- Target highly engaged free users with **paid conversion offers**.
- Reduce friction in final exam stages to improve certification completion.
- Investigate seasonal engagement spikes to replicate successful campaigns.

---

## Tools & Skills Used
- Tableau (Dashboards, Parameters, Calculated Fields)
- Product Analytics & KPI Design
- Cohort Retention Analysis
- Funnel Analysis
- User Behavior Analysis
- Data Visualization & Stakeholder Reporting

---

## Repository Structure
```text
learning-platform-product-analytics-tableau/
├── README.md
├── data/
├── tableau/
├── images/
└── docs/
    └── data_dictionary.md
