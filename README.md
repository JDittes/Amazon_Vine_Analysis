# Amazon_Vine_Analysis
I wanted to use the skills I had learned with AWS and PySpark to analyze Amazon reviews.

## Overview of the Analysis:
Through a program called "Vine," Amazon lets manufacturers post reviews for their products. Amazon also takes payments from review sites like SellBy to post review. I wanted to compare the percentage of Vine reviews that received Amazon's highest rating (5 stars) with the percentage of non-Vine sources that posted 5-star reviews.

Initially I looked at book reviews. I love to read books, and I like to post reviews of the books I read to Amazon's sister site, ![Goodreads.com](https://www.goodreads.com/user/show/5693583-james-jd-dittes). When I ran the data, however, I found no Vine reviews in the (very large data set). On advice from another student, I switched to the database of reviews for watches. I had already done most of my coding, so it was really just a matter of changing the S3 database link. Everything went fine after that.

As I interacted with the watch-review data. I found the reviews to be very popular. More than 8,400 reviews were posted, and these reviews had received almost 400,000 interactions from shoppers on the site. ![total votes](https://github.com/JDittes/Amazon_Vine_Analysis/blob/main/total_votes.png)

Considering the wide gap in motivation between those who are paying to post reviews on the site, and non-paid reviews, which would reflect the views of users and customers, I wanted to see if there was a wide difference between the percentage of 5-star reviews originating from the two categories.

## Results: 
#### Q: How many Vine reviews and non-Vine reviews were there?
A There were 47 Vine reviews and 8,362 non-Vine reviews of watches.

#### Q: How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
A. There were 15 5-star Vine reviews and 4,332 5-star reviews from non-Vine users.

#### Q: What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
A. Just under 32% of Vine reviews were 5-star, while 52% of non-Vine reviews are 5-star.

Here's the dataframe and the results of the code for Vine users.
![Vine users](https://github.com/JDittes/Amazon_Vine_Analysis/blob/main/vine_reviewers.png)

And here's the dataframe and the results of the code for non-Vine users.
![Non-vine reviewers](https://github.com/JDittes/Amazon_Vine_Analysis/blob/main/nonv_reviewers.png)

## Summary: 
I didn't find positivity bias for Vine reviews--quite the contrary. I found that non-Vine reviewers were 20% more likely to give positive reviews than professional reviewers. One result that might skew this data is the relatively small number of Vine reviews (only 47 out of 8,409 total). 

Still, the bias I would have expected from manufacturers just wasn't there. This may be because professional reviewers may have a broader understanding of competing brands, along with a deep understanding of watch technology which might make them more sensitive to defects in the watches that users may not recognize.

As an additional step, I would groupby the "verified_purchase" column to narrow the non-Vine reviewers to those who had actually purchased the item from Amazon. Sure it's possible that non-purchasing reviewers may have purchased the same watch elsewhere, but there may be other explanations, especially if that population has a higher number of negative reviews than the total sample of non-Vine reviewers.
