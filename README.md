# My_Cheat_cheat

## Searching for p_values less than 0.05
select_cols = p_values.loc[p_values < 0.05]
     

## Update the values in a panda column

df['column_name'] = df['column_name'].apply(lambda x: new_value if condition else x)

mapping_dict = {old_value: new_value}
df['column_name'] = df['column_name'].map(mapping_dict)

df = df.assign(column_name=new_values)

df['column_name'] = df['column_name'].replace(to_replace, new_value)

df.loc[df['column_name'] == some_condition, 'column_name'] = new_value

df['column_name'] = new_values

     

## sum of null values in each column
X_train.isna().sum()

     


## Fill NA with 0
df['pledged'] = df['pledged'].fillna(0)
     

## Searching for a mean of ('days_active value >= 6 AND <= 12 in 'backers_count')
mean_of_week_2_backers_counts = X_train.loc[(X_train['days_active'] >= 6) & (X_train['days_active'] <= 13), 'backers_count'].mean()

     

## List all numeric columns
df = df.select_dtypes(include='number')

     

## Convert y to numeric
df_clean['y'] = pd.get_dummies(df_clean['y'], drop_first = True, dtype=int)
     

## OneHotEncoder
ohe = OneHotEncoder(handle_unknown='ignore', sparse_output=False, dtype='int')
X_train_encoded = pd.DataFrame(data=ohe.fit_transform(X_train), columns=ohe.get_feature_names_out())
X_test_encoded = pd.DataFrame(data=ohe.transform(X_test), columns=ohe.get_feature_names_out())

     

## Fix the columns using the Pandas replace() method
car_data[["num-of-doors","num-of-cylinders"]] = car_data[["num-of-doors","num-of-cylinders"]].replace(str_to_int, regex=False)
car_data

     

## Converts String to Int using a dic
str_to_int = {"eight": 8, 
              "five": 5,
              "four": 4,
              "six": 6,
              "three": 3,
              "twelve": 12,
              "two": 2}
     
