# OPIM5512_lab1_YingZhang3300857_onlineF26
temp_f — air temperature, in deg F. 
Source: tmpf in the raw METAR file. 

dewpoint_f — dew point, in deg F. 
Source: dwpf in the raw METAR file. 

humidity_pct — relative humidity, %.
Source: relh in the raw METAR file.


windspeed_kt — wind speed, knots. 
Source: sknt in the raw METAR file.

load_mw — load, in mw. 
Source: load_mw in raw file of ISO New England

Additionally, 1 out of 744 hours is entirely missing in the data.

## Data Dictionary

### data/clean/weather_hourly.csv  (Partner A)
| column       | meaning                                          | units |
|--------------|--------------------------------------------------|-------|
| hour         | timestamp — the hour that BEGINS                 | —     |
| temp_f       | air temperature                                  | °F    |
| dewpoint_f   | dew point                                        | °F    |
| humidity_pct | relative humidity                                | %     |
| windspeed_kt      | wind speed                                        | knots |

**Convention:** `hour` is the hour that BEGINS. Weather is floored from the :51 observation.
**Missing hours:** drop the row.

### data/clean/demand_hourly.csv  (Partner B)
| column   | meaning                                   | units |
|----------|-------------------------------------------|-------|
| hour     | timestamp — the hour that BEGINS          | —     |
| load_mw  | New England system demand for that hour   | MW    |

**Convention:** `hour` is the hour that BEGINS. ISO-NE ships Hour Ending 1–24, so **subtract 1**
(HE 01 → 00:00).