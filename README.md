# Analyzing-Lake-Mendota-in-the-Winter

Using ggplot2 in R to Analyze Lake Mendota in the Winter. Specifically, observing how long Lake Mendota freezes each winter, and identifying the pattern through various graphs.

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

## Density Plot
<img width="676" alt="Screen Shot 2023-11-20 at 12 35 35 AM" src="https://github.com/adityakmehrotra/Analyzing-Lake-Mendota-in-the-Winter/assets/24847438/95d6da35-b2b7-4ad0-9311-3ba81f12114a">

## Box Plot
<img width="683" alt="Screen Shot 2023-11-20 at 12 35 38 AM" src="https://github.com/adityakmehrotra/Analyzing-Lake-Mendota-in-the-Winter/assets/24847438/28e811db-7e38-495d-a441-84317c33f079">

## Side-by-side Box Plots
<img width="681" alt="Screen Shot 2023-11-20 at 12 56 24 AM" src="https://github.com/adityakmehrotra/Analyzing-Lake-Mendota-in-the-Winter/assets/24847438/fbcaa8f5-5833-49c1-b406-5ceeb88869bd">

Run the R Script file to get an outputted HTML file with my results.
