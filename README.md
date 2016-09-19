# Content-Scraper-Nodejs
This project is a Node.js command line application that goes to an ecommerce site to gets the latest prices and saves them to a spreadsheet (CSV format). This spreadsheet will be used by another application to populate a database.This applications uses npm modules.

An npm Package for Node.js using a third party npm package to scrape content from the site. 

This creates a csv file

The column headers Title, Price, ImageURL, URL and Time. 

The current date time of when the scrape happened e.g. 2016-01-29.csv. 


## Basic Usage

```javascript
var Scraper = require("content_scraper");

var url = "http://google.com";

var shirts4mikeScraper = new Scraper(url);

/**
* When the "end" event is triggered an array of article 
* metadata is returned
**/
shirts4mikeScraper.on("end", console.log);

/**
* If a parsing, network or HTTP error occurs an
* error object is passed in to the handler or callback
**/
shirts4mikeScraper.on("error", console.error);
```

### Example of Returned Data

```javascript
[
   {

   },
   {

   }
]

```

`title`, `price`, `url` and `imageURL` are `strings` and `time` is a JavaScript `Date` object.
