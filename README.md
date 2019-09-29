# amex_credit_card_coupons_prediction 
[Link To Competition](https://datahack.analyticsvidhya.com/contest/amexpert-2019-machine-learning-hackathon/?utm_source=auto-email)
Amex Credit Card Coupon Prediction

Dataset Description
Here is the schema for the different data tables available. The detailed data dictionary is provided next.

[[https://s3-ap-south-1.amazonaws.com/av-blog-media/wp-content/uploads/2019/09/Screenshot-2019-09-28-at-8.58.32-PM.png|alt=first]]

You are provided with the following files in train.zip:

train.csv: Train data containing the coupons offered to the given customers under the 18 campaigns

|Variable |	Definition |
|---------|------------|
| id	| Unique id for coupon customer impression |
| campaign_id |	Unique id for a discount campaign|
| coupon_id |	Unique id for a discount coupon|
| customer_id |	Unique id for a customer |
| redemption_status |	(target) (0 - Coupon not redeemed, 1 - Coupon redeemed) |
 
*campaign_data.csv*: Campaign information for each of the 28 campaigns

| Variable |	Definition |
|----------|-------------|
| campaign_id |	Unique id for a discount campaign |
| campaign_type |	Anonymised Campaign Type (X/Y) |
| start_date |	Campaign Start Date |
| end_date |	Campaign End Date |

*coupon_item_mapping.csv:* Mapping of coupon and items valid for discount under that coupon

| Variable |	Definition |
| coupon_id |	Unique id for a discount coupon (no order)|
| item_id |	Unique id for items for which given coupon is valid (no order) |

*customer_demographics.csv*: Customer demographic information for some customers

|Variable |	Definition |
|---------|------------|
| customer_id |	Unique id for a customer |
| age_range |	Age range of customer family in years |
| marital_status |	Married/Single |
| rented |	0 - not rented accommodation, 1 - rented accommodation |
| family_size |	Number of family members |
| no_of_children |	Number of children in the family |
| income_bracket |	Label Encoded Income Bracket (Higher income corresponds to higher number) |

customer_transaction_data.csv: Transaction data for all customers for duration of campaigns in the train data

| Variable |	Definition |
|----------|-------------|
| date |	Date of Transaction |
| customer_id |	Unique id for a customer |
| item_id |	Unique id for item |
| quantity |	quantity of item bought|
| selling_price |	Sales value of the transaction |
| other_discount | Discount from other sources such as manufacturer coupon/loyalty card |
| coupon_discount |	Discount availed from retailer coupon |

item_data.csv: Item information for each item sold by the retailer

| Variable |	Definition |
|----------|-------------|
| item_id |	Unique id for item |
| brand |	Unique id for item brand |
| brand_type |	Brand Type (local/Established) |
| category |	Item Category |

test.csv: Contains the coupon customer combination for which redemption status is to be predicted

| Variable |	Definition |
|----------|-------------|
| id |	Unique id for coupon customer impression |
| campaign_id |	Unique id for a discount campaign |
| coupon_id |	Unique id for a discount coupon |
| customer_id |	Unique id for a customer |

*Campaign, coupon and customer data for test set is also contained in train.zip 
