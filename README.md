## Categories
declined = A_declined
cancelled = A_cancelled
approved = A_pending

RTPM cite this [tue paper](https://www.win.tue.nl/bpi/lib/exe/fetch.php?media=2017:bpi2017_paper_3.pdf) for the event classification


## Plan
1. get all the Application_IDs out of each category above
2. then build new, trace-based dataframe

## Trace DF
1. We take every application process one by one
2. From each we extract the full event-trace, and prefixes
    1. when it comes to prefixes, only stuff after A_accepted are interesting, everything before that is the same
3. Figure out the features to use