Discuss the purpose of this database in the context of the startup, Sparkify, and their analytical goals.

How to run the Python scripts
use cmd

An explanation of the files in the repository
there are two type json.file
one is data of song information
the other one is data log of user

I have one question.
I tried a command command but it was abort.
Then" ERROR:  current transaction is aborted, commands ignored until end of transaction block" always follows to next seqence
I want to cancel the wrong transaction that i executed command
can you give me some advice

State and justify your database schema design and ETL pipeline.

i created database fact data and four Dimension Table
actually songplays(fact table) was most important in tables, and it was connecting to the other tables by key values
I extracted the data by song, customer log, transform data ex) datetime, and Loaded in the songplays table
