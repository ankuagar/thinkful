### What was the hottest day? Where was that?
`select zip from weather where MaxTemperatureF in (select max(MaxTemperatureF) max_temp from weather);`

`select zip, date, max(MaxTemperatureF) max_temp from weather group by zip, date order by max_temp desc limit 1;`



### How many trips started at each station?
`select start_station, count(trip_id) num_trips from trips group by start_station;`


