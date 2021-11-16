# Surfs_Up:surfer:

## Overview of the statistical analysis:mag:
For this challenge, the user tries to convince some investors to invest in the user's idea, which is to open a surf shop "Surf n 'Shake" in Hawaii. For the challenge, an analysis of the climate of the city was carried out with the objective of showing, based on  different dataframes, the climate of Oahu in the months of June and December.

The analysis was carried out on jupyter notebook using Python to create a more friendly and understandable dataframes so that members can visualize the behavior of Oahu's weather during those months.
## Results:ocean:
In the results, two dataframes were created to visualize the temperature of Oahu in the months of June and December in order to provide investors with relevant weather data, the dataframes are shown below:

![](https://github.com/Frankdiazw/Surfs_Up/blob/main/Resources/June_temps.png)![](https://github.com/Frankdiazw/Surfs_Up/blob/main/Resources/December_temps.png)

- Figure 1 and 2. Dataframes from the months of June and December in Oahu.

- Based on Figures 1 and 2, three conclusions can be drawn:

  - In the temperature tables for June and December, it can be observed in the measure of central tendency that shows the average (mean), that the average temperature in June is 74.9 degrees Fahrenheit and in December the average temperature is 71 degrees. Fahrenheit on Oahu respectively. This means that the change in temperature does not vary much, which is a good sign for investors since there will not be a sudden change in temperature that could decrease the sales of the surf shop.
  - It can also be observed that during the month of June in Oahu its minimum registered temperature was 64 degrees Fahrenheit and 85 its maximum. On the other hand, in December its minimum recorded temperature was 56 degrees Fahrenheit and 83 degrees Fahrenheit. Taking a look at the maximum and minimum temperatures, it can be seen that the maximum temperature of both months does not vary much, which is good, investors can expect clients to feel familiar with the weather. However, there is a difference in the minimum temperatures on Oahu in both months, which could affect a bit in December in the sales of the surf shop, further action needs to be taken.
  - Regarding the quartiles, the table shows three quartiles of 25%, 50% and 75% respectively. Taking a look at both tables, it can be seen the similarity in both quartiles, which is good since both temperature ranges do not vary much. That being said, customers are going to experience very similar climates year-round on Oahu.

## Summary:sunny::heavy_dollar_sign:
- During the analysis of the Oahu weather during the months of June and December, the user was asked to perform a series of steps in the jupyter notebook so that it could perform the visualization in two dataframes of the temperature of Oahu for the investors.
Taking into account what has been said in the Results section (see Results for more information about it), it is a very good option to make the investment for the surf shop "Surf n 'Shake" since as you can see, the temperatures are around in the same ranges every year.
According to various sources consulted, it is considered a very cold temperature to surf and go to the beach when the temperature is registered below 50 degrees Fahrenheit. That said, during the analysis the lowest temperature recorded on Oahu was 56 degrees Fahrenheit, which is still above the minimum temperature for surfing.
It was also calculated that the average temperature of Oahu in the months of June and December were 75 and 71 degrees Fahrenheit respectively. These are very good numbers as customers can expect very similar temperatures throughout the year and both meet the requirement of being above the minimum. That said, for the store it is very good data, since store sales are not going to decrease drastically in any season of the year.

- If the information gathered wanted to be compared to another station, we can call the next code to se the most active stations to gather information for the analysis:
  - session.query(Measurement.station, func.count(Measurement.station)).group_by(Measurement.station).order_by(func.count(Measurement.station).desc()).all()

- :tropical_fish: We can also gather the amount of precipitation at the most active station for June and December.
  - session.query(Measurement.prcp).filter(Measurement.station == 'USC00519281').filter(extract('month', Measurement.date) == 6).all()
  - session.query(Measurement.prcp).filter(Measurement.station == 'USC00519281').filter(extract('month', Measurement.date) == 12).all()
