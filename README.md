# Amazon Prime - New Subscriber Overview
## The goal of this project is to investigate new Amazon Prime subscribers to surface recommendations on efficient customer acquisition strategies across geographies and product selection available via Prime to improve customer satisfaction.

Founded in 1994, Amazon is a global e-commerce and technology company serving millions of customers across the world. It offers a vast range of products, digital streaming, cloud computing, and artificial intelligence services, making it one of the largest online retailers globally. Their customers can sign up for Amazon Prime subscription plan available on a monthly and annual basis.

Now that they’ve hired a new data team and are strategizing their approach to new customer acquisition and customer retention, the company would like to build more understanding of customer demographics and products purchased via Prime. Given highly saturated US market, Amazon would like to learn how to effectively allocate their resources in terms of new customer acqusition efforts and improve customer satisfaction on products purchased via Prime. The company has 2 primary objectives: 1) learn how to target subscriber acquisition to maximize Prime revenue, and 2) to raise customer satisfaction on products purchased to prevent churn.

The Jupyter Notebook used to inspect and clean the data for this analysis can be found here [link].

The SQL queries regarding various business questions can be found here [link](https://github.com/karolinabajorek/Amazon-Project/blob/main/amazon_prime.sql).

An interactive Tableau dashboard used to report and explore sales trends can be found here [link](https://public.tableau.com/app/profile/karolina.bajorek/viz/AmazonPrimeAnalysis_17385937614220/Dashboard32).

## Dataset Structure
The dataset consisted of 3 tables, including information about subscribers, subscription prices and geographical regions.

<img width="639" alt="Screenshot 2025-02-04 at 06 11 59" src="https://github.com/user-attachments/assets/bc14294f-a0a0-4bba-ad7c-09378325c1ca" />


## Insights Summary
#### In order to evaluate lane performance, I focused on the following key metrics:
* **Yield:** The USD revenue per 1kg of charged weight.  
* **Charged-to-Actual Weight Ratio:** The ratio shows how much weight was charged per 1 kg of actual weight.  
* **Interquartile Range:** The difference between the 3rd and 1st quartiles of weekly weight charged measures the data's dispersion.  
* **% Dependence on Priority Services:** The percentage of weight charged shipped via FedEx priority services.  
#### Yield:
* Across customers, Customer C brought the most revenue per 1kg of weight charged on Europe-Americas shipments (4.86 USD/kg) while shipping the smallest volume on the route among  all customers (332,134 kg).  
* Customer C brought the highest yield on International Priority Freight (5.38 USD/kg) and International Priority Parcel shipping (3.43 USD/kg) for the Europe-Americas lane.  
* Considering Europe-Americas lane 1) for Customer A: economy parcel shipping is 3x pricier than priority service, and freight services are the same price. 2) For Customer B: economy freight shipping is 2.5x pricier than priority service, and parcel priority is cheaper than economy. 3) For Customer C: freight services are almost identically priced.  
#### Charged-to-Actual Weight Ratio:
* Across customers, Customer A had by far the highest overall charged-to-actual weight ratio(1.66) on Europe-Americas shipments.
* Customer A’s trend is consistent - having the highest charged-to-actual weight ratio across 17 of 18 analyzed weeks.
#### Interquartile Range:
* Across customers, Customer B had the highest Interquartile Range for weight charged on Europe-Americas shipments (19 142 kg).
* Within the distribution of average shipment size, Customer B also displays the highest dispersion of values (IQR 354 kg).
#### % Dependence on Priority Services:
* All the customers present staggering dependence on priority services for their Europe-Americas shipments - Customer A was almost entirely dependent on priority (99.41%).
* Customer A is highly dependent on priority services for its Europe-Americas shipments. However, it is least dependent on the Europe-Americas lane of all the customers (56.02%).
## Recommendations:
* **Prioritize priority shipments for Customer C** in the Europe-Americas lane during peak times. These have the highest yield on priority shipments among customers, for parcel and freight shipments, and the lowest volatility in weekly weight charged.
* **Fix evident pricing errors for all Customers A, B, and C**, where priority pricing is cheaper than the economy or of equal price as the economy, which encourages choosing priority over economy services.
* **Incentivize dimensional weight reduction for Customer A:** 1) Introduce tiered discounts for shipments that meet specific dimensional weight efficiency thresholds. 2) Offer incentives for better packaging practices, such as rebates for shipments where the actual weight is closer to the charged weight.
* **Introduce a contractual agreement to ensure consistent weekly volumes or caps on weekly volumes** on Europe-Americas priority shipments, especially for highly volatile and voluminous Customer B and, inconsistent Customer A, reducing strain during peak times.
* **Negotiate a flexible shipping agreement** - where Customers B and A allow shifting some priority shipments to next-day flights during peak times.  
* **Promote and offer price incentives on alternate lanes where feasible for economy shipments to encourage redistribution of shipments.** This could free up capacity for priority products in the Europe-Americas lane.
