## Starbucks Capstone Challenge: Using Starbucks app user data to predict effective offers

## Table of Contents
1. [Installation](#installation)
2. [Introducing a Dataset](#dataset-introduction)
3. [Project Motivation](#project-motivation)
4. [File Descriptions](#files)
5. [Results](#results)
6. [Licensing, Authors, Acknowledgements](#license)

### Installation <a name="installation"></a>
To run this project, the most crucial library required is the Python version of the Anaconda Distribution, which installs all the necessary packages for analysis and model building.

### Introducing a Dataset <a name="dataset-introduction"></a>
The dataset provided here is a simulation of customer behavior on the Starbucks rewards mobile app. Starbucks sends out offers to users of the mobile app every few days, which could either be an advertisement for a drink or an actual offer such as a discount or BOGO. However, not all users receive the same offer, and this presents a challenge that needs to be addressed using this dataset.
### Project Motivation <a name="project-motivation"></a>
This project aims to answer two business questions using the Starbucks rewards mobile app dataset. 
The first question focuses on identifying the key features that impact the effectiveness of an offer on the app. 
The second question examines whether the data on offer characteristics and user demographics can predict whether a user will take up an offer. 

To address these questions, three models were created for each of the three offer types: BOGO, discount, and informational.

### File Descriptions <a name="files"></a>
This repo contains 4 files.There is a notebook available here to showcase work related to the above questions and wrangling process. There are 3 data files used to address the above qustions
1. portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)
2. profile.json - demographic data for each customer
3. transcript.json - records for transactions, offers received, offers viewed, and offers completed

## Results<a name="results"></a>

As a brief summary of my findings:
#### i. Question 1 findings:
The top predictor of offer effectiveness across all three models was found to be membership tenure. The second and third most important features were income and age, with the order varying slightly depending on the offer type. For BOGO and discount offers, the feature importance distribution was relatively equal, while for informational offers, it was more balanced with income being the second most important variable.

#### ii. Question 2 findings:

Using 3 separate models to predict the effectiveness of each offer type proved to be a good decision, with high accuracy for BOGO and discount models (82.87% for BOGO and 87.38% for discount), while slightly lower accuracy for the informational offers (75.23%). Nonetheless, I consider 75% accuracy to be acceptable in a business context since informational offers do not incur any cost.

I am satisfied with the 80% and above accuracy for BOGO and discount models since it would be acceptable to present offers to customers in a business setting. Even if the model makes a few misclassifications, the overall revenue increase may justify the errors.

All of my results would be published [here](<https://scarlettstarbucks.blogspot.com/2023/05/udacity-data-science-nano-degree.html>)

### Licensing, Authors, Acknowledgements, etc.<a name="license"></a>

Data for coding project was provided by Udacity.
