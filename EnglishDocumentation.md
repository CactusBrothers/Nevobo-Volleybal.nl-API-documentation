# **WIP**
# Nevobo-Volleybal.nl-API-documentation
Unofficial API documentation for the Nevobo (Nederlandse Volleybal Band) website and the Volleybal.nl website. These 2 websites are linked, using the same club codes for example. If you want to add anything to this repo, please make a pull request!

As stated in https://www.nevobo.nl/nieuwsbericht/2016/09/07/competitiegegevens-voor-clubwebsites, nevobo has some urls for club managers to use on club sites and they are planning to add a full api support in the future but they are not working on it currently. However, these provided links are limited and confusing if you're just starting out. In this repo I will document these urls, as well as some extra urls I found (some urls are unofficial and might change in the future!).

## Official url's:
### **GET** https://api.nevobo.nl/export/poule/{regio}/{poule}/programma.{type}
**Url for getting the program of a poule**

* regio - the region of the poule: ‘regio-noord’ ‘regio-oost’ ‘regio-zuid’ ‘regio-west’ ‘nationale-competitie’ ‘kampioenschappen’.
* poule - poule code, present on volleybal.nl: go to the page of your team, then click export -> rss. This will open a link with region and code of the poule.
* type - the type of response: 'rss' 'xlsx' 'ics'

**Response**

Depending on the type provided in the url will the api return different formats:
* rss - XML format, containing a list of matches in the program.
* xlsx - Excel format, containing a spreadsheet with date, time, teams, location, field, region, poule, code, hallcode, hall, place, referees and status. This is more information than provided with rss!
* ics - Calendar format, conatain every match as event, to easily add to a calendar.

### **GET** https://api.nevobo.nl/export/poule/{regio}/{poule}/resultaten.{type}
**Url for getting the results of a poule (not standings!)**

* regio - the region of the poule: ‘regio-noord’ ‘regio-oost’ ‘regio-zuid’ ‘regio-west’ ‘nationale-competitie’ ‘kampioenschappen’.
* poule - poule code, present on volleybal.nl: go to the page of your team, then click export -> rss. This will open a link with region and code of the poule.
* type - the type of response: 'rss' 'xlsx' (not 'ics'!)

**Response**

Depending on the type provided in the url will the api return different formats:
* rss - XML format, containing a list of results in the poule.
* xlsx - Excel format, containing a spreadsheet with date, time, teams, location, field, region, poule, code, hallcode, hall, place, referees and status. This is more information than provided with rss!
* ics - Calendar format, conatain every match as event, to easily add to a calendar.

## TODO:
1. add file with all club and team codes
2. add program to get poule code from teamcode
