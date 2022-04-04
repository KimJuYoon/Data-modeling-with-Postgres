## Data Modeling with Postgres
***
By Yoon [https://github.com/KimJuYoon/Udacity/tree/master]</br>
<span style="font-size:100% ; color:blue">#udacity #ORM #postgres #ETL</span>  

**Introduction**

A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team is particularly interested in understanding what songs users are listening to. Currently, they don't have an easy way to query their data, which resides in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

They'd like a data engineer to create a Postgres database with tables designed to optimize queries on song play analysis, and bring you on the project. Your role is to create a database schema and ETL pipeline for this analysis. You'll be able to test your database and ETL pipeline by running queries given to you by the analytics team from Sparkify and compare your results with their expected results.


<details><summary> Data Set</summary>
[http://millionsongdataset.com/]

###### Song Dataset
> song_data/A/B/C/TRABCEI128F424C983.json
> song_data/A/A/B/TRAABJL12903CDCF1A.json

> {"num_songs": 1, "artist_id": "ARJIE2Y1187B994AB7", "artist_latitude": null, "artist_longitude": null, "artist_location": "", "artist_name": "Line Renaud", "song_id": "SOUPIRU12A6D4FA1E1", "title": "Der Kleine Dompfaff", "duration": 152.92036, "year": 0}


###### Log Dataset

>log_data/2018/11/2018-11-12-events.json
>log_data/2018/11/2018-11-13-events.json

>![log-data](log-data.png)

</details>

<details>
    <summary>Schema </summary>

#### Fact Table

| songplays |
| --------: |
| songplay_id |
| start_time |
| user_id |
| level |
| song_id |
| artist_id |
| session_id |
| location |
| user_agent |

#### Dimension Tables

| users     | songs      | artists    | time      |
| :-------- | :--------: | :--------: | --------: |
| user_id   |song_id     |artist_id   |start_time |
| first_name|title       |name        |hour       |
| last_name |artist_id   |location    |day        |
| gender    |year        |lattitude   |week       | 
| level     |duration    |longitude   |month      |
|           |            |            |year       |
|           |            |            |weekday    |

</details>

<details><summary> How to run the ETL pipeline</summary>

0. Run 'create_tables.py' to initialise the database
1. Run 'ETL.py' to processing ETL pipeline
2. Run 'test.ipynb' to ensure your executing

</details>