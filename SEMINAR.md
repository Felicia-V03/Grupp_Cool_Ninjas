# AI Frågorna

## 01
### Be ChatGPT och AIZO att applicera de fyra datalogiska delprocesserna på tärningsspelet Stegen från veckans övningskompendium. Skiljer sig svaren åt, och isåfall på vilket/vilka sätt?
Vi ser ingen skillnader.

## 02
### Be ChatGPT och Aizo att utifrån sina skapade flödesscheman även skapa pseudokod för spelet. Ser båda svaren likadana ut, eller hur skiljer de sig åt? Klista in ett av svaren och skriv från vilken tjänst lösningen kommer från.
Tänka på hur vi kan bryta ner problemet:
- Tärningskastet: Vi behöver en funktion som simulerar ett tärningskast och returnerar ett värde mellan 1 och 6.
- Mål och stege: Vi börjar med att försöka få en 1, sedan en 2, osv. tills vi når 6.
- Räkna kast: Håll koll på antalet kast som krävs för att nå varje siffra i stegen.
- Här är lite pseudokod för att komma igång:
- Skapa en funktion rollDice som returnerar ett slumpmässigt tal mellan 1 och 6.
- Initiera en variabel currentGoal till 1 (målet vi försöker nå).
- Initiera en variabel rollsCount till 0 (för att räkna antalet kast).
- Medan currentGoal är mindre än eller lika med 6:
- Kasta tärningen och öka rollsCount.
- Om resultatet är lika med currentGoal, öka currentGoal med 1.
- När loopen är klar, skriv ut rollsCount.

```
// Funktion för att simulera ett tärningskast
function rollDice() {
    // Returnera ett slumpmässigt tal mellan 1 och 6
}

// Variabel för att hålla reda på nuvarande mål
let currentGoal = 1;

// Variabel för att räkna antalet kast
let rollsCount = 0;

// Loop tills vi når mål 6
while (currentGoal <= 6) {
    // Kasta tärningen
    // Öka rollsCount

    // Om tärningskastet är lika med currentGoal
        // Öka currentGoal med 1
}

// Skriv ut antalet kast
```

## 03
### Be ChatGPT och Aizo att fixa den färdiga JavaScript-koden för spelet, samt att logga ut kontroller och resultat i konsollen. Testa koden i det medskickade programmet om det fungerar och redovisa resultat.
#### ChatGPT
```
// Funktion för att kasta en tärning och returnera ett nummer mellan 1 och 6
function rollDice() {
  return Math.floor(Math.random() * 6) + 1;
}

// Funktion för att spela spelet
function playDiceGame() {
  let target = 1;  // Målet börjar på 1 och går upp till 6
  let rollCount = 0;  // Räknare för antalet kast

  console.log("Spelet börjar! Målet är att få tärningarna i ordning: 1, 2, 3, 4, 5, 6");

  // Loop för att kasta tärningen tills vi når 6
  while (target <= 6) {
    let rollResult = rollDice();  // Kasta tärningen
    rollCount++;  // Öka kast-räknaren
    
    console.log(`Försök ${rollCount}: Du fick en ${rollResult}.`);  // Logga resultatet av varje kast

    // Kolla om vi fick rätt resultat för det aktuella målet
    if (rollResult === target) {
      console.log(`Grattis! Du fick rätt resultat: ${target}. Nu går vi vidare till nästa nummer.`);
      target++;  // Gå vidare till nästa mål (från 1 till 6)
    } else {
      console.log(`Tyvärr, inte rätt. Försök igen.`);
    }
  }

  console.log(`Spelet är klart! Totalt antal kast: ${rollCount}.`);
}

// Starta spelet
playDiceGame();
```
Så här se reslutat ut
```
Spelet börjar! Målet är att få tärningarna i ordning: 1, 2, 3, 4, 5, 6
Försök 1: Du fick en 4.
Tyvärr, inte rätt. Försök igen.
Försök 2: Du fick en 1.
Grattis! Du fick rätt resultat: 1. Nu går vi vidare till nästa nummer.
Försök 3: Du fick en 3.
Tyvärr, inte rätt. Försök igen.
Försök 4: Du fick en 2.
Grattis! Du fick rätt resultat: 2. Nu går vi vidare till nästa nummer.
Försök 5: Du fick en 6.
Tyvärr, inte rätt. Försök igen.
Försök 6: Du fick en 4.
Tyvärr, inte rätt. Försök igen.
Försök 7: Du fick en 3.
Grattis! Du fick rätt resultat: 3. Nu går vi vidare till nästa nummer.
Försök 8: Du fick en 5.
Tyvärr, inte rätt. Försök igen.
Försök 9: Du fick en 4.
Tyvärr, inte rätt. Försök igen.
Försök 10: Du fick en 2.
Tyvärr, inte rätt. Försök igen.
Försök 11: Du fick en 5.
Tyvärr, inte rätt. Försök igen.
Försök 12: Du fick en 6.
Tyvärr, inte rätt. Försök igen.
Försök 13: Du fick en 1.
Grattis! Du fick rätt resultat: 1. Nu går vi vidare till nästa nummer.
```


## 04
### Hur tror ni att ChatGPT och Aizo skulle lösa större och mer komplicerade kodproblem? Var någonstans går gränsen tror ni för vilken typ av uppkodning där det skulle börja uppstå problem?

#### ChatGPT
Vi tror att Chat GPT kan lösa komplicerade kodproblem, eftersom Chat GPT har utvecklat hela tiden och den en av de största AI-tjänst nu för tiden. 
#### Aizo
Vi tror att Aizo är uppbyggd med en begränsad vilkor eller funktioner som just nu har hen mest fokus i områden såsom HTML, CSS, UX, UI, Figma, JavaScript och datalogiskt tänkande.

## 05
### Klistra in nedanstående CSS och be ChatGPT och Aizo att förklara vad som händer.
### box-shadow: 12px 12px 2px 1px rgba(0, 0, 255, .2);

#### ChatGPT
Den här CSS-regeln applicerar en box-shadow på ett element. Här är en förklaring av varje del i regeln:
box-shadow: 12px 12px 2px 1px rgba(0, 0, 255, .2);
- 12px (horisontell förskjutning): Detta betyder att skuggan kommer att vara förskjuten 12 pixlar åt höger från elementet. Om värdet var negativt (t.ex. -12px), skulle skuggan förflyttas åt vänster.
- 12px (vertikal förskjutning): Här är skuggan förskjuten 12 pixlar nedåt från elementet. Ett negativt värde (t.ex. -12px) skulle göra att skuggan går uppåt istället.
- 2px (oskärpa, blur): Detta värde bestämmer hur mycket skuggan ska vara oskarp eller suddig. Ju större värde desto mer suddig blir skuggan. Här är den relativt liten (2px), så skuggan kommer att vara ganska skarp.
- 1px (spridning, spread): Detta värde justerar storleken på skuggan. Ett positivt värde gör att skuggan blir större än elementet, medan ett negativt värde minskar dess storlek. Här är spridningen satt till 1px, vilket gör att skuggan är något större än elementet.
- rgba(0, 0, 255, .2) (färg på skuggan): Färgen på skuggan anges med rgba, där:
0, 0, 255 är den blå färgen (RGB = röd, grön, blå; i detta fall är det rent blått).
.2 är alfa-värdet som styr transparensen (0 är helt genomskinligt, 1 är helt opakt). Här innebär .2 att skuggan är 20% opak, så den kommer vara ganska transparent.

Sammanfattning
Den här CSS-regeln skapar en blå, något suddig skugga som är förskjuten 12 pixlar både åt höger och ner, med en liten spridning och låg transparens (20% opak). Skuggan är alltså subtil och mjuk men synlig, och ger ett intryck av djup och dimension.

#### Aizo
Det ser ut som du är intresserad av CSS och specifikt box-shadow!   Den kod du har där är en box-shadow-regel som används för att lägga till en skugga runt ett element. Låt oss bryta ner vad varje del av värdet betyder:
- 12px - Detta är den horisontella offseten. Skuggan kommer att flyttas 12 pixlar åt höger.
- 12px - Detta är den vertikala offseten. Skuggan kommer att flyttas 12 pixlar neråt.
- 2px - Detta är oskärpan (blur radius). Ju större värde, desto mer suddig blir skuggan.
- 1px - Detta är spridningsradien (spread radius). Ett positivt värde ökar skuggans storlek medan ett negativt minskar den.
- rgba(0, 0, 255, .2) - Detta är skuggans färg, i detta fall blå med 20% opacitet.
Om du vill experimentera med box-shadow, vad skulle hända om du ändrar oskärpan eller spridningsradien? Testa och se vad som händer!

#### Vilka språkliga skillnader, om det finns några, kan ni se?
Både ChatGPT och Aizo förklara ganska lika på vad de betyder och vart det är men i ChatGPT förklara de även hur kan man också använda. Så Aizo förklara på den enkel sätt och ChatGPT förklara också på enkel men visa också hur kan man använda mer av koden.

## 06
### Klista in följande prompt i ChatGPT
Vi tror att AI eller ChatGPT generellt är lite utdaterad eller inte är så uppdaterad på de senaste reglerna och rekommendationerna som kommer och ändras ofta. Därför finns det en risk att AI föreslår utdaterade funktioner som vi egentligen inte bör använda längre, som den gör i det här fallet. 
Den är heller inte medveten om att det är utdaterad, och man måste tänka mer kritiskt och inte alltid ta svaren AI:n ger som 100% sanning.  
ChatGPT föreslår först en ändring och lägger också till ett "promise" längre ner i koden. Alla tre förslagen är helt lika varandra, alla tre har "promise".

## 07
### Be ChatGPT att beskriva skillnaderna mellan begreppen pattern recognition och abstraction, samt att ge exempel. Klicka därefter på er profilbild uppe i det högra hörnet, och välj därefter alternativet Anpassa ChatGPT.
Efter hade jämförat på resultatet av sökningen på två olika profiler ansåg vi att Chat GPT valde språknivå på två olika sätt vilken passar till olika profilen. Det är lättare begreppet och exempel i den andra frågan.

## 08
### Kan du skapa en funktion som tar emot ett ord och returnerar ordet med en stor bokstav i början, samt efter alla mellanslag och bindestreck?

```
function capitalizeWords(input) {
    return input.replace(/(?:^|[\s-])\S/g, function(match) {
        return match.toUpperCase();
    });
}

// Exempelanvändning
console.log(capitalizeWords("hej världen")); // Output: "Hej Världen"
console.log(capitalizeWords("detta-är-en-test")); // Output: "Detta-Är-En-Test"
console.log(capitalizeWords("fler exempel här")); // Output: "Fler Exempel Här"
```

### Kan du skapa en funktion som tar emot ett ord och returnerar ordet?
Om du bara vill ha en funktion som returnerar ett ord utan någon särskild manipulation kan vi skapa en enkel funktion som tar emot ett ord och returnerar det som det är:

```
function returnWord(word) {
    return word;
}

// Exempelanvändning
console.log(returnWord("hej")); // Output: "hej"
console.log(returnWord("världen")); // Output: "världen"
```

## 09
### I vilka scenarion kan ni som studenter känna att det är okej att be AI om hjälp? Och i vilka scenarion är det inte okej?

#### Det är okej:
- Att få råd, som studiehjälp, ideer eller du kan fråga om ting du funderar på eller du kan använda AI:n att lära nya saker. 
- Få hälp med lösa vissa problemer, om koden  inte  fungerar och du inte hittar vad som är fel, det kan hända att du har jobbat länge og du blir “blind”, du ser kanske inte problemer när du är trött till exempel, då er AI ett bra verktyg för att “se” bättre eller få bettre koll igen. 
- Att få tydligare förklaringar på vissa komplexa frågor, exemplevis om du undrar om python och JavaScript kan jobba tillsammans eller inte? och hur fungerar det? 
- Kan få hjälp av förklaringar som anpassar till kundskap nivå för både ämnet och språket, och om du inte förstår så kan du be AI:n om att omformulera, eller om du hittar en svårläst artikkel så kan du be AI:n om att skriva det på ett sätt som du själv förstår. 
- Det kan spara mycket tid - att söka, scrolla, leta och läsa på nätet kan ta extremt mycket tid, med en AI kan du fråga direkt, be den att svare bara på det du behöver hjälp med, utan at du måste använda mycket tid på att läsa orelevanta saker. 
- Tilgängelighet: för personer som har svårt att läsa, fokusera eller tappar fokus lätt, är AI:n ett bra verktyg för att göra ting lättare att läsa, kanske kan AI:n korta ner texten, eller du kan tilpassa svaren på sett som du själv behöver.  
#### Det är inte okej:
- Lösa hela uppgifter, du lär dig inte, du forstår kanske inte vad den gör, och du kan inte argumentera för varför du valde just den koden. 
- Koda upp allt åt dig, det blir lättare problemer och konflikter senare om du skulle ändra nonting. Om AI:n har löst problemet åt dig, så blir det jättesvårt att gå tillbaka för att lösa det, samtidigt blir kanske inte resultatet helt som du hade önskad när du inte gör det själv. 
- Klistra in förslag utan att veta vad det betyder eller vad koden gör. Gör research och be AI:n lära dig vad koden innebär, eventuelt googla eller använd andra sidor.

## 10
### Förutom att åka dit för fusk, diskutera vilka de tre största riskerna för er som studenter är att använda er av AI verktyg för att lösa era uppgifter. 
- Kreativitet förminskar och man förlorar förmågan att tänka själv, när man inte tänker själv så blir det mer och mer svårt att tänka efter ett tag.  Ju mer man använder hjärnan själv, desto lättare blir det att tänka, då är det viktigt att man kommer på ideer själv och inte använda AI för mycket. 
- Problemlösning/debugging förmågan blir sämre pågrund av man frågar AI som Aizo och ChatGPT för att lösa problemen istället söka lösningar själv eller tänka själv. 
- Källkritik blir sämre, man lär sig kanske att lita “direkt” på AI, och svaren man får från en AI kan vara utdaterad eller fel, det är viktigt att man tänker kritisk, även om AI:n låter självsäker. 
- Man lär sig inte att koda själv, och man lär sig inte att forstå vad koden faktiskt betyder och vad den gör om man bara tar lösninger från AI, specielt om man aldrig frågar vad lösningen betyder.

## 11
### Vilka styrkor och svagheter / risker ser ni hos Github Copilot för er som studenter?
#### Styrkor:
- Ta mindre tid att lösa uppgifter med hjälp av kodnings förslaget. 
- Kan hitta nya tekniker för att lösa ett problem.  
#### Svagheter / Risker:
- Lärdom försämras då man inte gör/skriver det själv, eller hittar på lösningarna själv.
- Lompetens / färdigheter församras.
- Kan minska din förmågan att problemslösa. 
- Du blir berorende på AI när du använder den för ofta, du orkar kanske inte tänka själv.

## 12
### Kan ni se några scenarion för er som studerande där Github Copilot skulle vara okej att använda?
- Explanation av kod  Exempel om du jobbar i ett projekt tillsammans med flera utvecklare och dina kollegor använder en funktion/ språk som du är ovan med och du vill inte fråga eller har inte tid att leta runt för att reda ut vad är det för funktion och hur den fungra. då AI kan vara bra alternativ för hjälpa dig nu. Fördelar är att du sparar tid och får snabb klaringar direkt.
- Har fått en bugg och hur ska man lösa den. - Den kan ge oss kodförslag på hur ska man lösa bugg eller problem.

## 13
### Vad tycker ni verkar vara mest "najs" med Github Copilot?
Copilot kommer med kodning förslag, fungerar lite som parprogrammering som kan hjälpa oss att vara mer effektiv i vår kodning 
Gör det lättare att “starta hjärnan” och komma på flera ideer om man inte har ideer från början 
Olika “brushes” med olika funktioner, till exempel “custom” brush, där man kan skriva /prompta vad den exakt ska göra

## 14
### Hur ser ni på våra roller som utvecklare i framtiden, där vissa oroliga röster höjs inför hotet om AI som skall ta över våra jobb på lång sikt? 
- Vi tror att junoir fontendtvecklare kan vara svårare att få job pågrund av företaget använder mer AI för att lösa de komplexa problem och samtidig kan minska personalkostnader i form av företaget har mindre behov av nya anställda i de små och mellan stora företag.
- På andra sida kan vara positiv att AI är ju ett verktyg som kan hjälpa oss och lära oss på nya saker och teknik. När man kommer ut till arbetliv betyder att vi är redo att anpassa oss till de verktygen som arbetsgivare använder i sitt företag. Samtidig förstår vi hur man använder AI mer försvarligt.

## 15
### Vilka risker ser ni med att använda sig av AI som en källa för kodskrivande i yrkeslivet?
Man blir beroende på AI och det kan leda till att sina färdigheter blir minskad. 
Man bidrar till att sprida ett problem: att man själv använder AI för att arbeta kanske gör att andra också börjar göra det. Om det sprider sig för mycket kommer vi så småningom att ha programmerare som inte programmerar särskilt mycket själva, utan snarare "promptare" på arbetsmarknaden. Vi gör det mer accepterat att använda AI istället för att tänka själv.

## 16
### Vilka andra AI tjänster kan vara relevanta för oss utvecklare att känna till och använda oss utav. Leta reda på 3 tjänster och skriv 3-4 menigar om vardera.
#### Codepal
Det kan man får hjälp med koder i flera olika språker samt kan också skapa upp koden åt oss. Ganska lätt att använda bara välja språken och kommando på vad ska de skapa för kod.
#### Replit GhostWriter
Den här AI vertyg är ganska ny men se också lätt att använda. Den kommer hjälpa till med förklara koden och ge råd. Den kan skriva hela koden också. Men den fungera bara i Replit som är deras program så den kan inte använda i Visual Studio Code så den kan vara nackdelen.
#### Codeium
Den se väldigt lätt att använda och kan använda ganska till många problem eller med koder. Codeium kan både ger råd eller hjälpa till med  skriva upp hela koden. Kan koppla direkt med Visual Studio Code som underlätt vi som kodar att öppna flera AI program när man ska kodar.

## 17
### Av de verktyg som ni letat upp samt de som tagits upp i tidigare frågor, vilket tror ni att ni skulle ha mest användning av i er roll som studerande, samt i er yrkesroll? Motivera!
- Att söka efter fakta och refereser för att stödja ditt projekt.
- ChatGPT är integrerad inuti Copilot, samtidigt som vi också har ChatGPT chatten, och vi har mycket erfaring med ChatGPT och tror att dissa verktyg vill fortsätta att vara till stor hjälp/stöd för oss. ChatGPT är ett flexibelt verktyg som kan används på många områden, och eftersom det fortsättar utveckla sig, är vi säker på att det vill stödja oss mer senare.
