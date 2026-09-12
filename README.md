# OPIM5512_lab1_YingZhang3300857_onlineF26
temp — air temperature, in deg F. 
Source: tmpf in the raw METAR file. 

dewpoint — dew point, in deg F. 
Source: dwpf in the raw METAR file. 

humidity — relative humidity, %.
Source: relh in the raw METAR file.


wind_speed — wind speed, knots. 
Source: sknt in the raw METAR file.

Additionally, 1 out of 744 hours is entirely missing in the data.
### data/clean/demand_hourly.csv  (Partner B)
| column   | meaning                                   | units |
|----------|-------------------------------------------|-------|
| hour     | timestamp — the hour that BEGINS          | —     |
| load_mw  | New England system demand for that hour   | MW    |

**Convention:** `hour` is the hour that BEGINS. ISO-NE ships Hour Ending 1–24, so **subtract 1**
(HE 01 → 00:00).
