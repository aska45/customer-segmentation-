# customer-segmentation-
Overview
This project aims to segment customers based on their transactional behavior and other attributes using machine learning techniques. Customer segmentation is a crucial strategy for businesses to better understand their customer base and tailor marketing efforts accordingly.

Data Understanding

Data Understanding

    Data of Retail Transaction: From 01 December 2010 to 09 December 2011
    Source Data: Online retail dataset by UCI Machine Learning Library

Data Dictionary:

    InvoiceNo: Invoice number uniquely assigned to each transaction.
    StockCode: Product (item) code.
    Description: Product (item) name.
    Quantity: The quantities of each product (item) per transaction.
    InvoiceDate: The day and time when each transaction was generated.
    UnitPrice: Product price per unit in sterling.
    CustomerID: Customer number uniquely assigned to each customer.
    Country: The name of the country where each customer resides

Data Cleaning:

    Quantity Range: The minimum and maximum values for Quantity are 80995, which could represent cancelled or returned orders.
    Negative UnitPrice: There are negative values in UnitPrice, which is uncommon. These transactions could represent cancelled orders by customers or bad-debt incurred by the business.
    Action: We will remove these transactions from the dataset as they do not represent actual sales.

Steps:

    Remove transactions with Quantity equal to 80995.
    Remove transactions with negative UnitPrice.

Explanation:

    Quantity Range: 80995 could indicate cancelled or returned orders, so we'll exclude them.
    Negative UnitPrice: These transactions are unusual and likely represent cancelled orders or bad-debt adjustments, so they will be dropped.



RFM Analysis
Recency Frequency Monetary (RFM) Analysis

    RFM analysis is a method to segment customers based on their purchasing behavior, focusing on three key metrics:

Recency:

    Definition: This metric measures how recently a customer made a purchase.
    In Other Words: It tells us how long it has been since a customer's last purchase.
    Example: If a customer made a purchase yesterday, their recency would be "1 day ago".

Frequency:

    Definition: This metric measures how often a customer makes purchases.
    In Other Words: It tells us how frequently a customer buys from us.
    Example: If a customer made 5 purchases in the last month, their frequency would be "5 purchases".

Monetary:

    Definition: This metric measures the total value of purchases a customer has made.
    In Other Words: It tells us the total amount of money a customer has spent.
    Example: If a customer spent 

    500".

Purpose of RFM:

    The goal of RFM analysis is to segment customers based on these three metrics to:
        Identify high-value customers who spend the most money.
        Understand customer buying patterns and preferences.
        Tailor marketing strategies for different customer segments.

Key Takeaways:

    Recency: How recent was the last purchase?
    Frequency: How often does the customer buy?
    Monetary: How much does the customer spend?

RFM analysis helps businesses target their efforts towards customers who are most likely to make repeat purchases and contribute significantly to revenue.

The last invoice date is 2011–12–09, we will use this date to calculate Recency.

Customer Clusters
Cluster 0 (29% of customers) - "Loyal Customers"

    Characteristics: Haven’t purchased for some time, but used to purchase frequently and spent a lot.
    Description: This cluster represents 29% of customers.
    RFM Profile: R=3, F=2, M=2
    Interpretation: Customers in this cluster used to buy frequently (F=2) and spent a lot, although they haven't made a purchase recently.

Cluster 1 (20% of customers) - "Almost Lost"

    Characteristics: Purchased recently, but do not purchase frequently and do not spend a lot.
    Description: This cluster represents 20% of customers.
    RFM Profile: R=2, F=3, M=3
    Interpretation: These customers purchased recently (R=2) but do not buy frequently (F=3) and do not spend a lot.

Cluster 2 (30% of customers) - "Lost Cheap Customers"

    Characteristics: Last purchase was a long time ago, purchased very few items, and spent little.
    Description: This cluster represents 30% of customers.
    RFM Profile: R=4, F=4, M=4
    Interpretation: Customers in this cluster have not made a purchase for a long time (R=4), purchased very few items (F=4), and spent little (M=4).

Cluster 3 (21% of customers) - "Best Customers"

    Characteristics: Purchase recently, frequent buyers, and spent the most.
    Description: This cluster represents 21% of customers.
    RFM Profile: R=1, F=1, M=1
    Interpretation: These are the "Best Customers" we saw earlier. They purchase recently (R=1), are frequent buyers (F=1), and spent the most (M=1).

For "Best Customers" segment:

    Recommendation: Focus on increasing customer purchases, so it is necessary to form a cross/up-selling strategy.
    Explanation: These customers are already the best in terms of recency, frequency, and monetary value. To maximize their value, focus on offering complementary or upgraded products/services to encourage additional purchases.

For "Loyal Customers" segment:

    Recommendation: Optimize budget and time campaigns to maintain loyalty and increase value.
    Explanation: Loyal customers are valuable assets. To keep them engaged and loyal, tailor marketing campaigns specifically for them. Offer exclusive deals, loyalty rewards, and personalized recommendations based on their past purchases.

For "Almost Lost" segment:

    Recommendation: Focus on activating customers and encouraging repurchases with a reactivation and retention strategy.
    Explanation: Customers in this segment are at risk of churning. To prevent loss, use reactivation strategies such as targeted promotions, reminders of past purchases, and personalized offers to encourage them to come back and make additional purchases.

For "Lost Cheap Customers" segment:

    Recommendation: Focus on reactivating customers with a reactivation strategy.
    Explanation: These customers have already churned, so the main goal is to bring them back. Use reactivation campaigns with attractive offers, incentives, and reminders of the benefits of your products/services to encourage them to return.

