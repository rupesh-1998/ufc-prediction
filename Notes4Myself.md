# 1. Scraping the files

## What each file in the scraper section does

``` scrape_ufc_stats_config.yaml ```
- holds the 'schema' for all the csv files compiled after scraping

``` scrape_ufc_stats_library.py ```
- holds all of the functions used to scrape ufc stats

``` scrape_ufc_stats_all_historical_data.ipynb ```
- parses all past ufc fight stats when run, does not include upcoming fights
- outputs: event details, fight details, fight results, fight stats

``` scrape_ufc_stats_fighter_tott.ipynb ```
- parses all fighters' details and tale of the tape
- outputs: fighter details, fighter tale of the tape

``` scrape_ufc_stats_unparsed_data.ipynb ```
- checks existing files for previously parsed data
- if there are no new or unparsed events, script stops
- if there are any unparsed events, script continues with parsing
- combine new data and existing data into one and write to file
- script '.py' version of this notebook avaiable to run on schedule

``` scrape_ufc_stats_working_example.ipynb ```
- shows how the previous scripts and notebooks work with small examples

To re-scrape all files, run ``` scrape_ufc_stats_all_historical_data.ipynb ``` and ``` scrape_ufc_stats_fighter_tott.ipynb ```.

Data for all events, fights, and fighters have scraped and saved as the following data files:
```
ufc_event_details.csv
ufc_fight_details.csv
ufc_fight_results.csv
ufc_fight_stats.csv
ufc_fighter_details.csv
ufc_fighter_tott.csv
```

``` fm_fighter_details.ipynb ```
- return a csv file with all fighters from fighter details and their urls in fight matrix for 'scrape_fight_matrix.ipynb' to use

``` scrape_fight_matrix.ipynb ```
- scrapes fightmatrix for ranks
- outputs figher ranks at specific dates at their weight class at that moment in time

