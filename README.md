# WEB_SURVEY

This program uses Flask's built-in development server without installing a separate server.
Purpose: Collection of initial, weekly and daily surveys

## Environment
|NAME|VER|
|---|:---:|
|Ubuntu|18.04|
|Python|3.6.9|
|Flask|2.0.3|
|Wizverg|2.0.3|

## Author
|NAME|Position|
|---|:---:|
|Chaewon Song|Leader|
|Changwon Lee|Member|

---

## Directory    
```
Distribution
│   app.py
│   calIndexSearch.py    
|   save_csv_daily.py
|   deleteOverlapData.py
|   deleteUser.py
|   done.py
│   -fin.txt
|   -members.csv
|   -mood_data.csv
|   -mood_data_1.csv
|
└───static
│   │   jscript.js
│   │   main.js
│   │   style.css
|   |   en_style.css
|   |   main.css
|   |   various png file
|    
└───templates
│   │   main page (login page)
│   │   sign up page
│   |   daily calendar page
│   |   daily CON page
│   |   one time survey page
│   |   weekly survey page
│   |   daily survey page
│
survey_data
|
└───2023-1
│   │   S703_daily.csv
│   │   S703_onetime.csv
│   │   S703_weekly.csv
|   |   S704_daily.csv
|   |   S704_onetime.csv
|   |   S704_weekly.csv
|   |   ...
|    
└───2023-2
|   │   S700_daily.csv
|   │   S700_onetime.csv
|   │   S700_weekly.csv
|   |   S701_daily.csv
|   |   S701_onetime.csv
|   |   S701_weekly.csv
|   |   ...
matching1
|
│   601.csv
│   602.csv
│   603.csv
|   ...
matching2
|
│   700.txt
│   701.txt
│   702.txt
|   |   ...

```
---

## How to run

```
python app.py
```

## How to start
```
python app.py
Connect with url/register
```

---

## Management file    

### Sign up member    
* newMember.py    
* members.csv

### Delete User
* deletetUser.py

### Download survey data
1. Create a folder in "survey_data" 
2. Create a text file containing user ID (only number, same as foler name) 
3. run downloadOnetimeSurvey.py, downloadWeeklySurvey.py and downloadDailySurvey.py
```
python downloadOnetimeSurvey.py
python downloadWeeklySurvey.py
python downloadDailySurvey.py
```

### Comparison and validation between collection rates and surveys
* This progress need fin.txt (people who end of collection)
* More than 10% collection rate
* fin.txt format (only number exclude character 'S')
#### See the comment
* modify for android
* modify for iOS
1. Create matching forlder to store Data files collected by date
2. run save_csv_daily.py then maked mood_data.csv
3. add header in mood_data.csv and run deleteOverlaData.py then maekd modified mood_data.csv
4. run done.py then maked overlap_both_per_sur_{date}.csv
