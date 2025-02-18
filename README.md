import pandas as pd
import matplotlib.pyplot as plt

#Data we're working with
data = {
    'product' : ['Rice', 'Beans', 'Cassava', 'Bourvita','Semovina', 'Biscuits', 'Butter', 'Supermarket', 'Chilly',  'Sacharlie'],
    'sales' : [1300, 1500, 4000, 5000, 4500, 2000, 4000, 5000,1500, 2300]
}

#Create Datafrase
df = pd.DataFrame (data)

#Sorting in ascending order
df_sorted = df.sort_values(by='sales')

#Getting the highest and lowest sale

highest_sale = max(df_sorted['sales'])
lowest_sale = min(df_sorted['sales'])
print('Highest Sale:', highest_sale)
print('Lowest Sale:', lowest_sale)

#Create Color

colors = ['blue', 'red', 'green', 'pink', 'purple', 'indigo', 'brown','grey', 'orange', 'yellow']

#Plot a bar chart
plt.figure(figsize = (10,10))
plt.bar(df_sorted['product'], df_sorted['sales'], color=colors)

#Assign labels
plt.title('A BAR CHART OF PRODUCT AGAINST SALES')
plt.xlabel('Products')
plt.ylabel('Sales')
plt.tight_layout()
plt.show()
