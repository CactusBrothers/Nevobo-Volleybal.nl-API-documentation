# Nevobo-Volleybal.nl-API-documentation
Unofficial API documentation for the Nevobo (Nederlandse Volleybal Band) website and the Volleybal.nl website. These 2 websites are linked, using the same club codes for example. If you want to add anything to this repo, please make a pull request!

As stated in https://www.nevobo.nl/nieuwsbericht/2016/09/07/competitiegegevens-voor-clubwebsites, nevobo has some urls for club managers to use on club sites and they are planning to add a full api support in the future but they are not working on it currently. However, these provided links are limited and confusing if you're just starting out. In this repo I will document these urls, as well as some extra urls I found (some urls are unofficial and might change in the future!).

## Official url's:
### **GET** https://api.nevobo.nl/export/poule/{regio}/{poule}/programma.{type}
**Url for getting the program of a poule**
regio: de regio waarin de poule plaatsvindt, ‘regio-noord’ ‘regio-oost’ ‘regio-zuid’ ‘regio-west’ ‘nationale-competitie’ ‘kampioenschappen’
poule: poule code, te vinden op volleybal.nl: ga naar een team, klik dan op
