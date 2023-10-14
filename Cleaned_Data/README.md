## Combining the data from the different ransomware groups

## Variables and exact formatting

All column name to follow the name below (case-sensitive): <br>

Company_Name: `str` <br>
Date_of_leak: `yyyy-mm-dd`, following Excel sheet formatting <br>
Data_Type: `str` <br>
Company_Address: `str` <br>
Company_Country: `str` <br>
Industry_Type: `str` <br>

<br> All data for Industry Type to be taken from `Linkedin` for coherency.

## Add the dataframe and select the appropriate columns

Each dataframe needs to have a column called `Ransomware_Group` to indicate where the data came from. Below shows the code:

```python
Lorenz = Lorenz[['Company_Name', 'Date_of_leak', 'Data_Type', 'Company_Address', 'Company_Country', 'Industry_Type']]
llist = ["Lorenz"]\*Lorenz.shape[0]
Lorenz['Ransomware_Group'] = llist
```
