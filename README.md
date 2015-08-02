#TimeDistPy

TimeDistPy (Timely Distribution of Data in Python) allows you view the data that has an active period. An example would be a software outsourcing company that has many projects it developed, wants to see the time-oriented view of how much they make in a certain period. Assume the company has projects data as follows in some data store.

## Input data

PROJECT_NAME | START_DATE | END_DATE | PROJECT_PROFIT
-------------|------------|----------|---------------
project1     |2012-02-3   |2013-01-05|20500
project2     |2012-02-6   |2012-04-21|45000
project3     |2012-02-4   |2013-02-12|32000
project4     |2012-10-12  |2013-05-7 |98000
    
And tddpy module allows you to distribute those values into days granularity as follows

    date        project1    project2    project3    project4
2012-02-3       1000        0           0           0
2012-02-4       1000        0           300         0
2012-02-5       1000        0           300         0
2012-02-6       1000        500         300         0
    .
    .
    .
    
After that, simple aggregation can be queried. For example, on day "2012-02-6", give the sum (or) maximum of profit for that day, and so on.
