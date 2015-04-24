# ISO Country, Language, Currency and Region Data

I created this repo as I wanted just the minimal dataset to import into other projects. It is based on the raw data from the excellent NodeJS project [OpenBookPrices/country-data](https://github.com/OpenBookPrices/country-data), is provided with the same [LICENSE](LICENSE.txt) and features the following changes:

- CSV files have been [CSV-linted](http://csvlint.io/) and reformatted to 'Standard CSV'
- The files have all been [JSON-linted](http://jsonformatter.curiousconcept.com/) and re-formatted slightly.
- Added [minified](http://www.httputility.net/json-minifier.aspx) (.min.json) version of each JSON file
- `regions.js` has been compiled into JSON and flattened down to 1 level
- `regions.js` has a new entry 'eurozone' for countries using the EURO (€)

**Note** that there is intentionally no regions.csv file.

## Countries

The data currently provided for each country is:

  * `name` The english name for the country
  * `alpha2` The [ISO 3166-1 alpha 2](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) code
  * `alpha3` The [ISO 3166-1 alpha 3](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-3) code
  * `status`: The ISO status of the entry: either 'assigned' or 'reserved'.
  * `currencies` An array of [ISO 4217 currency codes](http://en.wikipedia.org/wiki/ISO_4217) with the primary one first
  * `languages` An array of [ISO 639-2](http://en.wikipedia.org/wiki/ISO_639-2) codes for languages (may not be complete).
  * `countryCallingCodes` An array of the international call prefixes for this country.
  * `ioc` The [International Olympic Committee country code](http://en.wikipedia.org/wiki/List_of_IOC_country_codes)

## Regions

Countries are ofter grouped into regions. The list of regions is by no means exhaustive, pull requests very welcome for additions.

  * `countries` An array of `alpha2` codes for the countries in this region.

## Currencies

It is not that useful to just have the currency code(s) for a country, so included is currency data too:

  * `name` The english name for the currency
  * `code` The [ISO 4217](http://en.wikipedia.org/wiki/ISO_4217) code
  * `number` The [ISO 4217](http://en.wikipedia.org/wiki/ISO_4217) number
  * `decimals` The number of decimal digits conventionally shown

## Languages

A list of languages provided by [ISO 639-2](http://en.wikipedia.org/wiki/ISO_639-2);

  * `name` The english name for the language
  * `alpha2` The two letter [ISO 639-1](http://en.wikipedia.org/wiki/ISO_639-1) code for the language (may be blank).
  * `alpha3` The three letter terminological [ISO 639-2](http://en.wikipedia.org/wiki/ISO_639-2) code for the language (may be blank).
  * `bibliograpic` The three letter bibliographic [ISO 639-2](http://en.wikipedia.org/wiki/ISO_639-2) code for the language (may be blank).
