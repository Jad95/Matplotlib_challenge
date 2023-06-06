# Matplotlib_challenge
In this study, Pymaceuticals, Inc., a pharmaceutical company specializing in anti-cancer medications, screened potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer. The goal of the study was to compare the performance of Pymaceuticals' drug of interest, Capomulin, against other treatment regimens.

The study included 249 mice identified with SCC tumors, who received a range of drug regimens over 45 days. Tumor development was observed and measured periodically. The raw data of the study was provided as separate CSV files, `mouse_metadata.csv` and `study_results.csv`.

As a senior data analyst at Pymaceuticals, I was given access to the complete data from the study and was assigned to generate all the necessary tables and figures required for the technical report.

**Data Preparation**

Using pandas, I loaded the `mouse_metadata.csv` and `study_results.csv` files as separate DataFrames. Then, I merged the two datasets based on the common identifier "Mouse ID" using the pandas `merge()` function. The resulting merged dataset was stored in a variable called `merged_data`.

I then checked the number of unique mice IDs in the merged dataset using the `nunique()` function from pandas, which revealed that there were 249 unique mice IDs in the data.

Next, I checked for any mouse ID with duplicate time points using the `duplicated()` function from pandas, and identified that duplicates exist for some of the Mouse IDs. To remove the data associated with the duplicate Mouse IDs, I used the `drop_duplicates()` function and created a new DataFrame with the cleaned data named `cleaned_data`.

Finally, I sorted the cleaned data by "Timepoint" in ascending order using the `sort_values()` function from pandas and reset the index to a new sequential index using the `reset_index()` function.

**Data Analysis**

Using the cleaned data, I created several tables and figures required for the technical report. For example, I created a summary statistics table using the `groupby()` function from pandas to compute the mean, median, variance, standard deviation, and SEM of the tumor volumes in the cleaned data for each drug regimen.

Furthermore, I generated a bar plot using the pandas `plot()` function to show the total number of measurements taken for each treatment regimen throughout the course of the study.

Additionally, I created a line plot using the same `plot()` function to show the tumor volume changes over Timepoint for a single mouse treated with Capomulin, to describe how Capomulin affects tumor growth.

Using the `scatter()` function from matplotlib and the `linregress()` function from scipy.stats, I also plotted and analyzed the correlation between average tumor volume and mouse weight for the Capomulin treatment.

Determined the quartiles and IQR of the final tumor volume for all mice across all four treatment regimens.

Found any potential outliers using the upper and lower bounds method.

Created a box plot that shows the distribution of the final tumor volume for all mice in each treatment group.

**Conclusion**

In summary, the study on SCC tumor treatments revealed that Capomulin, one of Pymaceuticals' drugs of interest, demonstrated significant improvements in reducing SCC tumor growth compared to other treatments. Capomulin resulted in a relatively small final tumor volume with a low standard deviation, and was efficiently able to reduce tumor growth over time.

The cleaned data was used to generate various charts and tables, giving us a deeper understanding of the data trends and affecting factors of SCC tumor growth. The technical report derived from the analysis of this study will be used by Pymaceuticals to understand and improve their SCC tumor treatment offerings, and additionally by researchers in the medical community to gain insights on the best course of action for fighting SCC.

**Refrences**
- Official Python documentation: https://docs.python.org/3/
- NumPy documentation: https://numpy.org/doc/
- Pandas documentation: https://pandas.pydata.org/docs/
- Matplotlib documentation: https://matplotlib.org/3.3.3/contents.html
- Seaborn documentation: https://seaborn.pydata.org/
- Stack Overflow: https://stackoverflow.com/
- GitHub: https://github.com/

