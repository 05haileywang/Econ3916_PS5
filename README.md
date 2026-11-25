# Econ3916_PS5

Recommendation to the Head of Risk

I would not recommend approving the model for production yet. Although the LASSO model had an accuracy of 93.05%, this was the same as the null model that predicted no defaults. At the default threshold of 0.5, the model failed to identify any of the 139 applicants who defaulted.

However, the model still has some value. Its ROC AUC was 0.7071, and its PR AUC was 0.1833, which was higher than the baseline of 0.0695. This suggests that the model can identify differences in default risk, even though its accuracy does not show this.

I found that lowering the threshold to 0.144 reduced the total estimated cost from $2.40 million to $2.05 million, saving approximately $350,916 on the test set. This assumes a 60% loss when an applicant defaults and a 10% cost when a good applicant is declined, including an 8% lost interest margin and a 2% reputational cost.

The calibration results were also fairly good, and Platt scaling slightly improved the Brier score. However, I would want to validate the threshold using separate data before approving the model. If the model continued to reduce costs on new data, I would be more comfortable recommending it for production.
