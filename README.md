[![download tles](https://github.com/mrmykey/tlecdn/actions/workflows/tles.yml/badge.svg?branch=main)](https://github.com/mrmykey/tlecdn/actions/workflows/tles.yml)

# TLE CDN

The response time from [CelesTrak](https://celestrak.org/NORAD/elements/) can sometimes be slow. 
This repository caches the latest TLE (Two-Line Element) files from CelesTrak and **updates them hourly** 
to improve access speed.

## Source to Destination Mapping

The following TLE datasets are retrieved from CelesTrak and cached in this repository:

| CelesTrak Source                                                                                    | Cached Destination                                                                                        |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [active.txt](https://celestrak.org/NORAD/elements/gp.php?GROUP=active&FORMAT=tle)                   | [active.txt](https://raw.githubusercontent.com/mrmykey/tlecdn/refs/heads/main/active.txt)                 |
| [last-30-days.txt](https://celestrak.org/NORAD/elements/gp.php?GROUP=last-30-days&FORMAT=tle)       | [last-30-days.txt](https://raw.githubusercontent.com/mrmykey/tlecdn/refs/heads/main/last-30-days.txt)     |
| [space-stations.txt](https://celestrak.org/NORAD/elements/gp.php?GROUP=stations&FORMAT=tle)         | [space-stations.txt](https://raw.githubusercontent.com/mrmykey/tlecdn/refs/heads/main/space-stations.txt) |
| [100-brightest.txt](https://celestrak.org/NORAD/elements/gp.php?GROUP=visual&FORMAT=tle)            | [100-brightest.txt](https://raw.githubusercontent.com/mrmykey/tlecdn/refs/heads/main/100-brightest.txt)   |
| [analyst.txt](https://celestrak.org/NORAD/elements/gp.php?GROUP=analyst&FORMAT=tle)                 | [analyst.txt](https://raw.githubusercontent.com/mrmykey/tlecdn/refs/heads/main/analyst.txt)               |

