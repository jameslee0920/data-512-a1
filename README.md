### Goal
The goal of this project is to construct, analyze, and publish a dataset of monthly traffic on English Wikipedia from January 1 2008 through August 30 2020. 

### Data Source
Two different Wikimedia REST API endpoints were combined into a single dataset.  The data was then processed into a simple csv dataset to be analyzed.  The two Wikimedia REST API endpoints included are [Pageview](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews) and [Pagecounts](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts)

[**Wikimedia Foundation REST API terms of use**](https://www.mediawiki.org/wiki/Wikimedia_REST_API#Terms_and_conditions)

### Final Data Fields
| Column                  | Value     |
|-------------------------|-----------|
| year                    | YYYY      |
| month                   | MM        |
| pagecount_all_views     | num_views |
| pagecount_desktop_views | num_views |
| pagecount_mobile_views  | num_views |
| pageview_all_views      | num_views |
| pageview_desktop_views  | num_views |
| pageview_mobile_views   | num_views |
Example of generating a datetime value from year and month is included in notebook file.

### Known Issues and Special Considerations
One special consideration with the data is that the Pageview API excludes spiders/crawlers data, taking only user agent data, but data from Pagecounts API do not.  
Additionally, mobile data is unavailable until October 2014.  Previous data includes only desktop or main site views.  
