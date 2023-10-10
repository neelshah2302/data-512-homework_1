
[![GitHub license](https://img.shields.io/github/license/ishank09/data-512-homework_1)](https://github.com/ishank09/data-512-homework_1/blob/main/LICENSE)

# Wikimedia Articles - Pageview count extraction

# Goal of the project:
The goal of this project is to construct, analyze, and publish a dataset of monthly article traffic for a select set of pages from English Wikipedia from July 1, 2015 through September 30, 2023. We will be using a subset of wikimedia articles to extract page view counts for the same across time.

# Licence: 
https://www.mediawiki.org/wiki/API:REST_API#Terms_and_conditions

# REST API Documentation: 
https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews
https://wikimedia.org/api/rest_v1/#/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end

# Implementation:

1. Data_acquistion_articles.ipynb - This notebook will be run as the 1st step and helps in data acquistion. Use the REST API to get pageview counts for the articles in the subset. The intermediate output from running this notebook are 3 json files for Mobile, Desktop and Cumulative dataframes of time series of monthly activity.

   1. academy_monthly_mobile_201501-202309.json
   2. academy_monthly_desktop_201501-202309.json
   3. academy_monthly_cumulative_201501-202309.json

2. Data_Analysis_articles.ipynb - This notebook will be run as 2nd step and will display the final analysis like visualizations and steps for metric creation. The output of this notebook are 3 .png files for the 3 data vicualizations

   1. Max Average and Mean Average:
      ![min_avg_max_avg](https://github.com/neelshah2302/data-512-homework_1/assets/122260079/a3025d31-d0ed-4f2c-8374-e67c617a6659)

   2. Top 10 Peak page views
      ![top10_peaks](https://github.com/neelshah2302/data-512-homework_1/assets/122260079/df20894c-702e-4533-9518-eb938fd97d82)

   3. Fewwst Months
      ![fewest_months](https://github.com/neelshah2302/data-512-homework_1/assets/122260079/9097a07a-d355-4d99-8fdd-2fd7a6dd41a6)


# Issues or special considerations:

1. There are some articles for which the data isnt present or cannot be extracted using the API. I have printed the list of such articles in the notebook but more research on the same is needed.
2. The fetch for each article takes a long time and thus the overall required time for run is more than 20 mins. This is a big issue when the list or data is too big
