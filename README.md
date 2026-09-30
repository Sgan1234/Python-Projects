# NYC FloodNet: Street Flooding Analysis

A Python analysis of street-level flooding in New York City using data from the
[FloodNet](https://www.floodnet.nyc) sensor network, published on
[NYC Open Data](https://data.cityofnewyork.us/Environment/FloodNet-Street-Flooding-Events-Measured-by-FloodN/aq7i-eu5q/about_data).

## Overview

FloodNet is a network of low-cost sensors deployed across NYC to measure
street-level flooding in real time. This project explores the resulting flood
event data to answer questions about when, where, and how severely flooding
occurs.

## Research Questions

- How has flood frequency changed over time?
- Which locations experience the most flooding?
- Is there a relationship between flood depth and duration?
- What does a typical flood event "look like" over time?

## Dataset

- **Source:** NYC Open Data — FloodNet: Street Flooding Events Measured by FloodNet Sensors
- **URL:** https://data.cityofnewyork.us/Environment/FloodNet-Street-Flooding-Events-Measured-by-FloodN/aq7i-eu5q/about_data
- **Records:** One row per QC-approved flood event
- **Key columns:**

| Column | Description |
| :--- | :--- |
| `sensor_name` | Human-readable sensor location name |
| `sensor_id` | Unique sensor identifier |
| `flood_start_time` | Event start time (GMT) |
| `flood_end_time` | Event end time (GMT) |
| `max_depth_inches` | Peak flood depth during the event |
| `onset_time_mins` | Minutes from start to peak depth |
| `drain_time_mins` | Minutes from peak depth to zero |
| `duration_mins` | Total event duration |
| `duration_above_4_inches_mins` | Time at or above 4 inches |
| `duration_above_12_inches_mins` | Time at or above 12 inches |
| `duration_above_24_inches_mins` | Time at or above 24 inches |
| `flood_profile_depth_inches` | JSON array of depth readings |
| `flood_profile_time_secs` | JSON array of timestamps for the depths |

A flood event is defined as water depth exceeding 10 mm beneath a sensor.

## Tools

- Python 3
- pandas
- matplotlib
- seaborn

## Setup

```bash
git clone https://github.com/<your-username>/nyc-floodnet-analysis.git
cd nyc-floodnet-analysis
pip install pandas matplotlib seaborn
