# Final-assignment-Dog Social Traits and Popularity Data Analysis (2013-2020)-R Code #
Many temperament traits were regarded as playing an important role in dog breeds popularity. These traits always show dogs’ different behavioral and social aspects. In this analysis, I will focus on the association between dog breeds popularity rankings and social-related traits, to be more specific, on how friendly different dog breeds are while getting along with family, children, other dogs.

Data are from TidyTuesday (2022-02-01)

breed_traits.csv：https://raw.githubusercontent.com/rfordatascience/tidytuesday/main/data/2022/2022-02-01/breed_traits.csv

breed_rank_all.csv：https://raw.githubusercontent.com/rfordatascience/tidytuesday/main/data/2022/2022-02-01/breed_rank.csv

#Aims of analysis: 

This analysis is focus on exploring and visualizing how the four social-related traits: "Affectionate with Family", "Good with Young Children", "Good with Other Dogs", and "Openness to Strangers” associated with popularity ranking (2020) of dog breed, with examining the stability of popularity rankings across 2013-2020 for some dog breeds. It is noted that, to avoid redundancy, breed rankings refer to the 2020 rankings unless otherwise specified in the rest of analysis.

#Instructions on how to run my code:

Step 1: Access my final assignment Github repository: https://github.com/xw3065-xpw/Final-Assignment-Xinping-Wang

Step 2: Click "Code" in a green little box --> "Download ZIP"

Step 3: Download all files in the ZIP

Step 4: Open the "Final Assignment Xinping Wang.ipynb" with colab ([colab.google](https://colab.google/)) 

Step 5: Please make sure the runtime type is R ***

Step 6: Run from top to bottom OR Click "Run All"

#Dependencies needed:
broom, dplyr, readr, tidyr, ggplot2, stringr
______________________________________________

#Result summary:

** named tables and figures images could be found in the same repository **

-	Trait scores statistics summary:
  
The mean and standard deviation (SD) of the four social-related traits across all breeds were calculated and shown in table 1.
 
This provided the general basic idea for all dog breeds in the dataset. As for the average scores, the score of “Affectionate with Family” trait showed the highest mean, while the score of “Good with Other Dogs” trait showed the lowest mean. As for the stability, “Good with Young Children” showed the greatest variability across breeds (SD = 1.07), while “Affectionate with Family” scores were relatively consistent across breeds (SD = 0.80).

-	Trait scores of top 5 dog breeds:

One column chart (figure 1) was used to show the scores of four traits for the top 5 ranking dog breeds. It shows that the Affectionate with Family score was highest for 3 out of 5 breeds, while Good With Other Dogs score were lowest for 4 out of 5 breeds. And the scores of Good With Young Children and Openness To Strangers were varied across breeds. These indicates that for the most popular 5 breeds, social-related traits scores were not uniformly high. 
 
-	The associations between four trait scores and breeds popularity ranking: 

The scatter plots showed that as breeds popularity increased (=smaller ranking number), Good With Young Children scores and Openness To Strangers scores could be observed as increased obviously, while only minimal increasing of Affectionate with Family scores; and the Good With Other Dogs scores were nearly negligibly changed.

-	Multiple regression model: four traits’ scores combination and popularity rankings:


Generally, the multiple regression model (shown in table 2) did not significant show any of four traits was associated with the breeds’ popularity rankings while controlling the other traits as constant, which suggested that there might be more factors predicting the variation in dog breed popularity rankings other than social-related traits.

-	Comparison between Top 20 breeds and other breeds:

With using t-test and visualizing by boxplots, I tested the difference of four traits’ scores between Top 20 dog breeds and other breeds, the results shown in the figure 3. P-values results were (two decimal left): p=0.74 for Affectionate With Family, p= 0.81 for Good With Other Dogs, p=0.67 for Good With Young Children, and p=0.34 for Openness To Strangers; and also, all confidence intervals include 0. The boxplots (figure 3) also show similar medians and substantial overlaps. All these suggested that the traits’ scores showed relatively small difference between Top 20 breeds and other breeds.
 


-	Comparing traits’ scores of Top 20, bottom 20, and other breeds:

Furthermore, I compared four traits’ scores for top 20 breeds, bottom 20 breeds, and other breeds using ANOVA, and the group differences were visualized by boxplots (shown in figure 4)

P-values results are (two decimal left): p=0.87 for Affectional With Family, p=0.68 for Good With Other Dogs, p=0.41 for Good With Young Children, and p=0.26 for Openness To Strangers; and the boxplots showed many overlaps and the medians were similar for most traits’ scores, so these indicated that four social related traits also showed no significantly differences among these 3 breeds group (top 20, bottom 20, and other breeds).

- History rankings change from 2013-2020 for top 10 and bottom 10 breeds:

Line chart (figure 5) was used here to show how rankings change from 2013 to 2020 for top 10 breeds and bottom 10 breeds. It is shown that these two groups stayed clearly separated rankings during these years. Although the year-to-year fluctuations were slightly larger for top 10 breeds compared with for bottom 10 breeds, the year-to-year rankings were kind of stable overall, suggesting that for top 10 and bottom 10 breeds, the popularity rankings were strongly stable over time without much short-term big shifts.

-	Summary:

Overall, social-related trait selected from this dataset showed no significant association with dog breeds rankings in 2020 and the popularity rankings were stable from 2013-2020 for most and least 10 breeds. For future research, other additional factors could be examined, such as breed size, location, or media exposure, to explore potential associations with breeds popularity. 

