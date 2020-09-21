# Stock Analysis with VBA

## Overview of Project
* This is an aggregation of performance data of 12 stock symbols for 2017-2018 using VBA.

### Purpose
* The purpose of this project is to utilize VBA code (macros) to automate aggregating and summarizing stock performance from a large raw data set.

## Results

### Stock Performance: 2017 vs 2018
* Overall, the general trend was that stocks performed much better in 2017 vs 2018. 10 of the 12 stock symbols (tickers) performed better in 2017. The only two symbols which did worse in 2017 were RUN and TERP. 

![alt text](https://github.com/XZandermarsh/stock-analysis/blob/master/Resources/VBA_Challenge_2017_Original_Results.png "2017 Results")

![alt text](https://github.com/XZandermarsh/stock-analysis/blob/master/Resources/VBA_Challenge_2018_Original_Results.png "2018 Results")

* In terms of individual stock performance (return) in 2017, the top symbol was DQ with a 199.4% return, and the bottom symbol was TERP with a -7.2% return (loss). 

* For 2018, the top performing stock was RUN with 83.95% return. The worst performer in 2018 was DQ with a -62.6% return (loss).

### Refactoring & Impact On Program Runtime
* The original code ran in 0.773s for 2017 data and 0.699s for 2018, as shown in the screenshots below:
![alt text](https://github.com/XZandermarsh/stock-analysis/blob/master/Resources/VBA_Challenge_2017_Original_Time.png "2017 Original Runtime")
![alt text](https://github.com/XZandermarsh/stock-analysis/blob/master/Resources/VBA_Challenge_2018_Original_Time.png "2018 Original Runtime")

* After refactoring the program, it ran in ~0.1s for 2017 and 2018, as shown below:

![alt text](https://github.com/XZandermarsh/stock-analysis/blob/master/Resources/VBA_Challenge_2017_Refactored_Time.png "2017 Refactored Runtime")
![alt text](https://github.com/XZandermarsh/stock-analysis/blob/master/Resources/VBA_Challenge_2018_Refactored_Time.png "2018 Refactored Runtime")

* This represents an 88% improvement (reduction) for 2017, and an 85% improvement (reduction) for 2018. 

* The refactoring was performed by changing the way the program flowed through the for loops. In the initial program, the nested for loop calculated the total volume, start price, and end price of a given ticker, then wrote those results to the analysis sheet, then looped into the next ticker. This solution worked, but required the program to switch back and forth between sheets for each ticker, which added time to the program. 


* After refactoring, the program used an array to store all the results, then used a separate for loop to write the results directly from the array. This only required the program to change sheets once, instead of back and forth 12 times. In the first screenshot below, the original code has the both sheet activations inside a for loop. In the refactored version, the activate sheet commands have been placed outside the for loop, so they are only called once each.

* Original Code

![alt text](https://github.com/XZandermarsh/stock-analysis/blob/master/Resources/VBA_Challenge_Original_Code.png "Original Code")

* Refactored Code

![alt text](https://github.com/XZandermarsh/stock-analysis/blob/master/Resources/VBA_Challenge_Refactored_Code.png "Refactored Code")


## Summary
* Refactoring aims to improve the efficiency of a program's internal code while keeping the external functionality intact. The advantage of this activity can be many, but two primary benefits are speed and maintainability. Refactoring often involves improving the flow of a program, cutting out redundancies or finding more efficient and/or elegant methods for accomplishing the same goal. This can result in less resources required by the computer running the program, and may even make the code easier to follow and maintain for the user or others.

* The disadvantages of refactoring are the intoduction of new bugs, and additional time required for less apparent value added. Depending on the complexity of original code, there is not always a benefit to refactoring, as changing the structure of the program could break it in unforseen ways, which could require additional bugs that were not rpesent in the original code. 

* In the case of this program, there was a specific reason for why refactoring might be beneficial. Namely, that the tool could be used in the future for larger data sets. If it was known that the program would only ever be needed for this source data, refactoring may not have been worth the additional time input. However, the use cases for a program or section of code is not always known at the time of creation, so it is beneficial to refactor in preparation for the code's use in the future. Also, there is a measureable improvement in speed which was gained purely from refactoring. Even with the relatively small data set being analyzed, there was a substantial decrease in program run time after refactoring. It is reasonable to assume that the benefit to runtime would become even more substantial if measured between larger data sets, which was the reason given in the challenge.



