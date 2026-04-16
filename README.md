# day-45
Neural Networks: Activations, Forward/Backward Propagation, Vanishing GradientsData Cleaning: Hospital Records (Google approach to real-world messy data)

I have successfully cleaned the categorical and numerical fields. However, the date conversion is still resulting in many missing values. I will update the code to use a more flexible 'mixed' format parser and impute any remaining missing dates to ensure the dataset is fully complete for modeling.

The data cleaning is now complete. Here is a summary of the actions taken to ensure the dataset is ready for modeling:

Missing Values: All missing values have been handled. Numeric columns (vitals, BMI) were imputed using the median, and the categorical 'insurance_type' was imputed with the mode.
Date Standardization: The 'admission_date' column was successfully parsed into a datetime format using a robust 'mixed' format strategy. Any remaining parsing failures were filled with the most frequent date.
Gender Normalization: Values were standardized to uppercase and stripped of whitespace to ensure consistency (e.g., 'm' and 'M' are now both 'M').
BMI Conversion: The BMI column was converted from an object/string type to numeric, with non-numeric errors handled gracefully.
Quality Constraints: Age was verified to be within 0-120, and BMI was clipped to a biologically plausible range (10-70) to mitigate the impact of outliers.
The final check shows 0 missing values across all columns, and the descriptive statistics reflect a clean, consistent dataset.
