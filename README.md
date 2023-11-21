# Analyzing-Lake-Mendota-in-the-Winter

Using ggplot2 in R to Analyze Lake Mendota in the Winter. Specifically, observing how long Lake Mendota freezes each winter, and identifying the pattern through various graphs.

## Lake Mendota
- Scientists have been recording the dates when Lake Mendota first closes with ice (at least half the surface is covered with ice) and opens (more than half the surface is liquid water) since the middle of the 1800s.
- In most winters, there is a single uninterrupted period of time from the first time the lake is closed in the winter to the first time it reopens in the spring.
    - Some winters have multiple intervals of closure
- The data set I am using summarizes the raw data with a single row for each winter from 1855--56 through last winter, 2021--22.
    - The variable `year1` is the first year of the given winter.
    - The variable `duration` is the total number of days that Lake Mendota was closed by ice in the given winter.
        - Note: the word "winter" used here specifies a single season spanning two consecutive calendar years and does not use the endpoints from the winter solstice to the spring equinox, for example.
#### The data is in the `lake-mendota-winters-2022.csv` file in this repository

## Question: How long does Lake Mendota freeze each winter?

To answer this question, I used multiple graphs to visualize the data:

- Scatter Plot (with a Trend Line)
- Histogram (with Bin Endpoints)
- Density Plot (with Vertical Lines representing the Standard Deviations)
- Box Plot (with Outliers)
- Side-by-side Box Plots (with Outliers)

## Scatter Plot
<img width="680" alt="Screen Shot 2023-11-20 at 12 35 29 AM" src="https://github.com/adityakmehrotra/Analyzing-Lake-Mendota-in-the-Winter/assets/24847438/d4dffe48-d577-40aa-a9fc-fc21386613b1">

### Observations
- There appears to be a decrease in Lake Mendota's freeze duration over time
- Informally, we can interpret the blue curve in the plot as a description of what the climate is doing in Wisconsin.
  - When ignoring the year-to-year fluctuations, we see that the average freeze duration of Lake Mendota over the winter has decreased from 120 days (around 17 weeks) in the mid 1850s to just under 80 days (around 11 weeks) in 2022.
- The variation of the points around the blue curve may be interpreted as random “noise” caused by differences in the weather at key parts of the fall and winter seasons.


## Histogram
<img width="673" alt="Screen Shot 2023-11-20 at 12 35 32 AM" src="https://github.com/adityakmehrotra/Analyzing-Lake-Mendota-in-the-Winter/assets/24847438/6cd4ab6b-fc8e-4a45-8b3a-33b138601742">

### Observations
- The arguments `binwidth = 7` and `boundary = 0` determine which intervals will be used in the histogram.
    - Possible intervals include 0 to 7, 7 to 14, 14 to 21, and so on, but also $-7$ to 0, $-14$ to $-7$ and so on.
    - The actual minimum and maximum data values determine which intervals appear in the plot.
    - The smallest duration is 21 which is counted in the bin from 21 to 28.
    - Note that if `boundary = 7` had been specified, the bins would be exactly the same: pick **one boundary** and **one bin width** to determine the end points of **all bins**.
    - But, if `boundary = 10` had been specified, this would have shifted all of the bin boundaries three to the right and the graph would have different bins and different counts.
- An alternative way to specify the intervals is with the `center` of one of the intervals instead of the `boundary` between two adjacent ones.
- This graph centers a boundary at 0 with `binwidth = 7` still.
    - The intervals are from $-3.5$ to 3.5, 3.5 to 10.5, and so on.
    - This histogram is identical except that the intervals are shifted


## Density Plot
<img width="676" alt="Screen Shot 2023-11-20 at 12 35 35 AM" src="https://github.com/adityakmehrotra/Analyzing-Lake-Mendota-in-the-Winter/assets/24847438/95d6da35-b2b7-4ad0-9311-3ba81f12114a">

### Observations
- From this plot, we see that the distribution of year to year annual variation around the trend curve is approximately bell-shaped, but there is some slight left skewness (the left tail is bigger than the right tail).


## Box Plot
<img width="683" alt="Screen Shot 2023-11-20 at 12 35 38 AM" src="https://github.com/adityakmehrotra/Analyzing-Lake-Mendota-in-the-Winter/assets/24847438/28e811db-7e38-495d-a441-84317c33f079">

### Observations
- It appears that 4 times in the past 167 winters, the duration that Lake Mendota was closed in the winter by ice was 60 days or less.
- Also, 2 times in the past 167 winters, the duration that Lake Mendota was closed in the winter by ice was 140 days or more.
- More than half of the winters in the past have closed Lake Mendota because of ice for between 100 and 115 days.


## Side-by-side Box Plots
<img width="681" alt="Screen Shot 2023-11-20 at 12 56 24 AM" src="https://github.com/adityakmehrotra/Analyzing-Lake-Mendota-in-the-Winter/assets/24847438/fbcaa8f5-5833-49c1-b406-5ceeb88869bd">

### Observations
- We see that in the 1800s, a typical freeze duration was nearly 120 days whereas in more recent decades, a typical duration has decreased to under 90 days.

## Run the Code
Knit the rmd file (`ggplot2.rmd`) with the data file (`lake-mendota-winters-2022.csv`) and script file (`script.R`) downloaded to get an outputted HTML file (`ggplot2.html`) with my results.

All of these files are in the current repository.
