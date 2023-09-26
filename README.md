# Credit Risk Report

## Overview of the Analysis

The purpose of this analysis is to create and evaluate the accuracy of a data model that predicts the credit health/trustworthiness of some potential borrowers from peer-to-peer lending services. The various values included in this data set are the loan size (note: I am not sure what the units some of the columns are in, though it can be assumes USD without a multiplier), their interest rate, the income of the borrower seeking the loan, the debt-to-income ratio, the number of accounts (I am assuming banking accounts based off context but could be wrong), the borrower's total debt, and from this last one, some derogatory mark that labels whether the borrower is in significant debt. This last one in particular seems to put on a mark either at or past 20000 from a quick glance, but for the analysis this merely provides context.

## Results

* Model 1: Original Model:
    * Accuracy = 99%: the overall accuracy of the model
    * Healthy loan (0) precision = 100%: precision is prediction accuracy of this model for a specific category; this particular category has perfect precision
    * High-risk "unhealthy" loan (1) precision = 85%: decent accuracy for this category
    * Healthy loan recall = 99%: recall is how accurate the model is able to identify/capture data points within a specific category
    * Unhealthy loan recall = 91%

* Model 2: Resampled Training Model:
    * Accuracy = 99%
    * Healthy loan precision = 100%
    * Unhealthy loan precision = 84%: marginally lower than the original model
    * Healthy loan recall = 99%
    * Unhealthy loan recall = 99%: moderately higher than the orignal model

## Summary

In terms of finding a trend between the values, the original model seemed to do slightly better, but overall, the resampled model boasted higher accuracy, at least when comparing the values above. To add context, though, most organizations would rather have minor faults in untrustworthy loans than healthy ones as it lowers their overall risk since they line themselves up for less money to lose; the small loss of trust would be a decent enough tradeoff. With this in mind, one would likely still use caution to a model that has less than a 95% accuracy on all fronts, thus the goals of who uses it depends on its overall efficacy.