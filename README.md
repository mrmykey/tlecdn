[![download tles](https://github.com/mrmykey/tlecdn/actions/workflows/tles.yml/badge.svg?branch=main)](https://github.com/mrmykey/tlecdn/actions/workflows/tles.yml)

# TLE CDN

The response time from [CelesTrak](https://celestrak.org/NORAD/elements/) can sometimes be slow.
This repository caches the latest TLE (Two-Line Element) files from CelesTrak and OMM files from
[Space-Track](https://www.space-track.org), **updating every 2 hours** to improve access speed.

## Source to Destination Mapping

### TLE

Retrieved from [CelesTrak](https://celestrak.org/NORAD/elements/).

| Source                                                                                              | Cached Destination                                                                                                    |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [active.txt](https://celestrak.org/NORAD/elements/gp.php?GROUP=active&FORMAT=tle)                  | [active.txt](https://raw.githubusercontent.com/mrmykey/tlecdn/refs/heads/main/active.txt)                            |
| [last-30-days.txt](https://celestrak.org/NORAD/elements/gp.php?GROUP=last-30-days&FORMAT=tle)      | [last-30-days.txt](https://raw.githubusercontent.com/mrmykey/tlecdn/refs/heads/main/last-30-days.txt)                |
| [space-stations.txt](https://celestrak.org/NORAD/elements/gp.php?GROUP=stations&FORMAT=tle)        | [space-stations.txt](https://raw.githubusercontent.com/mrmykey/tlecdn/refs/heads/main/space-stations.txt)            |
| [100-brightest.txt](https://celestrak.org/NORAD/elements/gp.php?GROUP=visual&FORMAT=tle)           | [100-brightest.txt](https://raw.githubusercontent.com/mrmykey/tlecdn/refs/heads/main/100-brightest.txt)              |
| [analyst.txt](https://celestrak.org/NORAD/elements/gp.php?GROUP=analyst&FORMAT=tle)                | [analyst.txt](https://raw.githubusercontent.com/mrmykey/tlecdn/refs/heads/main/analyst.txt)                          |

### OMM KVN & JSON

Retrieved from [Space-Track](https://www.space-track.org) — all active objects with epoch within the last 10 days.

| Format | Space-Track Query                                                                                                                                                         | Cached Destination                                                                                                      |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| KVN    | [gp/decay_date/null-val/epoch/>now-10/format/kvn](https://www.space-track.org/basicspacedata/query/class/gp/decay_date/null-val/epoch/%3Enow-10/format/kvn)               | [active-omm.kvn](https://raw.githubusercontent.com/mrmykey/tlecdn/refs/heads/main/active-omm.kvn)                      |
| JSON   | [gp/decay_date/null-val/epoch/>now-10/format/json](https://www.space-track.org/basicspacedata/query/class/gp/decay_date/null-val/epoch/%3Enow-10/format/json)             | [active-omm.json](https://raw.githubusercontent.com/mrmykey/tlecdn/refs/heads/main/active-omm.json)                    |

### EOP

Retrieved from [CelesTrak](https://celestrak.org/SpaceData/).

| Source                                                                  | Cached Destination                                                                                      |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [EOP-Last5Years.txt](https://celestrak.org/SpaceData/EOP-Last5Years.txt) | [eop.txt](https://raw.githubusercontent.com/mrmykey/tlecdn/refs/heads/main/eop.txt)                   |
