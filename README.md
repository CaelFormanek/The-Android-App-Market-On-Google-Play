# The-Android-App-Market-On-Google-Play

Analysis of Android applications based on multiple variables such as price, storage size, and popularity.
<br />
<br />
  
### Using the data of Android applications to complete the following:

* Determine the average application rating across all applications within the sample
* Show the distribution of application categories
* Examine correlations between the following:
  * Size (MB) and price of applications
  * Price and rating of applications
  * Category and price of applications
* Analyze the popularity of free vs paid applications based on sentiment polarity


### Method for data cleaning and type correction:
* Columns *Installs* and *Price* were classified as objects instead of ints or floats
  * This is due to characters '+', '$', and ',' being present
* Cleaning method:

```
# List of characters to remove
chars_to_remove = ['+', ',', '$']
# List of column names to clean
cols_to_clean = ['Installs', 'Price']

# Loop for each column in cols_to_clean
for col in cols_to_clean:
    # Loop for each char in chars_to_remove
    for char in chars_to_remove:
        # Replace the character with an empty string
        apps[col] = apps[col].apply(lambda x: x.replace(char, ''))
```

### Techniques for analysis and visualizations:
* 


