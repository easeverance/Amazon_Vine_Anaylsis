# Amazon_Vine_Anaylsis

## Overview
The project team was tasked with analyzing Amazon reviews written by members of the paid Amazon Vine program.  Amazon Vine program is one in which the manufacturers provide product to reviewers in return for published online reviews on Amazon.  The shoe dataset was selected for this analysis.  Pyspark was used to perform the ETL process.  The analysis included a deep data dive to see if there was any sort of bias towards favorable reviews from Vine members.  In other words were positive reviews being given because the reviewer was being paid by the manufactuer. 

## Results
The shoe dataset was used to create a vine DataFrame that contained specific columns to review: review_id, star_rating, helpful_votes, total_votes, vine, and verified_purchase. 

![vine_df](https://user-images.githubusercontent.com/90973718/148703500-cd30fa7a-efe9-4ae6-8112-5fe456c4674c.png)

The total reviews were then broken down by reviews that had helpful reviews that totaled more than 50% of the total reviews. In total there were 27,009 reviews

![useful reviews](https://user-images.githubusercontent.com/90973718/148712275-00a0c3ec-8f25-4794-9736-7909c1b85c09.png)

![useful review count](https://user-images.githubusercontent.com/90973718/148712342-de5692ee-f699-42bc-b8b3-9f2b182d92a5.png)

The dataset was futher broken down between paid reviews and unpaid reviews. There were 22 paid reviews (Vine) and 26,987 unpaid reviews. 
  ### Paid Reviews

![paid count](https://user-images.githubusercontent.com/90973718/148712479-079d75d7-e607-4e47-bc72-01f113e516ca.png)

![paid reviews](https://user-images.githubusercontent.com/90973718/148712488-144ba7e1-24d8-4cd5-86a7-fdc64a37d7af.png)

  ### UnPaid Reviews
  
![unpaid count](https://user-images.githubusercontent.com/90973718/148712609-91d61b76-3ab1-4f65-a96a-df215f8e2e3a.png)

![unpaid reviews](https://user-images.githubusercontent.com/90973718/148712616-6ba4f268-5ea7-46c5-8b5b-3ce4a70274ca.png)

The reviews were then filtered by 5 star reviews. Out of a total of 14,488 5 star reviews 13 were paid (Vine) and 14,475 were unpaid

![total 5 star review](https://user-images.githubusercontent.com/90973718/148713002-92db5236-46ed-4219-8677-e5424b913a89.png)


  ### Paid 5 Star Review Count
  
![5 star review paid](https://user-images.githubusercontent.com/90973718/148713015-acaebe56-776d-46dd-95b5-e11a0693231c.png)

  ### Unpaid 5 Star Review Count

![unpaid 5 star review](https://user-images.githubusercontent.com/90973718/148713059-ccf72249-4076-41fd-96ba-988aeeb05c84.png)


Finally the percentage of 5 star reviews against the total review was examined.  

  ### Paid 5 Star Reviews Percentage
 
![percentage 5 star paid](https://user-images.githubusercontent.com/90973718/148713129-68c8491c-4510-4a8e-b7a0-82a8063b4352.png)

  ### Unpaid 5 Star Review Percentage
  
![percentage 5 star unpaid](https://user-images.githubusercontent.com/90973718/148713174-bc6f9d5c-0a7b-420e-9590-35ae798e610d.png)

## Summary
In conclusion out of the population sample there does not seem to be any positivity bias.  The percentage of 5 star reviews out of the toal paid and unpaid are 59% and 54% repectively, not much variance between the two sample populations.  

An additional analysis could be done with the total population against the total of 5 star reviews, regardless of being paid or unpaid.  As you can see from the analysis below the paid 5 star percentage of 59% and the unpaid 5 star percentage of 54% fall in line with the total 5 star percentage of 54%.  

![percentage 5 star total](https://user-images.githubusercontent.com/90973718/148713422-34e1b5ae-2fd6-47ce-a5c0-61bb71c055dc.png)

 


  



