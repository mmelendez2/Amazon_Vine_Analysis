# Amazon_Vine_Analysis

## Overview of the analysis

The purpose of this analysis was to pick a dataset from AWS and to use PySpark to perform the ETL process to extract the dataset, transform the data, and connect to an AWS instance, and load the transformed data into pgAdmin. After this, we'll use PySpark to determine if there's any bias toward favorable reviews from Vine members in our dataset

## Results

### How many Vine reviews and non-Vine reviews were there?

#### Vine Reviews (Paid):

![image](https://user-images.githubusercontent.com/89496798/152723290-607c06b3-6a48-404e-9358-ef68b37230ba.png)

#### Non-Vine Reviews (Unpaid):

![image](https://user-images.githubusercontent.com/89496798/152723317-b7a97a73-5826-4189-a320-72d721e1f3c9.png)

### How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

#### Vine Reviews (5-Stars):

![image](https://user-images.githubusercontent.com/89496798/152723409-cc6b2d3c-acf4-4d9e-bb1d-131786f188f8.png)

#### Non-Vine Reviews (5-Stars):

![image](https://user-images.githubusercontent.com/89496798/152723395-3964b463-f969-456e-9583-f4ba5bd8c292.png)

### What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

#### % of Vine Reviews (5-Stars)

![image](https://user-images.githubusercontent.com/89496798/152723454-db149b84-0509-423c-b7a8-177c57773fa6.png)

#### % of Non-Vine Reviews (5-Stars)

![image](https://user-images.githubusercontent.com/89496798/152723476-decd5fba-bed3-40fe-936f-01566fca2fc8.png)

## Summary

It appears there is a significantly higher count of Non-Vine, unpaid, reviews (24040) compared to Vine, paid, reviews (261).
The percentages of unpaid 5-star reviews is also higher than paid 5-star reviews by 4.72%. To strengthen our analysis, we may be able to implement natural language processing on the review_headline or review_body to help determine the legitimacy of the review. To do this, we can begin by classifying the text, extracting the information, and summarize the results. 

More specifically, we can split the review_body into subsets of data to be analyzed by tokenization, take mispelled words and convert them to their original form by normalization, and also find each word or sentence's part of speech by part-of-speech tagging. We can also incorporate stop words filtering to remove common words that don't add real value to what we're looking to analyze, rank the words by importance compared to the rest of the words in the text by using Term Frequency-Inverse Document Frequency (TF-IDF), and finally utilize machine learning model to produce an output.
