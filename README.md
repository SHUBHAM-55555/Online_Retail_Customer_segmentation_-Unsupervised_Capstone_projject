# Online_Retail_Customer_segmentation_-Unsupervised_Capstone_projject

![image](https://github.com/SHUBHAM-55555/Online_Retail_Customer_segmentation_-Unsupervised_Capstone_projject/assets/135215329/bd0d5d0c-b3c6-45c8-bd4c-59af3a155823)

ABSTRACT: Customer segmentation is the process by which you divide your customers into segments up based on common characteristics – such as demographics or behaviors, so you can market to those customers more effectively.

These customer segmentation groups can also be used to begin discussions of building a marketing persona. we have to divide customers in appropriate segments in this project.

# PROBLEM STATEMENT:

Target Customers for various marketing campaign, provide information about new lunch products by estimating the buying capacity of customers.

The main goal of the project is to:

Creating group of customers having similar properties and targeting various segmentes of customers for various product.

To build a string relationship with customers which are most valuable for the store.

To convert irregular customers into regular by offering good deals.

# Introduction :

Businesses all over the world are growing every day. With the help of technology, they have access to a wider market and hence, a large customer base.

Customer segmentation refers to categorizing customers into different groups with similar characteristics.

Customer segmentation can help businesses focus on each customer group in a different way, in order to maximize benefits for customers as well as the business

This project mainly deals in segmenting customers of an online business store in the UK.

# Data Description

Invoice No : Number uniquely assigned to each transaction. If this code starts with letter 'c', it indat-es a cancellation

StockCode: Product (item) code 5digit integral number uniquely assigned to each distinct product.

Description: Product (item) name. Nominal.

Quantity: The quantities of each product (item) per transaction. Numeric.

Invoice Date: Invoice Date and time. Numeric, the day and time when each transaction was generated.

Unit Price: Unit price. Numeric, Product price per unit in sterling.

CustomerID: Customer number. Nominal, a 5-digit integral number uniquely assigned to each customer.

Country: Country name. Nominal, the name of the country where each customer resides.

# Steps involved

Handling null values – Data contains lots of null values we have to drop all those null values because we don’t have any strategical intuition to handling those values all canceled order values are also dropped in order to perform segmentation appropriately.

Removing Outliers – We removed outliers which are present in quantity and Unit price in order to group customers appropriately.

Feature Extraction – We Extract features from Invoice Date that is day , days name , week , quarter and years which will be very helpful for exploratory data analysis.

Exploratory Data Analysis – We Explore data and built some meaningful insights such as top 10 most selling items .top 10 most potential customers , Sales generated per year , per month , per quarter ,per day name.

RFM Modeling – We extract feature like Recency , Frequency and Monetory and delvelop RFM score with respect to each customer and cluster customer by using these RFM score we group customers in three segments Diamond, Platinum and Gold .

From these we can conclude that Diamond customers are most valuable customers for store after that platinum customers are more important and gold customers are least important as compare two those two.

Implimention K-Means Clustering- We have chosen K_means clustering algorithm to cluster all these customers into 3 segments also we use elbow method , Silhouette score and Dedogram to estimate appropriate value of number of customers.

# Data Cleaning

![image](https://github.com/SHUBHAM-55555/Online_Retail_Customer_segmentation_-Unsupervised_Capstone_projject/assets/135215329/98660521-322d-4c01-b512-4dc748d2a08f)

In this step, the main focus will be to handle the null values and other errors in the data. Columns that are not required will also be dropped.

There are 1454 null values in the description column. There are 4223 different products in the dataset. It is not possible to fill the null values in a strategical manner. Hence, we will drop the null values of the description column.

There are 4372 unique customers in the dataset, there are also 133626 null values in the column. There is no particular method to fill these huge number of points. We cannot use median, mean or mode to fill these values. It is close to impossible that one customer ID can fill 133626 rows. Hence, we will drop the rows containing null values.

Before handling null values data contains 541909 but after dropping null values present in 2 columns which are description and customer id now data contains 406829 records.

Unfortunately 135080 Records have been lost in the process.

As customer ID is a 5 digit number, we can convert it from a float type to an integer type.

# Feature Engineering

Extraction some fetures from Invoice date column such as day , month , year ,day_name ,Quarter ,Hour and week

these column would be very important to generate some meaningfull insights from the data.


# Top 10 most repeatedly sold items And generated highest revenue
WHITE HANGING HEART T-LIGHT HOLDER is the most reapetedly sold items. Hence company should generate stratergies to increase the supply of all those 10 most frequently sold items.

From the above barplot we can clearly seen that top 10 most frequent customer hence company need to maintain good relationship with that customers

From the above bar plot these are the customers who has bought more products also boughts in a mass valume soo those customers are likely to be wholesellers or distributors.

Because that compant should provide more discounts to those customers also provide grete deals in order to make more profit from that customers.

Countries that were sold different items the most

From the above bar plot we can clealy seen that most of the itema has been sold in united kingdom.

Because of that company need to perform marketing campaign in united kingdom in order to expand there business in that company.

From the above bar plot we can see that most items has been sold in the 2011.

From the above bar plot we can clearly seen that the most revenue generate by the company is 8338694 in the year of 2011.

from the above bar plot we can clearly seen that in the month of seprtember,octomber and november most number of fromduct has been sold .

Hence company needs to provide more discounts and offers on there product to generate more revenue in that months.

Now in the months of december,january and february least items are sold therefore company needs to develop strategies and plan to seel more product in that months.

From the barplot we can clearly seen that in the month of novermber ,september and octomeber company made more revenue than other month.

There is a possibility that in those three months more number of special events and feativals are occured beacause of that most number of product are bought by the customer and revenue made by the company is at the most.

In the month of january customer had not bought items frequently but in this bar plot company generate better revenue in these month this could be done because customer bought very expensive items in january month.

from the above bar plot we can clearly seen that in the 'Afternoon' time slot most number of customer like to bought items because of the in this time slot most number of iteams has been sold and company able to generate most of the revenue in that time slot.

hence for that company needs to provide more man power in that time slot to sell items to there customers and provide customer satisfaction also provide some gift vouchers to the customer who bought there products in this time slot to gnerate more revenue in that time slot.

From the above bar plot we can clearly seen that when theweek day is Thuursday , Tuesday and Monday most number of customer prefers to bought items beacause of that most number of sales are generated in those 3 days.

company needs to apply some startegies to generate more and more revenue in these days.

from the above bar plot we can see that as the quarter increases customer prefers to bought more items.

At the end of the year most number of product has been bought by the customers.

But company generate high sales in quarter 3 soo we can estimate that most of the distributor and retailers bought items in huge quatity in the quarter 3 to supply the items to their customer for quarter 4.

From the above statement we can conclude that company recuire to maintain supply in quarter 3 beacause most of the retailers and distributor bought items in quarter 3.

Quarter 3 have to be very important for company to made profit in whole year.

# Co-relation

![image](https://github.com/SHUBHAM-55555/Online_Retail_Customer_segmentation_-Unsupervised_Capstone_projject/assets/135215329/3899c01e-a4c0-4ffc-8cc0-47e5a3f8e2af)


From the above co-relation plot we can see that most of the features are highly co-relation but we require only few features to cluster our customers.

so we can ignore this co-relation matrix.

# RFM MOdeling


![image](https://github.com/SHUBHAM-55555/Online_Retail_Customer_segmentation_-Unsupervised_Capstone_projject/assets/135215329/a604cc6e-e6c5-4eda-91b3-0395cdfcac0c)

# Conclusion

From the above RFM customer segmentation we can cluster customers into 3 categories according to there RFM score. we can build customers segmentation into gold,platinum and diamond class.

![image](https://github.com/SHUBHAM-55555/Online_Retail_Customer_segmentation_-Unsupervised_Capstone_projject/assets/135215329/dc259609-1de1-4c69-b075-3497919ffbd6)

# Diamond Class
The customers which have a RFM score greater than equal to 10 and till the end(in these scenario maximum RFM score is 12) those customers are belog to Diamond Category.

Those customers are the most important customers for the company with respect to sales.

Company should target those customers to sell expensive iteams and aware that customers when company launches new products.

Also company requires to develop marketing campeign add target these customer at first priority.

Those customers and more likely distributors who distribute there products in all the area in there limit so company require to offer these categories of customer a huge discounts when they buy items in huge quantity.

# Platinum class
The customers which have a RFM score greater than equal to 8 and less than equal to 10 those customers are belog to platinum Category.

Those customer are second most important customers to generate sales for the company.

Company should target those customers to expensive products and midium expensive products.

also company should maintain good relationship with these costomers category stay in contact with these customers regularly.

There is a possibility that these customers are retailers who boughts a items in huge amount sp these customer categories are important categories to generate sales for the company.

# Gold Class
The customers which have a RFM score less than 8 all these customer are belong to category gold class.

Most number of customer are belong to these class .

These are the regular customers of company but these customers are not bought items in huge frequency.

Company dont need to target these customer for expensive product.

Also when company launch a marketing campaign. No need to target these customer at the level of Diamond and Platinum class customers.

Applying Clustering Algorithems to segment customers.
Applied Unsupervised learing Algorithems to segment customers.


# Data Preprocessing
Applied stadernd Scalor to Standerdzed all values to perform machine learning algorithem effectively.

Created function to handle zero and negative values to avoid infinite numbers during log tranformation

# VISUALIZING RELATION BETWEEN RECENCY , FREQUENCY AND MONETORY IN 3D AXIS

![image](https://github.com/SHUBHAM-55555/Online_Retail_Customer_segmentation_-Unsupervised_Capstone_projject/assets/135215329/fe96a52c-2d84-4e5a-b3fb-03ff42ad6dbf)

# K-Means Clustering.
k-means clustering is a method of vector quantization, originally from signal processing, that aims to partition n observations into k clusters in which each observation belongs to the cluster with the nearest mean (cluster centers or cluster centroid), serving as a prototype of the cluster.

This results in a partitioning of the data space into Voronoi cells. k-means clustering minimizes within-cluster variances (squared Euclidean distances), but not regular Euclidean distances, which would be the more difficult Weber problem: the mean optimizes squared errors, whereas only the geometric median minimizes Euclidean distances. For instance, better Euclidean solutions can be found using k-medians and k-medoids.

# Conclusion
We appliend customer segmentation by using two technique firstly we group customers into three segment using RFM score by these we can get mmost valuable person and prioterise them accordind to there RFM score. This technique is very helpful for marketing cmpaign and also to traget customers for some of the specific products.

After that we have choosen k_means clastering divide clusteres into three segments K_means clusters works very well in these scenario it does noy affected by the outliers and also it forms clusters in very appropiate way . Also we use some techniques to estimate the perfect number of clusters by using elbow Method and silhouit score.

Also we use Pricipal component analysis to reduce the dimention of the dataset in order to visualise how k_means buildt clusters by visualising these we can conclude that k_means algorithems form a clusters according to the recency , frequency and monetory attributes of the customer it futher divinde it into three group and we label these group as Diamond , Platinum and gold.

Diamond class customers are most valuble customers for the store to target and to offers deals in order to generate more sales from the customer. This type are customers are typically Wholeseller,distributors.

Platinum customers are less valuable that duamond customers . stores management should build srategies for how they convert platinum customers into diamond class customers.

Gold customers are least valuable customers for the store management than Diamond and Platinum class customers.

