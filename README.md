# Oefening-Cocoapods-0
## Tips
No tips so far -_-

## Opgaves
1. Maak een nieuw project aan voor deze oefening.
2. Configureer Cocoapods:
  - Open de `Terminal` applicatie.
  - Gebruik het commando `cd` om te navigeren naar jouw project. Zorg ervoor dat je in de folder **project_naam/project_naam** zit.
  - Voer het commando `pod init` uit. Dit commando maakt voor jou de Podfile aan.
  - Open de Podfile en voeg de pod `AFNetworking` toe. Gebruik de slides indien nodig.
  - Voer het commando `pod install` uit.
  - Sluit nu het Xcode project. Vanaf nu open je altijd de **workspace** i.p.v. het project. Open alvast de workspace.
  - De pod is nu ter beschikking zoals eender welke andere klasse. Voeg dus waar nodig de header files in om van start te gaan.
3. Maak een subklasse aan van de klasse `AFHTTPSessionManager`. Deze klasse zal alle requests naar de web service voor jou verrichten. Maak in deze klasse gebruik van de volgende methodes:
  - `GET:parameters:success:failure:` om een Get request te versturen
  - `POST:parameters:success:failure:` om een POST request te versturen
  - `PUT:parameters:success:failure:` om een PUT request te versturen
  - `DELETE:parameters:success:failure:` om een DELETE request te versturen
4. De subklasse van `AFHTTPSessionManager` is verantwoordelijk voor volgende zaken:
  - Het parsen van de response van de web service: wanneer de request voltooid is moet je de response omvormen tot objecten van jouw model. Maak dus de nodige modelklassen aan en tover de response om tot een **(NSArray *)** van jouw objecten.
  - Het verwittigen wanneer klaar: wanneer de request voltooid is en het parsen gebeurd is, dient deze klasse dit aan te geven. Schrijf zelf een delegate protocol om zo aan te geven dat de resultaten beschikbaar zijn.
5. Voeg een `UITableViewController` toe aan het storyboard, schrijf je eigen subklasse hiervoor en connectere deze.
6. Geef in deze `UITableViewController` de resultaten van de request weer.
