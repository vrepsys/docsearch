---
title: Scraper Overview
---

## How?

The DocSearch scraper is written in Python and heavily inspired by the [Scrapy](https://scrapy.org/) framework. It goes through all pages of your website and extracts content from the HTML structure to populate an Algolia index.

It automatically follows every inter nal link to make s ure we are not missing any content, and uses the semantics of your HTML structure to construct its records. This means that `h1`,`h2`, etc., (`selectors`) titles are used as hierarchy, and each `p` is used as a potential result.&#x20;

Those CSS selectors can be overwritten, and each website has its own JSON configuration file that describes in more detail how the scraper should behave. You can find the complete list of options in [the related section](/docs/legacy/config-file).

If you'd like to [run DocSearch on your own](/docs/legacy/run-your-own), all the code is open sourced and even packaged as a Docker image. Download it, and run it with your own credentials.
