# Artificial Fashion Stylist

## Abstract 

Fashion retailers process millions of transactions per day. Because of this, even the smallest increase in average total transaction amounts can have a huge impact on the company's total revenue. Since fashion is more subjective than pairing hamburgers and buns at the grocery store, I plan to create an 'artificial stylist'. This predictive model will learn a customer's style based on past purchasing behavior, while also making suggestions based on current trends found online. In order to generate more revenue, it is key to find complimentary suggestions that the customer may not have previously thought to purchase.

<!--- I think this is good. Probably don't need the last sentence. -->

## Context

The problem with many retailers is how to increase convenience because of low patience and high expectation for instant gratification from many consumers. Most fashion retailers have thousands, if not tens of thousands of products on their website. This can be tedious and overwhelming for customers to find exactly what they're looking for. Search filters can help with this problem, but even with the filters there are often still many options one must sift through. This not only plays into the paradox of choice, but it could also be easy to miss the ideal item when it's being viewed around other vary similar items. Another problem is that sometimes consumers don't actually have a specific thing in mind, they may just have an "idea" of what they want. In the fashion world many consumers rely on personalized help in stores, this is hard to replicate online with just a simple search engine.

<!--- Not sure I understand first sentence. Consider removing. "plays into the paradox of choice" assumes insder knowledge, consider rewrite.  -->

This is important to solve because a consumer may give up and not purchase anything if they are not finding what they need or want. Some customers may not use filters and may lose patience. As I mentioned before, in other cases with filtering, similar items may blend together and the ideal item might be missed. Not getting the right items in front of the right consumers can result in loss of potential sales. This brings down potential total transaction amounts which then leads to less revenue. 


## Proposal 

What are the purchase patterns and behaviors of existing customers? Do we see fashion trends that are location based? What distribution of item categories are people generally purchasing (% active vs casual vs dress, etc)? Are these patterns tied to customer segments? Are customers like snowflakes (no two the same)? Or can we find similar consumers to use purchase suggestions for other similar consumers (customers with similar "taste"")? Are there lower selling items that are part of early trends that we can leverage media/social media to promote (create new demand, fomo)? Is it more effective to show customers items similar to what they have already purchased (or are searching for), or complimentary items that work well with the items they have purchased? In other words, are customers more likely to purchase the same thing multiple times? Or are they more likely to spend more by adding items to go with their existing purchase? Are there clear customer segments that are related to total transaction amount? Is there also a trend of item categories that correlates with different transaction amount totals? Can we find our early innovators, early adopters, early majority, late majority with this information?  

I plan to analyze the existing consumer and transaction information along with the retail item categories and details. 
• Analyze transaction details, compare and group similar consumers (based on purchase behavior)
• Analyze to see if there are regional similarities in purchasing behavior (trends by region)
• Scrape fashion publication sites, social media for trending fashion (clothing and accessory, hashtags and descriptor words)
• Analyze items that were purchased within a "category", match other items that are complimentary within that "line" 
• Analyze transaction details based on transaction amount, adoption lifecycle vs. trends, category distribution groups

Ideally, best case scenario would be to find segments of consumers who have similar purchase behaviors with slightly different items. This could help me to see complimentary items that are potentially being missed by other similar consumers. I would also hope to find not only the most popular selling items, but what are some moderate or low selling items that we can leverage trending to push sales for this *and* that. Instead of this *or* that. My assumption going in is that basics like camis and tshirts will be very popular. I want to find the experiential items that we can upsell to customers who are just looking for those basics. On that note, I am also hoping to find some existing and new trends coming for the season to confirm the 'experiential' purchases that are suggested.

## Conclusion

There is a significant amount of nuance when it comes to personal style. Making a more customized shopping experience attainable for every person could not only increase revenue, but also the overall consumer experience. I will take what could potentially be an overwhelming, time consuming and lonely experience and make it more efficient and personalized. The social value of suggestion in the fashion realm is high. I'd like to replicate this experience online. 

Overall, this idea has potential to create two very simple reinforcing loops. Money invested in the predictive model leads to more good suggestions which leads to more dollars per transaction which leads to more potential money re-invested into the machine learning which leads to more good suggestions and back around again. Branching off of an increase in good suggestions is also an increase in consumer satisfaction which leads to an increase in return visits which leads to an increase in potential sales which leads to an increase in dollars and back around again. Ideally the idea of this model can be generalized, it will just need to be slightly maintained to keep up on some minor feature tweaks dependent on trend shifts.

Potential limitations for this project could be that there is no pattern or connection with any of the transactions. It might also be difficult to gather information from fashion sites and social media to keep up on emerging trends. Other issues could be that the buyers for the organization have not successfully predicted trends and do not have the trending items to place in front of consumers. To go one step further, in order to get ahead of that, another model may be necessary to scrape for trending hashtags and styles online in order for buyers to forecast trends even quicker. 

