We import the csv file,we use head to see the first 5 rows

<img width="1495" height="754" alt="Screenshot 2025-11-14 210157" src="https://github.com/user-attachments/assets/7f74953d-207d-4cdb-9ef1-30a547145a3f" />




We use shape to see what shape it is

<img width="1500" height="210" alt="Screenshot 2025-11-14 210221" src="https://github.com/user-attachments/assets/ffe2e396-e150-4cd0-8988-ea5ab033b31f" />




To check the missing values we use usa_hours.isna().sum()

<img width="450" height="670" alt="Screenshot 2025-11-14 214052" src="https://github.com/user-attachments/assets/401988a2-4ea8-4a51-a330-eba53e1a4464" />
<img width="363" height="231" alt="Screenshot 2025-11-14 214304" src="https://github.com/user-attachments/assets/929b6361-be52-4915-a75d-106610363bf4" />



To drop and replace the Time period we concat both datasets into one which is the name of combined,we are going to use : combined['Time period'] = combined['Time period'].fillna("Unknown") and combined = combined.dropna(subset=['Time period']).
We use this so we can fill and replace all missing values with the string "Uknown".Then we overwrite duplicates with the master columns using : combined['Observation value'] = combined['OBS_VALUE']
combined['Observation status'] = combined['OBS_STATUS']
combined['Unit multiplier'] = combined['UNIT_MULT'],then final we are going to use combined['UNIT_MULT'] = combined['UNIT_MULT'].fillna(0)
combined['Unit multiplier'] = combined['Unit multiplier'].fillna(0),to fill with zeros the missing values and also to make easier to clean the column using concat.



<img width="677" height="186" alt="Screenshot 2025-11-15 132514" src="https://github.com/user-attachments/assets/2ad9841d-db2e-4c83-af4e-1db7e1caab3f" />


<img width="633" height="152" alt="Screenshot 2025-11-15 135146" src="https://github.com/user-attachments/assets/15865249-fe9c-417f-8605-106cc676d231" />


<img width="666" height="120" alt="Screenshot 2025-11-15 135303" src="https://github.com/user-attachments/assets/d7da75d1-b4cf-4944-98ed-da931ab35fe0" />



  We use mexico_hours dataset,we import the csv file then we check the shape.After that we check the missing values and last we drop the missing columns and use :
usa_hours[['UNIT_MULT', 'Unit multiplier']] = usa_hours[['UNIT_MULT', 'Unit multiplier']].fillna(0)
mexico_hours[['UNIT_MULT', 'Unit multiplier']] = mexico_hours[['UNIT_MULT', 'Unit multiplier']].fillna(0)
 to fill the missing values with zero, here we do this with a more classical way of dividing the 2 datasets instead of concat. 



<img width="1478" height="725" alt="Screenshot 2025-11-14 223002" src="https://github.com/user-attachments/assets/a443600d-54fd-489a-a45f-f86ce9a60926" />


<img width="895" height="757" alt="Screenshot 2025-11-14 223034" src="https://github.com/user-attachments/assets/edc22dd0-e611-4a5d-ad7c-e1e747d7a5fc" />

<img width="832" height="223" alt="Screenshot 2025-11-15 173605" src="https://github.com/user-attachments/assets/a9676c36-55ed-4275-8b8b-adcbfa5f7573" />


<img width="832" height="207" alt="Screenshot 2025-11-15 173622" src="https://github.com/user-attachments/assets/ef5bde06-121f-45e4-97f6-1f894c003853" />



We load again the cvs then we add a country name to each column,we do this so we can find easy both datasets.Next
we aiready concat the datasets because we want to combine multiple datasets into one and also because we have almost the same datasets,we concat pieces of data together so we can analyze everything at once.
To show all rows and columns from both datasets USA and Mexico we use pd.set_option('display.max_rows', None) and ('display.max_columns', None).



<img width="1174" height="565" alt="Screenshot 2025-11-15 121508" src="https://github.com/user-attachments/assets/c4d00a97-9887-49d9-953e-4b00b74b8207" />


<img width="1485" height="476" alt="Screenshot 2025-11-15 121551" src="https://github.com/user-attachments/assets/2688066a-b68e-45f7-b053-9b20579fc982" />


<img width="1488" height="468" alt="Screenshot 2025-11-15 121628" src="https://github.com/user-attachments/assets/12171efa-9c2f-47d8-89e8-8142c74911ca" />





Our goal: to find missing values and get rid of them 

Before: 

<img width="305" height="695" alt="Screenshot 2025-11-15 174517" src="https://github.com/user-attachments/assets/ea815af2-ed7c-43b1-8021-ed23b8070597" />


After: 


<img width="276" height="686" alt="Screenshot 2025-11-15 174829" src="https://github.com/user-attachments/assets/9f86bfe0-642b-474f-9ae3-9e79b2052161" />





