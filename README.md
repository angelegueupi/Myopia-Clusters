# Myopia Clusters

![image](https://user-images.githubusercontent.com/106934375/200454326-1bb7f9f7-2b6f-4f80-8064-76300eafac01.png)


In this project, you’ll apply what you learned about unsupervised learning by fitting data to a model and using clustering algorithms to place data into groups. Then, you’ll create a visualization that shares your findings. 


## Background

You are on the data science team of a medical research company that’s interested in finding better ways to predict myopia, or nearsightedness. Your team has tried—and failed—to improve their classification model when training on the whole dataset. However, they believe that there might be distinct groups of patients that would be better to analyze separately. So, your supervisor has asked you to explore this possibility by using unsupervised learning.

You have been provided with raw data, so you’ll first need to process it to fit the machine learning models. You will use several clustering algorithms to explore whether the patients can be placed into distinct groups. Then, you’ll create a visualization to share your findings with your team and other key stakeholders.

## Instructions

This activity is broken down into four parts: 

* Part 1: Prepare the Data

* Part 2: Apply Dimensionality Reduction 

* Part 3: Perform a Cluster Analysis with K-means

* Part 4: Make a Recommendation 

### Part 1: Prepare the Data
![image](https://user-images.githubusercontent.com/106934375/200479273-e9fc4fbb-e7ba-4195-977c-6ebf1bed36f5.png)


1. Read `myopia.csv` into a Pandas DataFrame.

2. Remove the "MYOPIC" column from the dataset.

    * **Note:** The target column is needed for supervised machine learning, but it will make an unsupervised model biased. After all, the target column is effectively providing clusters already! 

3. Standardize your dataset so that columns that contain larger values do not influence the outcome more than columns with smaller values.

### Part 2: Apply Dimensionality Reduction

1. Perform dimensionality reduction with PCA. How did the number of the features change?
2. 
3. ![image](https://user-images.githubusercontent.com/106934375/200479836-cbd11e9b-5906-4cb7-a1db-7908c2fe7099.png)



  * **Hint:** Rather than specify the number of principal components when you instantiate the PCA model, state the desired **explained variance**. For example, say that a dataset has 100 features. Using `PCA(n_components=0.99)` creates a model that will preserve approximately 99% of the explained variance, whether that means reducing the dataset to 80 principal components or 3. For this assignment, preserve 90% of the explained variance in dimensionality reduction.

2. Further reduce the dataset dimensions with t-SNE and visually inspect the results. To do this, run t-SNE on the principal components, which is the output of the PCA transformation. 

3. Create a scatter plot of the t-SNE output. Are there distinct clusters?
4. ![image](https://user-images.githubusercontent.com/106934375/200479662-1912539e-ae95-4e90-ac63-4d7c54b36377.png)


### Part 3: Perform a Cluster Analysis with K-means

Create an elbow plot to identify the best number of clusters. Make sure to do the following:
![image](https://user-images.githubusercontent.com/106934375/200480184-d21ceaa0-fa61-4fc2-a896-c5e09ff588a2.png)


* Use a `for` loop to determine the inertia for each `k` between 1 through 10. 
* ![image](https://user-images.githubusercontent.com/106934375/200480020-561d0352-48b4-4413-bbbd-63c8ff151385.png)


* If possible, determine where the elbow of the plot is, and at which value of `k` it appears.
* 
* ![image](https://user-images.githubusercontent.com/106934375/200480364-7be6c4a2-c910-4c21-904d-46e18ef064c6.png)

* 

### Part 4: Make a Recommendation

Based on your findings, write up a brief (one or two sentences) recommendation for your supervisor in your Jupyter Notebook. Can the patients be clustered? If so, into how many clusters? 

## Rubric

[Unit 20 Homework Rubric](https://docs.google.com/document/d/1046PZMnFwxcNkyIewuJc_RYhaErY42HoNUKORkh18A4/edit)

- - -

## References

Reduced dataset from [Orinda Longitudinal Study of Myopia conducted by the US National Eye Institute](https://clinicaltrials.gov/ct2/show/NCT00000169)

- - -

© 2022 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.



