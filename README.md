# cyclist-bike-share-analysis
My first case study for Data Analysis, capstone project for Coursera's Google Data Analytics Course.
This is the process I went through while completing this case study.

--ASK

1. Business task:
  "The problem we're trying to solve is understanding the similarities and differences between casual riders and annual members, so we can use that information to help convert casual riders into annual members."
2. Key stakeholders:
  "The key stakeholders are Lily Moreno (the marketing director), the Cyclistic executive team, and the marketing analytics team."
3. How insights drive the decision:
  "It unlocks the decision of how to target casual riders with a marketing strategy, based on how their riding behavior compares to that of current annual members."

--PREPARE
1. Data location & organization:
  "The data consists of 12 CSV files representing the past 12 months of Cyclistic trip data, each containing fields including ride_id, rideable_type, started_at, ended_at, start/end station names and IDs, start/end latitude and longitude, and member_casual."
2. ROCCC:
  Reliable — The data comes directly from Cyclistic's own ride-tracking system, capturing every trip taken, not a sample or estimate.
  Original — First-party data, collected directly by Cyclistic through its own bike-share system (not secondhand or scraped from a third party).
  Comprehensive — It includes the key fields needed to answer the business question — ride times, station locations, bike type, and rider type (member vs. casual) — though it's limited to trip-level behavior and doesn't include demographic or payment information.
  Current — Covers the most recent 12 months of ride data, so it reflects up-to-date usage patterns rather than outdated behavior.
  Cited — The data is publicly provided by Motivate International Inc. under their specific license, which is referenced in the case study.
3. Privacy considerations:
  We cannot connect a customers credit card 9nfo to a ride as that is breach of privacy, so we won't know how many times a particular rider has used the service.
4. Data integrity:
  Missing values in start_station_name/start_station_id and end_station_name/end_station_id — likely from dockless or valet-style returns where a bike wasn't returned to an official station.
  Possible inconsistent column structure across the 12 monthly files, if any months used a different schema.
  Potential invalid time values — cases where ended_at is earlier than started_at, which would produce a negative or nonsensical ride_length once calculated in the Process phase.
  Possible duplicate ride_id entries across files, which would inflate ride counts if not caught before merging.
