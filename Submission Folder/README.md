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


## Interesting Information 

### PLAY NEWS

- There is one Singaporean company attacked
- Government Data is stolen (defence sector information)
- Projects, technical documentations, contracts, agreements 
- Pizza recipe is an interesting one (why would they steal this?)


### Lorenz 

- VersaMax PLC users manual (I am not sure what is this or why they stole it)
- Harrassment Policy, Inspection Policy (why would they steal this?) 
- Cyber Insurance (irony...)
