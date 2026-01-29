DATA DICTIONARY – LEARNING PLATFORM PRODUCT ANALYTICS

OVERVIEW
This project uses multiple CSV datasets representing different stages of a digital learning platform’s user journey, from registration and onboarding to engagement, learning activity, exams, certifications, and career-track funnels.

The datasets are structured to support product analytics use cases such as cohort retention analysis, funnel conversion analysis, engagement depth measurement, and outcome evaluation.

All data is anonymized and used for analytical demonstration purposes.

--------------------------------------------------

FILE SUMMARY

student_onboarding.csv
Grain: One row per student
Purpose: Measure user registration and onboarding (activation)

student_engagement.csv
Grain: One row per student per cohort period
Purpose: Cohort retention and engagement tracking

student_learning.csv
Grain: One row per student per day
Purpose: Learning activity and engagement depth analysis

courses_engagement.csv
Grain: One row per course
Purpose: Course-level performance and completion analysis

career_track_funnel.csv
Grain: One row per career track per funnel step
Purpose: Career track conversion funnel analysis

student_exam_attempts.csv
Grain: One row per student per exam attempt
Purpose: Exam participation and success analysis

student_certificates.csv
Grain: One row per certificate issued
Purpose: Certification outcomes analysis

student_buckets_f2p.csv
Grain: One row per engagement bucket
Purpose: Engagement segmentation by free vs paid users

student_buckets_sub_duration.csv
Grain: One row per engagement bucket per subscription duration
Purpose: Engagement vs subscription length analysis

course_ratings.csv
Grain: One row per course rating value
Purpose: Learner satisfaction analysis

--------------------------------------------------

student_onboarding.csv

Columns:
student_id  
Unique identifier for each registered student

registration_date  
Date the student registered on the platform

student_onboarded  
Binary flag indicating onboarding completion  
1 = Onboarded  
0 = Not onboarded

Key Metrics:
- Activation rate
- Registration to onboarding conversion

--------------------------------------------------

student_engagement.csv

Columns:
student_id  
Unique identifier for each student

cohort  
Registration cohort (formatted as YYYY-MM)

period  
Engagement period index since registration  
0 = Registration period  
1, 2, 3... = Subsequent periods

engaged_students  
Binary engagement indicator  
1 = Engaged  
0 = Not engaged

paid  
Subscription status  
1 = Paid user  
0 = Free user

Key Metrics:
- Cohort retention
- Engagement decay
- Paid vs free retention comparison

--------------------------------------------------

student_learning.csv

Columns:
student_id  
Unique identifier for each student

date_utc  
Date of learning activity

minutes_watched  
Total minutes of learning content watched on that date

paid  
Subscription status  
1 = Paid user  
0 = Free user

Key Metrics:
- Daily and monthly engagement trends
- Minutes watched per student
- Learning depth analysis

--------------------------------------------------

courses_engagement.csv

Columns:
course_id  
Unique identifier for each course

course_name  
Course title

total_minutes_watched  
Total minutes watched across all students

minutes_per_student  
Average minutes watched per student

completion_rate  
Course completion rate (value between 0 and 1)

Key Metrics:
- Top and bottom performing courses
- Engagement vs completion comparison

--------------------------------------------------

career_track_funnel.csv

Columns:
track_name  
Career track name (e.g. Data Analyst, Business Analyst)

action  
Funnel step (enrolled, exam_attempted, certified)

students  
Number of students at this funnel stage

Key Metrics:
- Funnel conversion rates
- Drop-off analysis by career track

--------------------------------------------------

student_exam_attempts.csv

Columns:
student_id  
Unique identifier for each student

exam_category  
Exam subject or category

exam_date  
Date of exam attempt

exam_passed  
Binary exam outcome  
1 = Passed  
0 = Failed

Key Metrics:
- Exam attempt trends
- Pass vs fail rates

--------------------------------------------------

student_certificates.csv

Columns:
student_id  
Unique identifier for each student

certificate_type  
Type of certificate (course or career track)

issue_date  
Date certificate was issued

paid  
Subscription status  
1 = Paid user  
0 = Free user

Key Metrics:
- Certificates issued over time
- Paid vs free learning outcomes

--------------------------------------------------

student_buckets_f2p.csv

Columns:
buckets  
Engagement intensity bucket

f2p  
Free-to-paid indicator

students  
Number of students in each bucket

Key Metrics:
- Engagement distribution by payment status

--------------------------------------------------

student_buckets_sub_duration.csv

Columns:
buckets  
Engagement intensity bucket

sub_duration_days  
Subscription duration in days

students  
Number of students in each bucket

Key Metrics:
- Engagement vs subscription duration

--------------------------------------------------

course_ratings.csv

Columns:
course_id  
Unique identifier for each course

rating  
Course rating value (1 to 5)

students  
Number of students who gave the rating

Key Metrics:
- Course rating distribution
- Learner satisfaction patterns

--------------------------------------------------

ASSUMPTIONS AND NOTES

- All date fields are parsed as date data types in Tableau.
- Binary flags use 1 = Yes and 0 = No.
- Engagement is defined by recorded learning activity.
- Cohort period 0 represents the registration period.
- Dataset is structured for analytics demonstration and portfolio use.

--------------------------------------------------

INTENDED USE

This dataset supports demonstration of:
- Product analytics thinking
- Cohort retention analysis
- Funnel conversion analysis
- Engagement depth measurement
- Outcome and performance evaluation
- Stakeholder-ready analytics reporting
