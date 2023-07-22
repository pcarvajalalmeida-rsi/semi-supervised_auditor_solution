7/21/2020
The models developed up to yesterday where giving nice results.
The best were without imbalanced, and without NAICS.

Features included:

``
    ['Q','maxNumLoc', 
     'eff_tax%_perc_glob', 'eff_tax%_perc_ind', 
     'deduc2income_perc_glob', 'deduc2income_perc_ind',
     '4D_eff_tax%_perc_glob', '4D_deduc2income_perc_glob',
     '4D_eff_tax_perc_ind', '4D_deduc2income_perc_ind',
      'sumsum_gross_perc_glob', 'sumsum_gross_perc_ind']
        
        ```   
The more important feature was the cluster, and I verify that not because of a observation being in a cluster implies the model mark them as 1, which is god to let out the fear of somehow giving information to the model through the labeling.

When I added NAICS, NAICS as a wqhole became important, and took out a big part of the industry clustering importance.
However, the performance of the model did not improve to the one without NAICS.

I will continue analyzing imbalance because cross validation may give different results.

So my plan is to add cross validation, and then continue adding features.

I will keep analyzing:
POSITIVE CHANGE
    1) NAIVE
    2) Cluster-based labeling 
    3) Cluster based-labeling imbalanced
    
I will not include NAICS.
    
In addition, I aim to add features regarding outlier score.

Steps:
1) First put together the three models in a unique notebook
2) Use dictionaries to accumulate Xs[{model_name: X_of_that_model}] before changing to another model. That way all the validations I can do in a loop for features, etc.

I plan to use same features in all this models. Just X may differ.