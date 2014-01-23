Data Catalogs
===============

This repo contains a JSON file of city, county and state data catalogs. We need help analyzing these data catalogs and adding more data catalogs.

### To help analyze a data catalog already in the JSON file:

Pick an entry in the JSON file.
Follow the url in an entry and take a look at the data.
Edit the JSON and add as many of the following fields as possible to the entry, after analyzing the data. All of these fields are optional, but the more included, the better.

    "catalog-name": <"text">,
    "machine-readable": <true,false>,
    "file-format": <["csv","json","doc"]>,
    "date-last-updated": <"yyyy-mm-dd">,
    "update-period": <"hourly","daily", "weekly" etc.>,
    "easy-to-use-by-3rd-party": <true, false>,
    "description": <"text">,
    "comments": <"text">

For example, say we have an entry in the json file that looks like this:

    {
      "place":"Canada",
      "url":"http://data.gc.ca/data/en/dataset/d666bc4a-d9b0-4b48-84de-dedb963716be",
      "fips-code":"99999999999"
    }

After looking at the data we end up with an entry that looks like this:

    {
      "place":"Canada",
      "url":"http://data.gc.ca/data/en/dataset/d666bc4a-d9b0-4b48-84de-dedb963716be",
      "fips-code":"99999999999",
      "catalog-name": "Police personnel and selected crime statistics, municipal police services",
      "machine-readable": "true",
      "file-format": ["csv", "xml"],
      "date-last-updated": "2013-05-29",
      "easy-to-use-by-3rd-party": "true",
      "description": "Contains numbers of male/female police officers, civilian personnel, officers eligible to retire and other department and crime statistics, broken down by municipality",
      "comments": "This data set is probably never updated"
    }

Once you have updated entries, submit a pull request.

### To add a data catalog to the JSON file:

Create a new entry in the JSON file with the required fields:

    {
      "place":<"text">,
      "url":<"text">,
      "fips-code":<"text">
    }

You can look up a fips code via [http://fips-lookup.herokuapp.com/](http://fips-lookup.herokuapp.com/).

Note: The fips code must be a string since some fips codes start with a zero.

Add as many of the optional fields as possible, listed in the previous section.
Submit a pull request.

Thank you so much for your help!