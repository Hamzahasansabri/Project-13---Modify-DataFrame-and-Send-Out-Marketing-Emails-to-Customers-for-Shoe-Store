# Project-13---Modify-DataFrame-and-Send-Out-Marketing-Emails-to-Customers-for-Shoe-Store
import codecademylib3
import pandas as pd
#1
orders = pd.read_csv('shoefly.csv')\
print(orders.head(5))
#2
orders['shoe_source'] = orders.shoe_material.apply(lambda x: \
  'animal' if x == 'leather' else 'vegan')
#3
orders['salutation'] = orders.apply(lambda row: \
  'Dear Mr. ' + row['last_name']
  if row['gender'] == 'male'
  else 'Dear Ms. ' + row['last_name'], axis=1)
