# Twitter-in-StreamSets
Streaming filtered Tweets by StreamSets Data Collector using API v2 

## Requirements
* StreamSets Data Collector (DC) Instance: https://hub.docker.com/r/streamsets/datacollector
* Twitter Developer Account associated with a project: https://developer.twitter.com/en/portal/dashboard
* Twitter API v2 Consumer Keys and Access Tokens

## Background
Twitter API v1 truncates Tweet texts effectively hindering text analysis. API v2 provides this access; however, integrating API v2 with StreamSets Data Collector is not quite straightforward. This Git aims to simplify the process. Complete step-by-step tutorial is available in this repo.

## Process
1. Connect DC to Twitter using OAuth2: https://streamsets.com/documentation/datacollector/latest/help/datacollector/UserGuide/Processors/HTTPClient.html#concept_s4p_15f_5y
2. Create and post rules to the POST endpoint URL using Preview mode in DC: https://developer.twitter.com/en/docs/twitter-api/tweets/filtered-stream/api-reference/post-tweets-search-stream-rules
3. Verify the rules by GET request to the same endpoint URL
4. If rules are present, change the endpoint URL and use GET method to stream the filtered Tweets: https://developer.twitter.com/en/docs/twitter-api/tweets/filtered-stream/api-reference/get-tweets-search-stream
