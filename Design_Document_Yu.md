Capstone Project: Book Ads Recommendation System
---


​    

​   
# Overview

Crawl book and magazine ads on Craigslist and classify book Ads into three (or more) categories 

(1) Science/eduction/art/technology

(2) Children's Books

(3) entertainment/Food & Wine/Mystery & Suspense/Romance/Fantasy

Store book Ads into different MySQL tables. When user type in a query/search, search engine can return 

top K similar books in the same category. 



​    

​   

# Main Use Case

1 . Crawler

Crawl books Ads data from Craigslist

2 . Ads Classification

Based on title and keywords to classify the Ads: 

3 . Queries Classification 

Based on title and keywords to classify the queries: 

4 . Ads Engine

Select top K Ads from the same table and return them to user

​    

​     

# High Level Design Diagram

 **Web Crawler**

![webcrawler](https://github.com/yumao1008/capstone/blob/master/webcrawler.PNG)

​    

​   

**Search  Engine**

![searchEngine](https://github.com/yumao1008/capstone/blob/master/searchEngine.PNG)


​    

​   
  



# Detailed Design

**```Crawler:```**

Input: Book Ads data from Craigslist 

Output:  Ads ( AdID, Keywords, Title, Author, Condition, Price, thumbnail, Description, Contact Info)

**```Ads Classification:```**

Input: Keywords, title and description

Output: Category of the book Ads:

(1) science/eduction/art/technology

(2) Children's Books 

(3) Entertainment/Food & Wine/Mystery & Suspense/Romance/Fantasy

**```Data store:```**  

Store the Ads into different MySQL tables based on classification.

 Ad:  AdID, Keywords, Title, Author, Condition, Price, thumbnail, Description, Contact Info

**```Ads Engine:```**

Input: user query

Function: Query understand, query classification, select the same category table from MySQL

Output: Top K relative Ads from the same table and return them to user


​    

​   


# Future Work

Use word2vec and TF-IDF to classify the Ads and queries

Add more categories for book Ads 

Learn how to use spark to improve this project
