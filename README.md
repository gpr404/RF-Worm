This code is intended to take XY coordinates from C. elegans tracks and analyze them using Random Forest to determine what locomotor state they are currently exhibiting. 

There are 4 major parts that should be run in this order AND in the same environment: 

1. Calc Track Features + RF Model
This is the main code, where the xy coordinates from the raw Excel sheets are taken and used to calculate various track features (linear speed, track curvature, etc.) relevant to help the random forest classify the locomotor states.
Each track feature also has a temporal rolling median to give the Random forest a way to make use of temporal information to classify locomotor states better. This code also has the major outputs, such as Excel sheets exports of average speed, average track curvature, overall fraction of time spent in each locomotor state, and average duration of each bout of locomotor state.  
2. Import New Data
Pretty much the same as the Calc Track Features + RF Model, I made this code to make it easier for me to import new strains used throughout the experiment. I will eventually merge these two codes, but no promises.
The final data frame used for the data visualization is **All.GT**
3. LDA Plots
This code is used to both run and plot the results of a Linear Discriminant Analysis of the RF results combined with track features to determine whether locomotor states across various strains are similar or different.
4. Worm Track Plot
This code is used to plot 10 randomly picked worms' tracks to compare the overall look of the path to get a better understanding of how these worms move around the plate 
