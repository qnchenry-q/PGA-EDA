# PGA-EDA

Golf is a game of patience, precision, and tradition. Traditionally, there are four shot types, the drive, the approach, the chip, and the putt. The former two are considered 'long' shots and the latter two 'short' shots. There is a preconcieved notion in golf that the 'short-game' is more important than the 'long-game.' The idea of this project is to challenge that notion via statistical tests.

## Data
The data was parsed from PGA.com. There are 188 golfers and the data covers the 2019 pga season. It includes information pertaining to 'strokes-gained' for each shot type, for each golfer. Strokes gained essentially measures the effectiveness of a golfer's shot compared to that of the average competitor. The goal was to examine whether those who excelled in the short or long areas of the game performed better on the final score card. 

## Metrics
Since strokes-gained is a normalized statistic, I began indexing those who excelled at a shot by indexing those whose 'strokes-gained' was greater than zero for that shot type. I then engineered new features encompassing the short and long games by averaging together the strokes gained for short-type shots and long-type shots. Two test groups were formed by subsetting those whose strokes gained were greater than zero in the newly engineered field.

![pga scoring averages](https://user-images.githubusercontent.com/59183694/119506252-5b704c00-bd33-11eb-90cb-684f4c002c1a.png)

![long strokes gained histogram](https://user-images.githubusercontent.com/59183694/119506141-3f6caa80-bd33-11eb-802b-6ce8f973983c.png)
![short strokes gained histogram](https://user-images.githubusercontent.com/59183694/119506217-527f7a80-bd33-11eb-84e6-1eafb320c8d5.png)



## Results
The statistical test implemented was Welch's T-Test. Welch's T-Test is used to gain insight as to whether two populations have equal means. Below is a histogram showing the two populations. The x-axis is mapped to the number of strokes gained. The y-axis shows the number of occurences of that strokes-gained value in the popuation. The null hypothesis for this trial was that the two populations did in fact have equal means. The test concluded that we are unable to say that the populations' means are different. 

![long_short_golf_scoring](https://user-images.githubusercontent.com/59183694/119506307-67f4a480-bd33-11eb-9498-3573c5588443.png)

