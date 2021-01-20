# Python for Power BI developers: Filling gaps in a timetable in PowerBI


## What’s the situation?

Suppose you have a monitoring system that logs failed calls to your server. The server is up and running most of the time but is also down from time to time. You’d like to show this visually, but your dataset of failed calls over time is sparse.

## What’s the objective?

Instead of showing numbers in a table—which can be hard to interpret at a glance—you have in mind a visual that resembles how heart rates are presented to medical personnel (in other words, a “heartbeat chart”). That would help to make it more obvious when the system is down, so the user can take corrective action.


(...)

Take a look at the the rest of the article on Medium! :smile:

TODO: Link Medium article here

## Replicating the above 

### I. Python separately from PowerBI

You can create your filled time table separately in the Jupyter notebook **fill_time_gaps_Medium.ipynb** instead of embedding the Python script in PowerBI. 

Python (through the Jupyter notebook) creates "calls_server_across_time_filled.csv". Then PowerBI can pull this csv file and build visual on top of it. Please refer to the tab "Python and PowerBI separately" in the pbix file. 

### II. Python embedded in PowerBI

You can also embed directly your Python script in PowerBI. 
1. Python script (through Transform Data in PowerBI) reads original table of sparse failed calls "calls_server_across_time"
2. Python processes it and fills in time gaps 
3. Python outputs result in PowerBI. You need to select "df_merge" table in the selection after running Python script

Finally, like in I., PowerBI can build nice visuals on top of the output table. Please refer to the tab "Python within PowerBI" in the pbix file. 
