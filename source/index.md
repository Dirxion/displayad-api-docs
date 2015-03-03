---
title: API Reference

language_tabs:
  - cURL
 

toc_footers:
  - <a href='http://www.dirxion.com'>API Powered By Dirxion</a>
  - <a href='http://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the Dirxion DisplayAdInfo API!  You can use our API to retrieve display ad information based on the user provided criteria.  This API
will allow users to retrieve advertiser data for single or multiple markets, within single or multiple headings.  The API will return JSON data containing
the ad information.

# Useage/Searching

Searching can be done directly or using the form atrribute.If you are searching from a form the URL is
http://www.yellowpagesgrouplive.ca/html5/ad_info_api.php

```shell
curl "http://www.yellowpagesgrouplive.ca/html5/ServiceGetAdInfo.php?BookCode=CLGRY&HeadingCode=0000005053,0000005052"

```

> The above command returns JSON structured like this:

```json
{"directories":[{"cgy13htm (CLGRY)":{"headings":[{"0000005053":{"total_ads":"6"},"0000005052":{"total_ads":"15"}}]},"cgy14htm (CLGRY)":{"headings":[{"0000005053":{"total_ads":"6"},"0000005052":{"total_ads":"11"}}]}}]}


```

### HTTP Request

`GET http://www.yellowpagesgrouplive.ca/html5/ServiceGetAdInfo.php?BookCode=CLGRY&HeadingCode=0000005053,0000005052`

### Query Parameters

Parameter | Description
--------- | -----------
BookCode  | The bookcode for the yellowpage publication (CLGRY)
HeadingCode |  A coma seperated collection of heading you wish to search (0000005053,0000005052)
BusName | Must be used in conjunction with a heading code to find a specific advertiser in that heading

<aside class="success">
If you have any questions let us know
</aside>
