# **Daltix Data Analyst Challenge**
In this challenge you will explore a subset of data that mirrors (in a simplified manner) some of the data we work with at Daltix.  
The goal of this challenge is to explore the data we provide and share all insights you find relevant in a business-friendly manner.  
This challenge is __hard__! You should aim to complete it within 36h (1,5 day) and send it back to us.  
  
Some tips:
* Imagine you are presenting these to both technical and non-technical members of your company. 
* Take into consideration that the code you produce should be readable and reusable by a colleague in the future.


## Table of Contents
1. [How to send us back the challenge](#how-to-send-us-back-the-challenge)
2. [Dataset Description](#dataset-description)
  
# How to send us back the challenge

## Instructions
1. Fork this repository to your personal git account
2. Complete the challenge in the `da_challenge.ipynb`
    * Make sure you save the notebook with outputs, as we might not run it locally!
    * No need to send us back the dataset, unless you somehow altered the files; if you choose to do so, make sure to include a note explaining what and why you did it.
3. Make sure your repository is public before sending it back to us :thumbsup:

# Dataset Description
Each CSV file included in this challenge is a subset of a table in our database.

### **product.csv** 
**Source:** https://daltix-public-interviews.s3-eu-west-1.amazonaws.com/data-analyst-challenge/product.csv

Contains attributes pertaining to products we scraped from webstores.
* __daltix_id__: The id that uniquely defines a product within a shop, in a specific country. It's an hash of (product_id, shop, country)
* __product_id__: The shop's own internal code for a product
* __article_nr__: The shop's own article number for a product
* __shop__: The shop to which the product belongs to
* __country__: The country code of the shop that contains the product; note that one shop can be in more than one country!
* __name__: The name of the product
* __brand__: The brand of the product
* __eans__: The EAN code of the product. This code is uniquely defined across all webstores and identifies a product. For more details consult -> [Wikipedia](https://en.wikipedia.org/wiki/International_Article_Number); note that some products can have more than one EAN code!
* __contents__: A dictionary that contains the following keys: 
    * _approximate_content_: indicates whether the content is exact or approximate (_e.g. "200g" vs "±200g"_)
    * _content_value: the numeric value of the contents (_e.g. "200"_)
    * _content_unit_: the unit of the contents (_e.g. "g"_)
     
     
### **price.csv**
**Source:** https://daltix-public-interviews.s3-eu-west-1.amazonaws.com/data-analyst-challenge/price.csv

This table contains the prices for the assortment in **product.csv** over a set period of time.
* __daltix_id__: The id that uniquely defines a product within a shop, in a specific country. It's an hash of (product_id, shop, country)
* __product_id__: The shop's own internal code for a product
* __shop__: The shop to which the product belongs to
* __country__: The country code of the shop that contains the product; note that one shop can be in more than one country!
* __location__: The physical location of the store; these are usually municipalities and prices can change in the same shop on different locations
* __price__: The price of the product
* __unit_std__: The sale unit for that price
* __date__: The date when the price was valid
    
    
### **category.csv** 
**Source:** https://daltix-public-interviews.s3-eu-west-1.amazonaws.com/data-analyst-challenge/category.csv

This table contains the category tree of our products.
* __daltix_id__: The id that uniquely defines a product within a shop, in a specific country. It's an hash of (product_id, shop, country)
* __shop__: The shop to which the product belongs to
* __country__: The country code of the shop that contains the product; note that one shop can be in more than one country!
* __categories__: The category tree of the product, ordered hierarchically from largest to smallest category (_e.g. [main_category, sub_category_1, sub_category_2, ...]_); note that some products can belong to different categories
    
    
### **promo.csv** 
**Source:** https://daltix-public-interviews.s3-eu-west-1.amazonaws.com/data-analyst-challenge/promo.csv

This table contains the promotional information of our products.
* __daltix_id__: The id that uniquely defines a product within a shop, in a specific country. It's an hash of (product_id, shop, country)
* __shop__: The shop to which the product belongs to
* __country__: The country code of the shop that contains the product; note that one shop can be in more than one country!
* __location__: The physical location of the store; these are usually municipalities and prices can change in the same shop on different locations
* __promo_type__: The conditions on the promotion
* __dlevel__: The discount level of the promotion
* __date__: The date when the promotion was valid
  
_____
  
With that said, **good luck**! 😀

> The Daltix Team