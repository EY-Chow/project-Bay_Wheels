# Bay Wheels August 2021 Data Exploration Project by Elaine Chow

## Dataset

The data contains information on more than 200,000 bike-share rides in August 2021 in the Bay Area, including the type of bike, type of user, time of ride, start and end latitude/longitude points and date and time of ride. I augmented the dataset with additional columns: estimated distance, estimated cost and ride duration.

The original dataset can be found in on the Lyft website [here]( https://s3.amazonaws.com/baywheels-data/index.html) with a brief description of the data fields at [here]( https://www.lyft.com/bikes/bay-wheels/system-data).

In addition, there is a more detailed description of the Bay Wheels bike-sharing service in the Jupyter notebook for this project.


## Summary of Findings

In this dataset, there were specific fields I focused on: the type of rider (casual or member), the type of bike (classic, electric or docked), the day of the week, the start hour for the ride, the duration of the ride (calculated from start and end time), the estimated distance of the ride (calculated from start and end latitude/longitude points) and the estimated cost of the ride (calculated from the fee structure in place at that time). 

In the exploration, I found that in August 2021 there was a difference in ridership patterns between members and casual (non-member) riders. Rides by casual riders outnumbered rides by members on all days of the week. There were more rides by casual riders on the weekends, and there were more rides by members on the weekdays instead of the weekends. Rides by members tended to peak on Tuesday and tended to be lowest on Saturday and Sunday, while rides by casual riders were highest on Saturday and Sunday.

However, the ridership patterns between classic and electric bikes were similar; this is probably because both casual and members ride more electric bikes than classic bikes and because overall there are more rides by casual riders than by members. Electric bikes were overwhelmingly more popular than casual and docked bikes on weekends and weekdays as well. Both classic and electric bikes were ridden more often on Sunday, Tuesday and Saturday. Docked bikes, which were ridden only by casual riders, were ridden more often on Saturday and Sunday.  Interestingly, the number of rides by members on classic bikes is only slightly less than the number of rides by casual riders on classic bikes; this may be because the first 45 minutes of a classic bike ride is free for members.

There is a strong correlation between the duration of the ride and the estimated cost of a ride, which makes sense because Bay Wheels rates are based on time. There is also a strong correlation between the hour of day that a ride starts and the hour of day that a ride ends, which makes sense because the start time precedes the end time.

In general, plotting histograms of ride duration, estimated ride cost and estimated ride distance showed:

When plotted on a log-scale, the ride duration distribution is roughly unimodal, with a peak clustered at about 10 minutes. 

When plotted on a log-scale, the distribution of estimated ride cost shows a large spike at around $3, with another much smaller peak at around $6.

When plotted on a log-scale, the distance distribution is roughly unimodal, with spikes at roughly 0.9 km, 1.5 km, peaking at 1.75 km, with another spike at about 2.5 km.

## Key Insights for Presentation

For the presentation, I focused on rider type and bike type versus date and time data. I start by looking at total of rides per day, followed by the number of rides per day for members and casual riders and the number of rides per day on electric bikes and classic bikes. I use line charts to show the data patterns. I also created a bar chart showing mean ride duration in minutes by day of the week and rider type.
