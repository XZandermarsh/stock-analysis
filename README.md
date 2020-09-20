# Kickstarting with Excel

## Overview of Project
* This is an analysis of Kickstarter campaign data.

### Purpose
* The purpose of this project is to analyze various attributes of Kickstarter campaigns to understand if there are any indicators of success/failure.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
* For this portion of the analysis, the launch date and end date for each campaign had to be converted into a readable data format via a formula in Excel. The Category/Subcategory field also had to be split into two separate fields for proper grouping using Excel's "Text to Columns" feature

* After converting the dates into the correct format, a Pivot Table was used to aggregate the campaigns into the month in which the campaign was created. The intent was to compare the number of successful and failed campaigns by the month they launched in and observe any trends. 

### Challenges and Difficulties Encountered

* There were no challenges faced in this particular analysis, but one potential challenge could have been if the data had large spikes in certain months but not an overall trend. This could have occured if the data set was smaller (such as only having data for one year). This could lead to uncertainty about whether a particular month is best/worst to launch a campaign because one would not expect high/low months to be adjacent. 

* For example: the chart below would be the result if only 2011-2012 data were used, where April and November appear to be the best months, which does not match the overall trend outlined in the results section. There were also no failures in these two years, so the success rate (%) would actually appear to be 100%.

![alt text](https://github.com/XZandermarsh/Kickstarter_Challenge/blob/master/resources/Results%20by%20Start%20Month%202011%202012.png "Theater Outcomes vs Launch Date (2011-2012)")

### Analysis of Outcomes Based on Goals

* For this portion of the analysis, a new sheet was created with some goal ranges and formula fields, such as Number Successful, Number Failed, and Number Cancelled, as well as the percentage for each result as a part of the total projects within that goal range.

* The next step was to use the COUNTIF function to count the number of campaigns with each result within each goal range. These results were then converted into percentages for ease of comparison between the ranges.

* Finally, we were asked to create a line chart with percentage of success and failure based on goal.

### Challenges and Difficulties Encountered

* Challenges with this portion of analysis include using the structure and syntax of the COUNTIF function correctly. After the formula was filled out as instructed, I realized that the quantities did not match the example given in the instructions. After investigating, the formulas needed to use the ">=" and "<=" signs, not ">" and "<". After correcting this error, the data and chart matched the instructions.

## Results

### Outcomes Based on Launch Date
* The data suggests that May has the highest number of successful Kickstarter campaigns, with June being a close second.
* December had by far the lowest number of successful campaigns.
* This trend is present for the overall data, and also within the Theater parent category, as you can see by the two charts below:

![alt text](https://github.com/XZandermarsh/Kickstarter_Challenge/blob/master/resources/All_Outcomes_vs_Launch_2.png "All Outcomes vs Launch Date")
![alt text](https://github.com/XZandermarsh/Kickstarter_Challenge/blob/master/resources/Theater_Outcomes_vs_Launch.png "Theater Outcomes vs Launch Date")


### Outcomes Based on Goals

* The data suggests that there is not a strong correlation between the initial goal and the overall success of the campaign. As seen by the chart below, there appears to be a slight negative correlation between goal and success rate for campaigns under $25k, but there is another peak for campaigns in the $35k to $45k goal range. However, upon closer inspection, there are far fewer data points available as the goal increases. For example, there are 1005 total projects with goals less than $25k, but there are only 42 projects with goals at $25k or greater. This means that the succes rate seen at the $35k to $45k range may have a much larger margin for error than the lower goal ranges. More data in the higher ranges would be needed to fully draw a conclusion on this question.

![alt text](https://github.com/XZandermarsh/Kickstarter_Challenge/blob/master/resources/Outcomes_vs_Goals.png "Outcomes vs Goals")

* The chart below shows the total projects as a function of the goal. As mentioned above, the number of campaigns tend to decrease above the $5000 mark, to the point where we cannot draw conclusions from the success rate as the sample size decreases. 

![alt text](https://github.com/XZandermarsh/Kickstarter_Challenge/blob/master/resources/Total_Projects_vs_Goal.png "Total Projects vs Goals")

