**1. Waze Dataset:**

<img src="https://github.com/pltnhan/wazecustomerchurn/assets/145864240/d95c908b-f90b-4278-971c-758d9c5bb207" alt="Image Description" width="500">

**2. Distribution of variables:**

<img src="https://github.com/pltnhan/wazecustomerchurn/assets/145864240/322d85ea-f070-45a9-99b8-d587769262b5" alt="Image Description" width="500">

Comments:
- drives: is right-skewed, approximately log-normal, with a median of 48. However, some drivers had over 400 drives in the last month.
- total_sessions: is a right-skewed distribution. The median total number of sessions is 158.7.
- n_days_after_onboarding: is a uniform distribution with values ranging from near-zero to 3,500 (9.5 years).
- driven_km_drives: is a right-skewed distribution with half the users driving under 3,496.5 kilometers.
- activity_days: nearly uniform distribution of ~500 people opening the app on each count of days.


**3. Correlation:**

<img src="https://github.com/pltnhan/wazecustomerchurn/assets/145864240/06397b4b-c7d4-4ed2-bb02-a2f9ecdff6ab" alt="Image Description" width="500">

It appears that:
- Less than 18% of users churned.
- Distance driven per driving day (km_per_driving_day) had a positive correlation with user churn. (The farther a user drove on each driving day, the more likely they were to churn.)
- On the other hand, the number of activity days (activity_days) had a negative correlation with churn. (Users who logged into the app more days in the last month were less likely to churn.)

**4. Decision Tree Model**

<img src="https://github.com/pltnhan/wazecustomerchurn/assets/145864240/b3892ab9-e076-48cc-82a9-ffeb601f021a" alt="Image Description" width="500">

The barplot above shows that in this decision tree model, driving_days, n_day_after_onboarding, total_navigations_fav1, and drives have the highest importance, in that order. These variables are most helpful in predicting the outcome variable, left.

**5. XGBoost Model:**

<img src="https://github.com/pltnhan/wazecustomerchurn/assets/145864240/32f779c5-ae10-4afd-bb0a-b4cd7097a20e" alt="Image Description" width="500">

Based on the results of feature importance from the two models, it can be concluded that driving_days and n_day_after_onboarding mostly affect users' decisions that will churn or retain.

**6. Conclusion:**

<img src="https://github.com/pltnhan/wazecustomerchurn/assets/145864240/16a2db5e-7f6e-4edb-b6db-ca808e12303e" alt="Image Description" width="500">
<img src="https://github.com/pltnhan/wazecustomerchurn/assets/145864240/0c75fa2b-a047-49a6-83fa-7fdd0baf25ff" alt="Image Description" width="500">

!! The more driving days in the last month or the longer time installed the app means that users do not churn.




