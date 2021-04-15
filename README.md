# Cheatsheet for python pandas

### Imports
Numpy is often used together with pandas
```
import numpy as np
import pandas as pd
```

### Create a series of data and indexing the series
```
my_numpy_array = np.random.rand(5) //create list with 5 random numbers
my_series = pd.Series(my_numpy_array, index) // creates a Series
my_series_index = pd.Series(my_numpy_array, index = ["First", "Second", "Third"]) //creates a Series with row indexes 'First', 'Second','Third'

my_series_index["First] //indexing through row name
my_series_index[0] // indexing with index 
```


### Creating a data frame from a numpy array
```
array_2d = np.random.rand(3,2)
array_2d[0,1]
df = pd.DataFrame(array_2d)

df.columns = ["First","Second","Third","Fourth"."Fifth",'Sixth'] //
df = pd.read_csv(CSV_PATH,nrows =2) # only first two rows are read
df = pd.read_csv(CSV_PATH, nrows=5, usecols = ['First','Fifth']) //returns a data frame with only those two columns 'First','Fifth'
```

### Return a unique column (or Series object)
```
artists = df['artists']
unique_artists = pd.unique(artists)
len(pd.unique_artists)
```

### Return a boolean column (or Series object)
```
bool_series = df['artist'] == 'Nirvana' // returns a boolean Series object
bool_series.value_counts() // returns how many True or False values
```

### Indexing with loc and iloc
```
df.loc [Row_Indexer,Column_Indexer]
df.loc [1035,'artist'] ## 

df.loc [df['artist']=='Bacon,Francis', :] 

df.iloc[100:300, [0,1,4]] //row 100 to 300, column 0 1 4 

pd.to_numeric(df['width'], errors='coerce') //makes everything that isn't an number to NaN

df['height'] * df['width']
"""
# create new column with size
df = df.assign(area=area)

df['area'].max()
df['area'].idxmax() // returns a lowlabel of max element
df.loc[df['area'].idxmax(),:] //returns the row with maximum area
```











 
 



