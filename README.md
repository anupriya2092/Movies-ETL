# Movies-ETL
Perform ETL of the movies data from different sources using Python and Jupyter notebook.

## Purpose and Overview of the project

1. In this project we have performed ETL(Extract Transform Load) for two different datasets from Wikipedia and Kaggle.

2. We have extracted the Wiki and Kaggle data from their respective files ,then transformed the datasets by cleaning them up and merging them together and finally
  loaded the clean dataset to SQL database.

3. The wikipedia data was in JSON format and the Kaggle data was in CSV format that we extracted. The data from both the sources was filtered, parsed, sorted, interpolated,
   pivoted, summarized, aggregated and merged to create a consistent data structure.
   
4. The data extracted from wikipedia was more inconsistent. So we considered each column and using varoius pandas functions and regex , cleaned up the data to get a consistent
   format for each of the columns.

5. Depending on the values in each columns and null values we dropped some of the columns and kept the rest. Finally we merged the wikipedia data and the kaggle data to get
   movies_df dataframe.

6. After merging both the dataframes we dropped one of the columns that was redundant having same data as the other and for the kaggle data that was empty , we filled those values 
   with wikipedia data.

7. Finally  we loaded the merged dataframe to the movies table in SQL database by connecting pandas and SQL through SQLalchemy by craeting a databse engine. We also loaded the
   ratings data in the ratings table in the same database.