# Oefening-Cocoapods-0

In deze oefening maak je gebruik van **Cocoapods**, **AFNetworking** en **Grand Central Dispatch**.

## Tips
1. Zorg ervoor dat je lokale server runt:
  - Open de `Terminal` applicatie.
  - Gebruik het commando `cd` om te navigeren naar jouw `.json` file.
  - Voer het commando `json-server file.json --watch` uit.
2. De JSON server draait steeds op: **http://localhost:3000**
3. Als je manueel de JSON file aanpast, moet je soms de JSON server herstarten. Gebruik `CTRL+C` om te stoppen en `↑` om het vorige commando op te roepen.

## Opgaves
1. Maak een nieuw project aan voor deze oefening.
2. Maak een `.json` file aan en vul deze met enkele objecten. Aan jou de keuze ;-) Plaats de file in de folder **project_naam/project_naam**.
3. Configureer Cocoapods:
  - Open de `Terminal` applicatie.
  - Gebruik het commando `cd` om te navigeren naar jouw project. Zorg ervoor dat je in de folder **project_naam** zit, op het niveau van het Xcode project (dit is het bestand met de extensie `.xcodeproj`).
  - Voer het commando `pod init` uit. Dit commando maakt voor jou de Podfile aan.
  - Open de Podfile en voeg de pod `AFNetworking` toe. Gebruik de slides indien nodig.
  - Voer het commando `pod install` uit.
  - Sluit nu het Xcode project. Vanaf nu open je altijd de **workspace** i.p.v. het project. Open alvast de workspace.
  - De pod is nu ter beschikking zoals eender welke andere klasse. Voeg dus waar nodig de header files in om van start te gaan.
4. Maak een subklasse aan van de klasse `AFHTTPSessionManager`. Deze klasse zal alle requests naar de web service voor jou verrichten. Maak in deze klasse gebruik van de volgende methodes:
  - `GET:parameters:success:failure:` om een Get request te versturen
  - `POST:parameters:success:failure:` om een POST request te versturen
  - `PUT:parameters:success:failure:` om een PUT request te versturen
  - `DELETE:parameters:success:failure:` om een DELETE request te versturen
5. De subklasse van `AFHTTPSessionManager` is verantwoordelijk voor volgende zaken:
  - Het parsen van de response van de web service: wanneer de request voltooid is moet je de response omvormen tot objecten van jouw model. Maak dus de nodige modelklassen aan en tover de response om tot een **(NSArray *)** van jouw objecten.
  - Het verwittigen wanneer klaar: wanneer de request voltooid is en het parsen gebeurd is, dient deze klasse dit aan te geven. Schrijf zelf een delegate protocol om zo aan te geven dat de resultaten beschikbaar zijn.
6. Voeg een `UITableViewController` toe aan het storyboard, schrijf je eigen subklasse hiervoor en connectere deze.
7. Geef in deze `UITableViewController` de resultaten van de request weer.
8. Breid jouw model uit en voeg een relatie toe. Bijvoorbeeld: je bouwt een app om hotels te bekijken, voeg reviews toe per hotel.
  - Maak de nodige aanpassingen aan jouw `.json` file.
  - Maak de nodige modellen aan.
  - Breid de functionaliteit van jouw subklasse van `AFHTTPSessionManager` uit om dit te download, te parsen, etc.
9. Zorg ervoor dat je in de app nieuwe elementen van jouw model kan toevoegen.
  - Je zult dus ook gebruik moeten maken van de juiste web service om deze aanpassing door te voeren naar jouw database.
10. Zorg ervoor dat je in de app bestaande elementen van jouw model kan aanpassen.
  - Je zult dus ook gebruik moeten maken van de juiste web service om deze aanpassing door te voeren naar jouw database.

## Oplossing
De oplossingen vind je terug onder de repository **Demo-Cocoapods**.
