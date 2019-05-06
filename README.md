Text classification: 

Text classification is one of the most important tasks in Natural Language Processing. It is the process of classifying 
text strings or documents into different categories, depending upon the contents of the strings. Text classification has a variety of 
applications, such as detecting user sentiment from a tweet, classifying an email as spam or ham, classifying blog posts into different 
categories, automatic tagging of customer queries, and so on. Different ML classification algorithms like Naive Bayes, SVM and Neural 
Networks can be used for text classification. 

 

About Reuters-21578 dataset: 

The dataset consists of a README file, collection of 22 data files, an SGML DTD file describing the data file format, 
and six files describing the categories used to index the data. All files are available uncompressed, and in addition a single 
gzipped UNIX tar archive of the entire distribution is available as reuters21578.tar.gz. 

The texts can be classified into 5 main categories: TOPICS, EXCHANGES, ORGS, PEOPLE, and PLACES. 

There are sub categories for each main category. But most of the sub-categories have very few documents. So while developing our 
model we will take into account only the top 20 categories based on the total number of documents belonging to them. 

 

Approach: 

1. Using the five category text files derived a data frame consisting of sub category, main category of all possible combinations. 
Initialised the news lines as 0. 

2. Read the 22 SGML files using Beautiful Soup. 

3. Update the newsline column (in the data frame created in step1) with the actual frequency of documents belonging to each category. 

4. Identify the top 20 categories based on the number of documents belonging to each category. 

5. Create a vector showing the categories that each document can belong to. This will be the target variable. 

6. The text body will be used as the X variable. 

7. First clean the document body(X variable) by removing special characters, stop words, lemmatizing. 

8. Prepare the text data by tokenizing so that it can be fed to the RNN model. Define maximum vocabulary size and fit the X variable. 

9. Build the model using gated RNN. 

10. Save the model for future predictions. 
