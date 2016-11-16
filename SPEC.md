# DD1316-P-delen
#Specifikation

##Inledning
Jag har tänkt programmera ett enkelt datorspel som kan liknas med en variant av det klassiska ”Snake”. Flera spelare ska kunna spela spelet mot varandra men för den som inga kompisar har ska det även finnas ett enspelarläge där man utmanar datorn. Spelarnas huggormar placeras slumpmässigt ut på spelplanen och tar därefter turer om att bli tilldelade en slumpartad matranson på en, två, eller tre grodlår och spelaren får därefter välja åt vilket håll dennes huggorm skall växa (ett steg per grodlår). Förlorar gör man om man går in med sin orm i någon annans orm, alternativt om man inte har möjlighet att växa åt något håll. 
För att detta relativt enkla men hysteriskt roliga spel ska bli till verklighet måste en del utmaningar överkommas. Det kan bli knepigt att få det grafiska gränssnittet att se riktigt bra ut men den största svårigheten kommer troligtvis ligga i att få spelet att vara anpassningsbart för att kunna tillfredsställa även de största kompisgäng. Fokus måste därmed hållas stenhård på att alla programmets komponenter är dynamiska och fungerar oberoende av antalet spelare som kan tänkas vilja vara med på det roliga.

##Användarscenarier
###Spel mot datorn
Osquar har tråkigt på föreläsningen i linjär algebra. Detta är visserligen ingen nyhet men vad som däremot är nytt är hans nyligen införskaffade spel Hungriga Huggormar! Med vänster hand slänger Osquar anteckningsblock, pennskrin, och förmodligen även sin framtida karriär som ingenjör ned från bänken och med höger hand hivar han i samma veva upp sin dator. Osquar hoppar direkt in i enspelarläget och utmanar datorn för att se vem som svänger smidigast med sin huggorm. Osquar och datorns nykläckta huggormar placeras slumpmässigt ut på spelplanen och Osquar är så fascinerad av spelets magnifika grafik att han kunde trott att han var i paradiset och inte på teknis, om det nu ens finns en skillnad mellan dessa två. Osquar har mycket tur och får många stora ransoner grodlår, vilket leder till en spektakulär vinst mot datorn som inte ens är nära på att ha en huggorm som är lika lång, slank och otrasslig som Osquars. Vips var det dags för Osquar att ta sig till nästa föreläsning!

###Spel med kamrater
Osquldas plan om en trevlig tjejmiddag gick i stöpet då hon insåg att hon inte hade några billyspizzor i frysen. Med kompisarna redan på väg till Osquldas så kallade studentlägenhet behövde hon tänka fort för att klara sig med sin heder i behåll. Underst i högen med reklamutskick ser hon en annons om ett oändligt roligt datorspel, Hungriga Huggormar! Hon tänker att detta kanske kan vara hennes chans att rädda kvällen och startar upp sin dator och i samma sekund som hennes kamrater knackar på dörren startar hon upp spelet. Osqulda och hennes kompisar sätter sig runt soffbordet, klickar på flerspelarläget, matar in att fyra teknologer önskar deltaga, och sedan börjar de genast spela. . Tjejerna jagar varandra med sina imaginära huggormar långt in på morgontimmarna och när de sedan ligger helt utslagna tänker de att det var en natt de aldrig kommer glömma.

##Kodskelett
```
class spel(object):
    """Hela spelet utgår från huvudklassen spel."""
    def enSpelare
```

##Programflöde

Programmet börjar med att ett objekt av antingen **enspelarläge** eller **flerspelarläge** skapas beroende på hur många det är som önskar spela spelet. Därefter anropas metoden *skapaSpelplan* som tillhör överklassen **spel**. Med hjälp av metoden *ritaOrm*, som anropas en gång per spelare (inklusive datorn), placeras alla spelares nykläckta små ormar slumpmässigt ut på spelplanen. 



