---
title: "How the hell does Google Search Work?"
excerpt: "Google Search is a fully-automated search engine that uses software known as web crawlers that explore the web regularly to find pages to add to our index. In other words, it's like garbage men going around collecting trash and taking it back to the landfill periodically."
coverImage: "/assets/blog/how-the-hell-does-google-search-work/google-on-smartphone.jpg"
date: "2024-03-12T05:35:07.322Z"
author:
  name: Alan Esquivel
  picture: "/assets/blog/authors/alanesquivel.png"
ogImage:
  url: "/assets/blog/how-the-hell-does-google-search-work/google-on-smartphone.jpg"
---

First things first, Google doesn't accept payment to crawl a site more frequently, or rank it higher. If anyone tells you otherwise, **you're getting played**. Google doesn't guarantee that it will crawl, index, or serve your page, even if your page follows the [Google Search Essentials](https://developers.google.com/search/docs/essentials).

## Google Search is a three stage system

1. [Crawling](https://developers.google.com/search/docs/fundamentals/how-search-works#crawling): Google downloads text, images, and videos from pages it found on the internet with automated programs called crawlers.
2. [Indexing](https://developers.google.com/search/docs/fundamentals/how-search-works#indexing): Google analyzes the text, images, and video files on the page, and stores the information in the Google index, which is a large database.
3. [Serving Search Results](https://developers.google.com/search/docs/fundamentals/how-search-works#serving)

## Crawling

The first step is discovery, to see what web pages are out! The great adventure of the web crawler to find new web pages. You can call this "URL discovery". The program that does the fetching is called [Googlebot](https://developers.google.com/search/docs/crawling-indexing/googlebot) (also known as a crawler, robot, bot, spider, or garbage man in my example lol). Googlebot uses an algorithmic process to determine which sites to crawl, how often, and how many pages to fetch from each site. 

Not every page is crawlable by the little homie Googlebot, Some pages may be [disallowed for crawling](https://developers.google.com/search/docs/crawling-indexing/robots/robots_txt#disallow) by the site owner, other pages may not be accessible without logging in to the site.


## Indexing

Once GoogleBot finishes his 8 hour workday, the next step is to index all the webpages he crawled. This includes reviewing title elements, images, alt attributes (you know the one web developers always leave empty cause it takes forever to think of alt tag names), videos and more.

During the indexing process, Google determines if a page is a [duplicate of another page on the internet or canonical](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls). The canonical is the page that may be shown in search results. To select the canonical, we first group together (also known as clustering) the pages that we found on the internet that have similar content, and then we select the one that's most representative of the group. The other pages in the group are alternate versions that may be served in different contexts, like if the user is searching from a mobile device or they're looking for a very specific page from that cluster.

This is important, because during the next stage where Google serves the content, all the nitty gritty dull work you skip when creating web pages, can be the reason your content isn't served in Google Search Results.

## Serving search results

Based on all the data GoogleBot collected and is indexed, depending on what users search, Google will determine what results are the highest quality and most relevant to the user's query. Relevancy is determined by hundreds of factors, which could include information such as the user's location, language, and device (desktop or phone). For example, searching for "bicycle repair shops" would show different results to a user in Paris than it would to a user in Hong Kong.

Based on the user's query the search features that appear on the search results page also change. For example, searching for "bicycle repair shops" will likely show local results and no image results, however searching for "modern bicycle" is more likely to show image results, but not local results.

Photo by [Edho Pratama](https://unsplash.com/@edhoradic?utm_content=creditCopyText&utm_medium=referral&utm_source=thedigitalblog) on [Unsplash](https://unsplash.com/photos/smartphone-showing-google-site-yeB9jDmHm6M?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash).