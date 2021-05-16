# PGA-EDA

Golf is a game of patience, precision, and tradition. Traditionally, there are four shot types, the drive, the approach, the chip, and the putt. The former two are considered 'long' shots and the latter two 'short' shots. There is a preconcieved notion in golf that the 'short-game' is more important than the 'long-game.' The idea of this project is to challenge that notion via statistical tests.

## Data
The data was parsed from PGA.com. There are 188 golfers and the data covers the 2019 pga season. It includes information pertaining to 'strokes-gained' for each shot type, for each golfer. Strokes gained essentially measures the effectiveness of a golfer's shot compared to that of the average competitor. The goal was to examine whether those who excelled in the short or long areas of the game performed better on the final score card. 

## Metrics
Since strokes-gained is a normalized statistic, I began indexing those who excelled at a shot by indexing those whose 'strokes-gained' was greater than zero for that shot type. I then engineered new features encompassing the short and long games by averaging together the strokes gained for short-type shots and long-type shots. Two test groups were formed by subsetting those whose strokes gained were greater than zero in the newly engineered field.

## Results
