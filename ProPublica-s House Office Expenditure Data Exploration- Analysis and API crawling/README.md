# ProPublica's House Office Expenditure Data Exploration, Analysis and API crawling

In this project I've decided to ask and answer some questions about the United State's House Office, 
namely it's expenditure from 2009 to 2018. 

All datasets can be downloaded from here: https://www.propublica.org/datastore/dataset/house-office-expenditures
Note that I have only used the datasets contained in the "Detailed" folder.

The formulated questions are as follow:

__1 - What is the total of all the payments in the dataset?__


__2 - What was the average annual expenditure with a 'START DATE' date between January 1, 2010
and December 31, 2016 (inclusive)?__


__3 - What was the highest average staff salary among all representatives in 2016? 
Assuming staff sizes is equal to the number of unique payees in the 'PERSONNEL COMPENSATION' category for each representative.__


__4 - What percentage of the expenditures of the top 20 spenders in 2016 come from members of the Democratic Party? 
Representatives are identified by their 'BIOGUIDE_ID', which can be used to look up representatives 
with ProPublica's Congress API to find their party affiliation. 
Considered an expenditure as being in 2016 if its 'START DATE' is in 2016.__


__5 - Define the 'COVERAGE PERIOD' for each payment as the difference (in days) between 'END DATE' and 'START DATE'. 
What is the standard deviation in 'COVERAGE PERIOD'? Only considered payments with strictly positive amounts.__


__6 - Find the 'OFFICE' with the highest total expenditures with a 'START DATE' in 2016. 
For this office, find the 'PURPOSE' that accounts for the highest total expenditures. 
What faction of the total expenditures (all records, all offices) with a 'START DATE' in 2016 do these expenditures amount to?__


__7 - What was the median rate of annual turnover in staff between 2011 and 2016 (inclusive)? 
Turnover for 2011 should be calculated as the fraction of a representative's staff from 2010 who did not carry over to 2011.
Only considered representatives who served for at least 4 years and had staff size of at least 5 every year that they served.__


The script can be run directly from beginning to end without the need to do anything else.

If an error is encountered in the API section, please register with ProPublica on https://www.propublica.org/datastore/api/propublica-congress-api
to obtain your own token key for API access. When you obtain this key please replace the headers variable

                              headers = {"X-API-Key" : "insert you own key here"}

The questions and answers are all being stored in a dictionary called results which will display at the end of the notebook.

Please feel free to ask any questions, propose code refactor, and ask your own questions about these very extensive datasets.

Have fun!
