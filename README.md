# Statistica-UNITN
Page of 2019 marks: https://docs.google.com/spreadsheets/d/1xDTFy_oSF6smH6gWwwt4T3QZtLoTRGazkQRKLxoxvhQ/pubhtml  
The students ID are not publicly available.

Programs made in Python to manage the [exercise website](http://datascience.maths.unitn.it/ocpu/library/doexercises/www/) of the professor Agostinelli.  
With this programs you are able to:
* [Brute force ID numbers](https://github.com/MarcoDiFrancesco/statistica-unitn/blob/master/bruteForceMatricola.py) (matricole) of students
* [Download marks](https://github.com/MarcoDiFrancesco/statistica-unitn/blob/master/getMarks.py) of the students you have the ID number, and put them in a [Google Spreadsheet](https://docs.google.com/spreadsheets/)
* [Request token](https://github.com/MarcoDiFrancesco/statistica-unitn/blob/master/requestToken.py) continuously (usefull for the 1st May exercise)

All of these programs need:
* Python installed
* The gspread (Google Spreadsheets) libraries installed:  
`pip install gspread`
* Selenium libraries installed  
`pip install -U selenium`
* [Download](https://sites.google.com/a/chromium.org/chromedriver/downloads) selenium driver to make it working with Chrome, old version of the drivers is already present in the repository

Download marks program needs:
* A [Google Spreadsheet](https://docs.google.com/spreadsheets), once done copy the link key into the programs you want to use in the section  
`sheet = gc.open_by_key()`  
e.g. with the link `https://docs.google.com/spreadsheets/d/1xDTFy_oSF6smH6gWwwt4T3QZtLoTRGazkQRKLxoxvhQ`  
write `sheet = gc.open_by_key('1xDTFy_oSF6smH6gWwwt4T3QZtLoTRGazkQRKLxoxvhQ')`
* Drive API on [Cloud console](https://console.developers.google.com/apis) to connect it with Spreadsheet, ([tutorial](https://developers.google.com/sheets/api/quickstart/python)), once downloaded the Spreadsheets API in JSON format, rename the file to `credentials.json` and put it the the project folder

Done