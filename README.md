# In this assessment, my task was to load in csv and xlsx files with the option of the user choosing what files to load

1. The first step is to load in pandas and numpy as follows: 
```
import pandas as pd
import numpy as np
```

2. The next step is to produce an input for the user as well as split the file once inserted.

```
file = input("Enter file name: ")
name, ext = file.split(".")
data = ""

```

3. We have to make sure to use try/except in order to make the code professional if the user didn't manage to enter the correct name.

4. If elif and else method has been used in order to pick out the correct file extension like below:

```
try:
  if ext.lower() == "csv":
      data = pd.read_csv(file)
  elif ext.lower() == "xlsx":
    data = pd.read_excel(file)

  else:
    print("Invalid file type")

  print(data.head())

except FileNotFoundError:
    print("File was not found, try again (include folder name)")

except Exception as e:
    print(f"An error occurred: {e}")

```

5. .lower has been used to make sure that the data entry only searches lower capital letters.

6. print(data.head()) has been used to pick out the top 5 rows from the csv or xlsx file.

7. Below is the video of how the program runs:


https://github.com/user-attachments/assets/27cb5a4c-8f33-43cf-ac03-3ec56d5c90f6


