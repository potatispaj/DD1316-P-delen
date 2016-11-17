# DD1316-P-delen
#Specifikation

##Inledning
Jag har tänkt programmera ett enkelt datorspel som kan liknas med en variant av det klassiska ”Snake”. Flera spelare ska kunna spela spelet mot varandra men för den som inga kompisar har ska det även finnas ett enspelarläge där man utmanar datorn. Spelarnas huggormar placeras slumpmässigt ut på spelplanen och tar därefter turer om att bli tilldelade en slumpartad matranson på en, två, eller tre grodlår och spelaren får därefter välja åt vilket håll dennes huggorm skall växa (ett steg per grodlår). 

Förlorar gör man om man går in med sin orm i någon annans orm, alternativt om man inte har möjlighet att växa åt något håll. 
För att detta relativt enkla men hysteriskt roliga spel ska bli till verklighet måste en del utmaningar överkommas. Det kan bli knepigt att få det grafiska gränssnittet att se riktigt bra ut men den största svårigheten kommer troligtvis ligga i att få spelet att vara anpassningsbart för att kunna tillfredsställa även de största kompisgäng. Fokus måste därmed hållas stenhård på att alla programmets komponenter är dynamiska och fungerar oberoende av antalet spelare som kan tänkas vilja vara med på det roliga.

##Användarscenarier
###Spel mot datorn
Osquar har tråkigt på föreläsningen i linjär algebra. Detta är visserligen ingen nyhet men vad som däremot är nytt är hans nyligen införskaffade spel Hungriga Huggormar! Med vänster hand slänger Osquar anteckningsblock, pennskrin, och förmodligen även sin framtida karriär som ingenjör ned från bänken och med höger hand hivar han i samma veva upp sin dator. Osquar hoppar direkt in i enspelarläget och utmanar datorn för att se vem som svänger smidigast med sin huggorm. Osquar och datorns nykläckta huggormar placeras slumpmässigt ut på spelplanen och Osquar är så fascinerad av spelets magnifika grafik att han kunde trott att han var i paradiset och inte på teknis, om det nu ens finns en skillnad mellan dessa två. Osquar har mycket tur och får många stora ransoner grodlår, vilket leder till en spektakulär vinst mot datorn som inte ens är nära på att ha en huggorm som är lika lång, slank och otrasslig som Osquars. Vips var det dags för Osquar att ta sig till nästa föreläsning!

###Spel med kamrater
Osquldas plan om en trevlig tjejmiddag gick i stöpet då hon insåg att hon inte hade några billyspizzor i frysen. Med kompisarna redan på väg till Osquldas så kallade studentlägenhet behövde hon tänka fort för att klara sig med sin heder i behåll. Underst i högen med reklamutskick ser hon en annons om ett oändligt roligt datorspel, Hungriga Huggormar! Hon tänker att detta kanske kan vara hennes chans att rädda kvällen och startar upp sin dator och i samma sekund som hennes kamrater knackar på dörren startar hon upp spelet. Osqulda och hennes kompisar sätter sig runt soffbordet, klickar på flerspelarläget, matar in att fyra teknologer önskar deltaga, och sedan börjar de genast spela. Tjejerna jagar varandra med sina imaginära huggormar långt in på morgontimmarna och när de sedan ligger helt utslagna tänker de att det var en natt de aldrig kommer glömma.

##Kodskelett
```
spelarLista[] #varje element i denna lista är ett objekt av typen spelare
levandeSpelare[] #Initiellt en kopia av spelarLista, men elementen plockas bort allt eftersom spelarna dör

class spelKlass(object):
    #En klass med metoder för en- och flerspelarläge   
    def initialisering(antalSpelare, storlekSpelplan)
        """Ritar upp spelplanen utifrån värdet på parametern storlekSpelplan.
        Varje ruta på spelplanen lagras som ett objekt av ruta-klassen.
        Skapar lika många spelare-objekt som parametern antalSpelare anger.
    def ritaOrm(spelare, tillväxt):
        """Uppdaterar den aktuella spelarens orm på spelfältet."""
    def kontrolleraTillväxt(spelare, tillväxt, riktning = 0):
        """Ser till att önskat drag är tillåtet
        Kontrollerar ruta.ledig för den ruta som användaren vill gå till.
        Om ingen riktning matas in, alltså riktning = 0, kollar metoden
        om spelaren kan gå åt något håll över huvud taget.
        Returnerar True eller False"""
        
    def enspelarläge():
        """Slumpar ut spelarnas ormar och ritar upp dessa med hjälp av metoden ritaOrm.
        Därefter kommer en whileloop som loopar tills någon vinner.
            I början av varje iteration kontrolleras längden på listan levandeSpelare[].
            Om längden är 1 har någon vunnit och loopen avbryts. 
            Annars tar spelaren och datorn turer om att göra sina drag.
            För spelarens drag anropas tur(spelare)
            Sedan gör datorn sitt drag."""
        
    def flerspelarläge():
        """Slumpar ut spelarnas ormar och ritar upp dessa med hjälp av metoden ritaOrm.
        Därefter kommer en whileloop som loopar tills någon vinner.
            I början av varje iteration kontrolleras längden på listan levandeSpelare[].
            Om längden är 1 har någon vunnit och loopen avbryts. 
            Annars tar de levande spelarna turer om att göra sina drag. 
            Metoden tur(spelare) anropas för varje person
            Om tur returnerar false tas spelaren bort från listan levandeSpelare[]"""
        
    def tur(spelare):
        """Kollar, med hjälp av metoden kontrolleraTillväxt, om spelaren kan göra ett drag. 
        False --> Förlust, True --> Fortsätt
        Slumpar en matranson.
        Frågar åt vilket håll spelaren önskar gå.
        Anropar kontrolleraTillväxt. Om draget slutar i en katastrof "dör" spelaren.
        Efter genomfört drag anropas ritaOrm för att uppdatera grafiken.
        returnerar true eller false beroende på om spelarens orm avled eller inte"""
        
    def datorTur()
        """Algoritm för datorns drag.
        Grafiken uppdateras med ritaOrm
        Returnerar True eller False beroende på om datorn överlevde sitt drag."""

class spelare(object):
    """Varje spelare blir tilldelad ett spelare-objekt.
    Varje spelare-objekt har ett namn, färg, längd, status, mänsklig, samt
    position (vilket är platsen för ormens huvud, som ett ruta-objekt)"""

class ruta(object):
    def __init__(self, x, y):  #Varje ruta på spelplanen lagras som ett klassobjekt
        self.x = x
        self.y = y
        self.ledig = True
```

##Programflöde

Programmet börjar med att ett objekt av en av klasserna **enspelarläge** eller **flerspelarläge** skapas beroende på hur många det är som önskar spela spelet. Det första som händer därefter är att metoden *initialisering* som tillhör överklassen **spelKlass** anropas. Denna skapar först ett objekt av klassen **spelare** för varje mänsklig spelare och ritar därefter upp spelplanen med den storlek som anges i en separat fil. Med hjälp av metoden *ritaOrm*, som anropas en gång per spelare (inklusive datorn), placeras alla spelares nykläckta små ormar slumpmässigt ut på spelplanen.

Nu kan själva spelet börja. En loop går igenom alla spelare i tur och ordning och slumpar för varje spelare fram en matranson, låter spelaren välja åt vilket håll denne vill röra sig samt anropar metoden *ritaOrm* som uppdaterar spelplanen. Ifall det är endast en spelare som spelar anropas en annan metod varannan gång vilken ser till att "datorn" gör ett drag. Loopen bryts när endast en spelare är kvar vid liv. Spelet notifierar då användaren om vem som har vunnit spelet och en fråga ställs om användaren vill börja om spelet eller avsluta. 
