# Starbucks Capstone Challenge

## Table of Contents
1. [Installation](#installation)
2. [Introducing a Dataset](#dataset-introduction)
3. [Project Motivation](#project-motivation)
4. [File Descriptions](#files)
5. [Results](#results)
6. [Acknowledgements](#license)

### Installation <a name="installation"></a>
This project requires the newest Python version of Anaconda Distribution, which installs all the necessary packages for analysis and model building.

### Introducing a Dataset <a name="dataset-introduction"></a>
This data set contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. Once every few days, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). Not all users receive the same offer, and that is the challenge to solve with this data set.
 
### Project Motivation <a name="project-motivation"></a>
This project aims to answer two business questions using the Starbucks rewards mobile app dataset. 

1. The first question focuses on identifying the key features and their order of importance that impact the effectiveness of an offer on the app. 
2. The second question examines whether the data on offer characteristics and user demographics can predict whether a user will take up an offer. 

To address these questions, three models were created for each of the three offer types: BOGO, discount, and informational. The chosen method was Random Forest Classifier which can apply better for the unbalancing state of data.

### File Descriptions <a name="files"></a>
This repo contains 4 files.There is a notebook available here to showcase work related to the above questions and wrangling process. There are 3 data files used to address the above qustions
1. portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)
2. profile.json - demographic data for each customer
3. transcript.json - records for transactions, offers received, offers viewed, and offers completed

## Results<a name="results"></a>

As a brief summary of my findings:
#### I. Question 1:
Membership tenure was the strongest predictor of offer effectiveness across all three models, followed by income and age, with their importance varying slightly by offer type. In BOGO and discount offers, feature importance was relatively consistent, whereas informational offers showed a more balanced distribution, with income as the second most significant factor.

#### II. Question 2:

Using separate models for each offer type yielded strong results, with high accuracy for BOGO (83.16%) and discount (86.8%) models, and acceptable accuracy for informational offers (76.47%). The lower accuracy is reasonable since informational offers have no associated costs.

Accuracy above 80% for BOGO and discount models is satisfactory for business use, as revenue gains from correctly targeted offers can outweigh occasional misclassifications. Further analysis can be implemented to examine the high rate of ineffective offers for short membership period and successful converion rate peak on range of 500-1,000 days of membership, as well as higher influence of income for range under 50,000 to conversion rate for informational offers.

I published my finding results in the link [here](<https://andynq8.blogspot.com/2024/12/data-science-starbucks-capstone.html>)

### Acknowledgements, etc.<a name="license"></a>

Data for implementing this project was provided by Udacity.
