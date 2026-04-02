Amazon Product Selector Tool A Python-based tool for Amazon sellers to find profitable products and monitor prices using the Amazon Product Advertising API. ## Features - Search for products by keyword
Filter by weight (< 100g)
Identify products with 50+ monthly sales
Find lowest-priced variants of the same product
Monitor price changes across sellers
Export results to CSV ## Requirements - Python 3.8+
AWS Account with PA-API credentials
Amazon Associates Account ## Installation bash git clone https://github.com/YOUR_USERNAME/amazon-product-selector.git cd amazon-product-selector pip install -r requirements.txt ## Usage ```python
from selector import AmazonSelector selector = AmazonSelector( access_key=‘YOUR_ACCESS_KEY’, secret_key=‘YOUR_SECRET_KEY’, partner_tag=‘YOUR_PARTNER_TAG’
) # Search for products
results = selector.search(‘keychain’, max_weight=100, min_sales=50) # Find lowest price variants
lowest_price = selector.find_lowest_price(asin=‘B0DQBWWBTG’)
