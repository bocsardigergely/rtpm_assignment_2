## Categories
declined = A_denined  
cancelled = A_cancelled  
approved = A_pending  

RTPM cite this [Professional 1](https://www.win.tue.nl/bpi/lib/exe/fetch.php?media=2017:bpi2017_paper_3.pdf) for the event classification !WINNER! [Professional 4](https://www.win.tue.nl/bpi/lib/exe/fetch.php?media=2017:bpi2017_winner_professional.pdf)

RTPM cite this [Academic 1](https://www.win.tue.nl/bpi/lib/exe/fetch.php?media=2017:bpi2017_paper_31.pdf) for a different event classification & Section 6 Analysis of Incomplete Cases

RTPM cite this !WINNER! Academic: [Academic 2](https://www.win.tue.nl/bpi/lib/exe/fetch.php?media=2017:bpi2017_winner_academic.pdf) for a different filtering cases not yet finished - section 2 last part - might prove above papers' event clf are the same


## Plan
1. get all the Application_IDs out of each category above
2. then build new, trace-based dataframe

## Trace DF
1. We take every application process one by one
2. From each we extract the full event-trace, and prefixes
    1. when it comes to prefixes, only stuff after A_accepted are interesting, everything before that is the same
3. Figure out the features to use
 

## Init Features - event logs
case_attr = ['FirstWithdrawalAmount', 'NumberOfTerms', 'Accepted', 'MonthlyCost', 'Selected', 'CreditScore', 'OfferedAmount', 'OfferID', 'case:LoanGoal', 'case:ApplicationType', 'case:concept:name', 'case:RequestedAmount']

event_attr_cat = ['org:resource', 'concept:name', 'lifecycle:transition']  
event_attr_num = ['time:timestamp']


## TODO

How to encode datetime in pandas df?
- https://www.analyticsvidhya.com/blog/2020/05/datetime-variables-python-pandas/