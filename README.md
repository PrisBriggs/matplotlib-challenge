# matplotlib-challenge

Georgia Tech Data Analytics BootCamp - February 2023

Homework Module 05 - Matplotlib Challenge
By Priscila Menezes Briggs

In this challenge, as a senior data analyst who just joined Pymaceuticals, Inc. -- a new pharmaceutical company that specializes in anti-cancer medications and recently began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer --, my task is to generate all of the tables and figures and to write a top-level summary of the results from their most recent animal study. In this clinical study, 249 mice who were identified with SCC tumors received treatment with a range of drug regimens. Over the course of 45 days, tumor development was observed and measured. To perform this analysis, I was given access to the complete data from this study. The purpose of this study was to compare the performance of Pymaceuticals’ drug of interest, Capomulin, against the other treatment regimens.

For this challenge, a script on Jupyter Notebook using Python with Matplotlib and Pandas packages was developed to calculate the desired values and analyze the study results.Two datasets Mouse_metadata.csv and Study_results.csv had been provided as resources, which were composed of the following columns with data:

Mouse_metadata.csv: Mouse ID, Drug Regimen, Sex, Age_months, Weight (g).
Study_results.csv: Mouse ID, Timepoint, Tumor Volume (mm3), Metastatic sites. 

The resource data was cleaned up to remove duplicates. Results for each block below have been calculated and different types of plots were created for better visualization and understanding of the results. The topics under analysis were:

- Summary Statistics: the mean, median, variance, standard deviation and SEM of the tumor volume for each drug regimen were calculated. 
- Bar and Pie Charts: bar plots were created using two different methods to show the total number of time points for all mice tested for each drug regimen. The distribution of female versus male mice was presented with a pie plot through the same previous two methods. 
- Quartiles, Outliers and Boxplots: The final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin, was calculated, as well as the quartiles and IQR, and the existence of any potential outliers was verified across all four treatment regimens. 
- Line and Scatter Plots: A line plot of tumor volume vs. time point was generated for a random mouse treated with Capomulin. Besides, a scatter plot of average tumor volume vs. mouse weight for the Capomulin regimen was generated. 
- Correlation and Regression: It was performed the calculation of the correlation coefficient and linear regression model for mouse weight and average tumor volume for the Capomulin regimen. The scatter plot previously created was used to illustrate the model. 
- Analysis: A summary of the analysis of some of the results found in this study was made. 

Some of the conclusions from this analysis are described below and are also written in the notebook:

Topic: Data clean-up
* As a whole, the resource datasets are likely to be reliable due to there being originally only one duplicate mouse ID and, in the group of four most successful drugs, only one outlier data point was found, relative to volume of the tumor (seen in the box plots).

Topic: Summary Statistics
* The five drugs that resulted in the smallest average tumor volume according to the study were: Capomulin, Ceftamin, Infubinol, Ramicane and Propriva. Capomulin and Ramicane were by far the best drugs in terms of mean tumor volume. Propriva, however, despite having a smaller mean tumor volume than Ceftamin and Infubinol, had the highest tumor volume variance, standard deviation and standard error of the mean compared to all other four drugs. This indicates that its results are more likely to show an inaccurate representation of true average tumor values. Therefore, the drugs with the best results in combating tumor development were Capomulin, Ceftamin, Infubinol and Ramicane. The corresponding values that led to this analysis are shown in the summary_stats_df data frame.

Topic: Bar and Pie Charts
* According to tumor treatment studies(1), “since mouse dropout may reflect moribund outcomes due to drug toxicity or excessive tumor burden due to lack of efficacy, the remaining sample size at each time point” is measured. This indicates that drugs with more mice surviving to the last time point are likely to be more effective in reducing tumor growth. On the face of it, the bar plots show that Capomulin and Ramicane had a noticeably higher amount of time points measured, with Capomulin having 55% more time points measured than Propriva, the drug with the fewest time points measured. ((1) see References)
* Studies say that “there are significant differences in how male and female animals and cells experience disease and react to drugs, in part due to intrinsic hormonal and genetic differences.”(2) Pie charts show the number of males in this current study is 2% greater than the number of female mice, which indicates that the mouse population was nearly evenly distributed by sex. ((2) see References)

Topic: Line and Scatter Plots
* As an example, the line plot shows the evolution of tumor volume over the period studied for a mouse treated with Capomulin. It can be seen that this drug reduced tumor volume by about 9% for this mouse.

Topic: Correlation and Regression
* Scatter plots show a strong positive correlation (=0.84) between mouse weight and average tumor volume, ie, the heavier the mouse, the greater the probability of that mouse developing a tumor with greater volume.

The file main.ipynb inside the Pymaceuticals folder contains the script for this analysis. A starter code previously provided was used as reference for the calculations. 

The script and written analysis for this challenge are found in the GitHub's repository on:
https://github.com/PrisBriggs/matplotlib-challenge

The references to build this script were the activities and lessons given in class in addition to the websites below. 

All webpages visited in February/2023.

References:

Dropping rows from dataframe
https://stackoverflow.com/questions/28679930/how-to-drop-rows-from-pandas-data-frame-that-contains-a-particular-string-in-a-p

Aggregate method in Pandas
https://cmdlinetips.com/2020/05/fun-with-pandas-groupby-aggregate-multi-index-and-unstack/

Style formatting of dataframe
https://stackoverflow.com/questions/71575511/multiindex-column-names-and-pandas-styler-alignment

Sorting values from dataframe
https://stackoverflow.com/questions/55423048/how-to-sort-values-in-descending-order-bar-plot-from-pandas-dataframe

Adding axes labels to pandas plot
https://stackoverflow.com/questions/21487329/add-x-and-y-labels-to-a-pandas-plot#:~:text=You%20can%20set%20the%20labels%20on%20that%20object.&text=Or%2C%20more%20succinctly%3A%20ax.,name%2C%20if%20it%20has%20one.

Formatting plots
https://pandas.pydata.org/pandas-docs/version/1.1/user_guide/visualization.html#visualization-formatting
https://matplotlib.org/stable/gallery/color/named_colors.html
https://stackoverflow.com/questions/6390393/matplotlib-make-tick-labels-font-size-smaller
https://stackoverflow.com/questions/72338356/how-to-show-values-in-pandas-pie-chart
https://stackoverflow.com/questions/68909283/how-to-customize-pandas-pie-plot-with-labels-and-legend
https://stackoverflow.com/questions/7082345/how-to-set-the-labels-size-on-a-pie-chart-in-python
https://stackoverflow.com/questions/46226032/how-to-change-the-linestyle-of-whiskers-in-pandas-boxplots
https://matplotlib.org/stable/gallery/spines/spines.html#sphx-glr-gallery-spines-spines-py
https://stackoverflow.com/questions/32443015/remove-edgewidth-of-matplotlib-boxplot-flier
https://towardsdatascience.com/change-tick-frequency-matplotlib-axis-6af2c6bce1ea
https://matplotlib.org/2.1.2/api/_as_gen/matplotlib.axes.Axes.tick_params.html#matplotlib.axes.Axes.tick_params

Bar plots
https://datavizpyr.com/bar-plots-with-matplotlib-in-python/

Indexing of dataframe
https://stackoverflow.com/questions/22356881/using-a-pandas-dataframe-index-as-values-for-x-axis-in-matplotlib-plot

Pie plots
https://www.python-graph-gallery.com/140-basic-pieplot-with-panda
https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.plot.pie.html

Boxplots
https://matplotlib.org/stable/gallery/statistics/boxplot_demo.html
https://matplotlib.org/stable/gallery/statistics/boxplot_vs_violin.html#sphx-glr-gallery-statistics-boxplot-vs-violin-py
https://towardsdatascience.com/create-and-customize-boxplots-with-pythons-matplotlib-to-get-lots-of-insights-from-your-data-d561c9883643

References used in the written analysis:
(1) https://www.nature.com/articles/s41598-021-87470-x
(2) https://www.understandinganimalresearch.org.uk/news/why-we-need-female-mice-in-drug-trials#:~:text=Males%20and%20females%20don't,can%20be%20missed%20or%20misinterpreted.