# PYTHON_NUMPY_AND_PANDAS
Basic concepts and operations in Python using NumPy and Pandas for data manipulation and analysis.

# 1.Create a numpy array containing the numbers from 1 to 10, and then reshape it to a 2x5 matrix.

import numpy as np

arr = np.arange(1, 11).reshape(2, 5)

print("Array:\n", arr) 

print("Array Shape:\n",arr.shape)

print("Array Dimension:\n",arr.ndim)

![q1](https://github.com/user-attachments/assets/96b35b10-c319-4dcd-964b-65e5057732d2)

# 2. Create a numpy array containing the numbers from 1 to 20, and then extract the elements between the 5th and 15th index.

arr = np.arange(1, 21)

extracted_elements = arr[5:16]

print("Array:\n", arr)

print("Extracted elements (between 5th and 15th index): ", extracted_elements)

![q2](https://github.com/user-attachments/assets/bfbf45aa-6fd3-464c-90c5-7db05809f8a4)

# 3. Create a Pandas series with the following data: {'apples': 3, 'bananas': 2, 'oranges': 1}. Then, add a new item to the series with the key 'pears' and the value 4

import pandas as pd

fruits = pd.Series({'apples': 3, 'bananas': 2, 'oranges': 1})

print("Fruits List:\n",fruits)

fruits["pears"] = 4

print("\n Updated Fruits List:\n",fruits)

![q3](https://github.com/user-attachments/assets/accad617-de8c-4863-93f7-428466cee679)

# 4. Create a dataframe with the following columns: name, age, and gender. The dataframe should have 10 rows of data.

df = pd.DataFrame({
    "name": ["Aadhya", "Arun", "Nithya", "Vivek", "Meera", "Sreeja", "Santhosh", "Anjali", "Ravi", "Anupama"],
    "age": [24, 30, 28, 32, 27, 29, 35, 22, 31, 26],
    "gender": ["Female", "Male", "Female", "Male", "Female", "Female", "Male", "Female", "Male", "Female"]
})

df

![q4](https://github.com/user-attachments/assets/3d06d522-69cd-4dde-a2fa-ef594e3e4a07)

# 5. Add a new column to the data frame created in question 1, called occupation. The values for this column should be Programmer, Manager, and Analyst, corresponding to the rows in the dataframe.

df["occupation"] = ["Programmer", "Manager", "Analyst", "Programmer", "Manager", 
                     "Analyst", "Programmer", "Manager", "Analyst", "Programmer"]

df

![q5](https://github.com/user-attachments/assets/ad34048f-6c39-4a98-9731-99b469c2bd43)

# 6. Select the rows of the dataframe where the age is greater than or equal to 30.

df_selected_age = df[df["age"] >= 30]

print(df_selected_age)

![q6](https://github.com/user-attachments/assets/45437e4a-ff65-4218-975e-825c7e9e9794)

# 7. Convert this dataframe to a csv file and read that csv file, finally display the contents.

df_selected_age.to_csv("selected_age_data.csv", index=False)

print("File saved as selected_age_data.csv \n")

df_from_csv = pd.read_csv("selected_age_data.csv")

print(df_from_csv)

![q7](https://github.com/user-attachments/assets/507d1a79-9fbe-4d55-b9de-b3b2b6ee2492)












