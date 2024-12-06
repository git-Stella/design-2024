---
Title: LOAD
Description: Stella´s load page
Template: analyze
---

# LOAD

I denna uppgift så analyserar vi hur tre olika sidor optimiserar sin laddning.

Urval
-----------------------

Jag har valt att ta med en "fandom" sida, https://honkai-star-rail.fandom.com/wiki/Honkai:_Star_Rail_Wiki då jag vet att de använder mycket ads och jag ville se om det hade en stor påverkan. Sedan tog jag en liknande sida, https://arknights.wiki.gg/wiki/Arknights_Terra_Wiki som tidigare hade en fandom motsvarande men hade flyttats till en ny domän för att ha mindre ads. Detta för att kunna jämföra. Såklart kan ju annat påverka också men jag var intresserad av att kunna jämföra dem. Sedan valde jag youtube, https://www.youtube.com/, då den laddar in så många videor och jag upplever den som en sida som ofta har problem när man får dålig uppkoppling men annars förvånandsvärt effektiv.

Metod
-----------------------

Jag använde mig av sidan https://pagespeed.web.dev och av network sidan under inspect för att få fram relevant data för analysen.

Resultat
-----------------------

Dokumentera dina resultat från din studie. Berätta vad du kom fram till, vilka resultat du hittade och observerade.

Star rail wiki:
![StarRailWiki](%assets_url%/img/starwiki.png)
<div class="calc">
    <source media="(min-width: 668px)" srcset="https://docs.google.com/spreadsheets/d/e/2PACX-1vSM2xsrNji4uk80eHkJBwy29jK3AI8HKdsso_ONSxDNcl2LS3ARFuDZfj3P1JwfHRONBUXGCtxAgfiy/pubhtml?gid=0&amp;single=true&amp;widget=true&amp;headers=false&w=650">
    <source media="(min-width: 376px)" srcset="https://docs.google.com/spreadsheets/d/e/2PACX-1vSM2xsrNji4uk80eHkJBwy29jK3AI8HKdsso_ONSxDNcl2LS3ARFuDZfj3P1JwfHRONBUXGCtxAgfiy/pubhtml?gid=0&amp;single=true&amp;widget=true&amp;headers=false&w=450">
    <iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vSM2xsrNji4uk80eHkJBwy29jK3AI8HKdsso_ONSxDNcl2LS3ARFuDZfj3P1JwfHRONBUXGCtxAgfiy/pubhtml?gid=0&amp;single=true&amp;widget=true&amp;headers=false"></iframe>
</div>
De skulle kunna reducera mängden oanvänd javascript. Också de laddar redan in mycket bilder och CSS element så att också ha flera tredje part ads och sådant på en redan väldigt belastad sida skapar en del problem.

Arknights terra wiki:
![TerraWiki](%assets_url%/img/arkwiki.png)
<div class="calc">
    <source media="(min-width: 668px)" srcset="https://docs.google.com/spreadsheets/d/e/2PACX-1vSM2xsrNji4uk80eHkJBwy29jK3AI8HKdsso_ONSxDNcl2LS3ARFuDZfj3P1JwfHRONBUXGCtxAgfiy/pubhtml?gid=189716273&amp;single=true&amp;widget=true&amp;headers=false&w=650">
    <source media="(min-width: 376px)" srcset="https://docs.google.com/spreadsheets/d/e/2PACX-1vSM2xsrNji4uk80eHkJBwy29jK3AI8HKdsso_ONSxDNcl2LS3ARFuDZfj3P1JwfHRONBUXGCtxAgfiy/pubhtml?gid=189716273&amp;single=true&amp;widget=true&amp;headers=false&w=450">
    <iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vSM2xsrNji4uk80eHkJBwy29jK3AI8HKdsso_ONSxDNcl2LS3ARFuDZfj3P1JwfHRONBUXGCtxAgfiy/pubhtml?gid=189716273&amp;single=true&amp;widget=true&amp;headers=false"></iframe>
</div>
Även denna tipsade pagespeed om att reducera oanvänt CSS och javascript. Den laddar in mängder med bilder denna också men är lite mer effektiv och har mindre tredje parts kod.

Youtube:
![Youtube](%assets_url%/img/youtube.png)
<div class="calc">
    <source media="(min-width: 668px)" srcset="https://docs.google.com/spreadsheets/d/e/2PACX-1vSM2xsrNji4uk80eHkJBwy29jK3AI8HKdsso_ONSxDNcl2LS3ARFuDZfj3P1JwfHRONBUXGCtxAgfiy/pubhtml?gid=1275858046&amp;single=true&amp;widget=true&amp;headers=false&w=650">
    <source media="(min-width: 376px)" srcset="https://docs.google.com/spreadsheets/d/e/2PACX-1vSM2xsrNji4uk80eHkJBwy29jK3AI8HKdsso_ONSxDNcl2LS3ARFuDZfj3P1JwfHRONBUXGCtxAgfiy/pubhtml?gid=1275858046&amp;single=true&amp;widget=true&amp;headers=false&w=450">
    <iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vSM2xsrNji4uk80eHkJBwy29jK3AI8HKdsso_ONSxDNcl2LS3ARFuDZfj3P1JwfHRONBUXGCtxAgfiy/pubhtml?gid=1275858046&amp;single=true&amp;widget=true&amp;headers=false"></iframe>
</div>
Även denna sida får samma tips av pagespeed. Den tipsar även om att göra sig av med "render blocking resources". Oavsett så youtube har många av samma typer av problem som de tidigare sidorna, men för att fungera som tänkt har den ett ännu större behov av att ladda in fler stora filer.

Enligt dessa mätvärden så skulle jag räkna Arknights Terra wiki som vinnaren. Man kan tänka på olika sätt, relativt till objekten som laddas in så förlorar den mot Star Rail Wiki, men Star Rail Wiki tar mycket lång tid att ladda in allting och är större, kräver högre prestanda. Youtube klarar sig inte ens igenom pagespeed´s test och får störst storlek trots att den laddar in färre objekt. Andra plats räknar jag som youtube. Den laddar in mycket fortare än Star Rail wiki, trots den större storleken. Den laddar också in färre objekt men många av de objekt som laddas in på Star Rail Wiki är ads.

För att räknas som att det laddar snabbt skulle jag nog sätta att gränsen går vid 3 sekunder ungefär. Och för att räknas som långsamt så skulle jag nog anse att det ska gå åtminstonde 12 sekunder innan jag anser att det är för långsamt för att kunna vara villig att använda en sida ofta. Star Rail Wiki misslyckas med detta måttet medans de andra två klarar sig till att vara normal hastiget. Jag har däremot haft bättre erfarenhet med ad blocker på.

Analys
-----------------------

Det verkar som att det vanligaste enkla att lösa problemen skapas av oanvänd CSS eller javascript kod. Dessa dök upp på alla tre sidorna och gjorde det långsammare. Det var intressant att youtube inte var så illa optimerad, då jag personligen upplevt den som en sida som lätt slutar fungera om internet connection blir dålig. Den laddar in färre objekt men sidan är större och den laddar ändå in det relativt fort. Man hade lätt kunnat göra ett argument för att ranka den över mitt val till rank 1 på grund av detta, jag valde bara att prioritera att kunna hålla ner storleken på sidan och att snabheten kommer före istället för att ta hur snabbt det är relativt till storleken på sidan.

Rapport av
-----------------------

Stella Karlsson