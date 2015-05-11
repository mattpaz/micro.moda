+++

date = "2015-04-25"
draft = false
title = "Next Steps"
slug = "todo"
comments = true
summary = "next steps for this site"

series = [ "About this site" ]

+++

Some of my to do items include ...
<!--more-->


## Things to Fix
* http://localhost:1313/snapshots/edu/www.njcu.edu/
* http://localhost:1313/snapshots/edu/www.ollusa.edu/
* http://localhost:1313/snapshots/edu/www.shawuniversity.edu/
* http://localhost:1313/snapshots/edu/www.nyu.edu/
* http://localhost:1313/snapshots/edu/www.stcl.edu/
* http://localhost:1313/snapshots/edu/www.potsdam.edu/
* http://localhost:1313/snapshots/edu/www.snhu.edu/
* http://localhost:1313/snapshots/edu/www.sbuniv.edu/
* http://localhost:1313/snapshots/edu/www.newrk.rutgers.edu/
* http://localhost:1313/snapshots/edu/www.salem.kent.edu/
* http://localhost:1313/snapshots/edu/www.okcu.edu/
* http://localhost:1313/snapshots/edu/www.odu.edu/
* http://localhost:1313/snapshots/edu/www.bgsu.edu/

## Things to Link to
* http://www.ipv6matrix.org/domain-mit.edu
* http://dnsviz.net/d/mtsu.edu/dnssec/

## Vocabs
* Validation (Valid|Invalid|Unknown)
* Technology Taxonnomy?  
 * __http headers__
  * x-generator
  * x-powered-by
  * server
  * via
  * set-cookie
 * __metatags__
  * generator
  * twitter:card
  * viewport
 * __json__
  * domain->ipv6



Related Links (via Alexa)
--------------------
* Add 'em in

Content Analysis
--------------------
* Word Count
* Paragraph Count
* Flesch Kincaid Reading Ease
* Gunning Fog Score
* Coleman Liau Index
* SMOG Reability Index
* Automated Reability Index

Link Analysis
--------------------
* Add data from my sifted index

Alexa Data
--------------------
* Alexa Speed: 891
* Alexa Links In: 60 429
* Alexa Reach: 1 897
* Alexa Popularity: 1 673



## Fine Tuning Hugo
Fine tuning this site by learning more about Hugo

* Front Matter
 * weight
 * summary - http://gohugo.io/content/summaries/
  * summary divider
* Sections = Types (but can be overriden)
 * List templates - can be overridden
 * By default, content is ordered by weight, then by date
 * http://gohugo.io/templates/list/
 * http://gohugo.io/templates/views/
* Taxoxnomies
 * Taxnonomy Templates - can be overridden
 * http://npf.io/2014/08/making-it-a-series/
 * http://gohugo.io/templates/terms/
 * http://gohugo.io/taxonomies/templates/
 * http://gohugo.io/taxonomies/displaying
 * http://gohugo.io/taxonomies/methods/
* Partials - http://gohugo.io/templates/partials/
* Menus - http://gohugo.io/extras/menus/
* Investigate Later
 * Pagination - http://gohugo.io/extras/pagination/
 * Scoping & Scratch - http://gohugo.io/extras/scratch/
 * Shortcodes - http://gohugo.io/extras/shortcodes/



## Data to Add
* json
 * basic
  * content->rss[] -
   * https://github.com/sdepold/jquery-rss  
   * http://stackoverflow.com/questions/22273907/use-jquery-to-read-a-json-google-news-feed
  * content->analysis->html->page_size


  * content->analysis->text->counts->word
  * content->analysis->text->counts->sentence
  * content->analysis->text->counts->avg_sentance_words
  * content->analysis->html->dom->body->hash
  * content->analysis->html->dom->counts->tags
 * image
  * content->analysis->html->links->rel->image_src

## Long Term ToDos and Wish List
As I get time, here are some of the things I hope to investigate next.

* __Google Custom Search__ - Integrate Search
 * https://developers.google.com/custom-search/docs/structured_data
* __Color Palette Extraction__ - Think about various techniques for extracting color palettes from screenshots
 * https://www.npmjs.com/package/thief
 * http://cloudinary.com/blog/api_for_extracting_semantic_image_data_colors_faces_exif_data_and_more
* __ApacheTika__ - I got started with processing pages before Tiki existed, but it could work a heckuva lot better for lots of things (for Open Graph & Twitter Card, etc in particular)
 * http://stackoverflow.com/questions/3711357/getting-title-and-meta-tags-from-external-website
 * https://github.com/pierroweb/PhpTikaWrapper
* __DFP__ - even if I don't use ads, I might use DFP for Small Business to support geospatial targeting of relevant snaphot
* __Before/After Comparisons__ - Once I start processing long term, provide before/after comparisons of screenshots
 * http://juxtapose.knightlab.com/
* __Elastic Search__ - Once I get things up and running, think about a faceted search supported by a hosted Elastic Search instance
* __SenderBase Processing__ - Grab Snapshots from SenderBase for additional info
 * http://stackoverflow.com/questions/14145886/how-to-programmatically-query-senderbase-org


<!--
## Siftr

* http://stackoverflow.com/questions/14145886/how-to-programmatically-query-senderbase-org

## Design
* http://www.ebpearls.com.au/our-work/
-->
