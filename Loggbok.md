## Loggbok

### 2024-03-19

Idag började jag med projektet. Jag skapade först alla html sidor och fixade filstruktur, skapade mappar för css, img och js. Jag började lite med headern, jag lade till texten i nav och logo-bilden. Nästa gång ska jag fixa css för headern så att den passar för både mobil och desktop.

### 2024-03-26

Idag gjorde jag klart headern och började på footern. Footern fungerar nu på mindre skärmar men jag har inte börjat skriva css:en för datorer/större skärmar än.

### 2024-04-09
Jag ändrade färger på headern och footern eftersom vit var finare. Längst ned lade jag till ett nyhetsbrev, bilden gjorde jag själv, sedan la jag rutor med input mitt i bilden så att det blir så som jag designade. På mobila enheter förstoras bilden så att den passar mobilens smala skärm. Jag ändrade så att webbsidan fungerar och ser bra ut på både mobil, surfplatta och dator genom t ex ändra storlek på text m.m. Sedan började jag med den första sidan och lade till den första delen - guider där det finns en knapp som leder till sidan "guider". 
För att organisera css:en skapade jag css filer för varje sida, i style.css finns css som gäller för alla sidor, såsom headern och footern. "Småsidor.css" tänker jag använda till material.html och tvatta-frimarken.html eftersom de kommer vara simpla sidor och lika varandra bara med olika innehåll.

### 2024-04-16
Jag har gjort del 2 och del 3 på sidan hem. Del 3 med nyheter och event fungerade först inte men sedan bytte jag plats så att jag länkade till javascripten längst ner på sidan och då funkade det. Första sidan är klar.
Sedan började jag med min andra sida: "Guider". Jag gjorde klart del 1 med två rutor, en som leder till sidan material och en som leder till sidan tvätta frimärken. Sedan började jag med del 2 och skrev html. Jag gjorde även lite css, gjorde den delen responsiv med css grid.

Nu har jag gjort klar den andra sidan, guider. Den är responsiv och passar för både mobil och dator. Jag har också lagt till den prickade linjen bredvid menyn på datorer och ändrat texterna till snygga färger.

### 2024-04-23
Jag har gjort klart sidan material. Det var en mini sida men nästan bara text och bilder. Längst upp till vänster till en tillbaka knapp som går tillbaka till förra sidan, guider. Längst ner finns en länk som gör att man bläddras till toppen av sidan.
Nu är jag klar med sidan tvätta frimärken. På sidan finns en bild, text och en ordnad lista. Det valde jag för att koden skulle vara mer semantisk. 

### 2024-04-30
Jag började med sidan händer just nu. Lade in text och rutorna. Även en rubrik längst upp för att man lättare ska kunna veta vilken sidan man är på. Jag har gjort rutorna responsiva med flexbox så att på mindre skärmar är rutorna rakt under varandra och på större skärmar bredvid. Jag ska lägga till ytterligare några rutor med event, jag behöver inte ändra css dock utan bara lägga till class="ruta". Men däremot ska jag ändra lite textstorlek på mobiler. Nu har jag gjort det!
Lade till alt på alla bilder för att öka tillgängligheten.

Jag testade att validerna en av mina HTML sidor, "guider" och fick upp man inte får ha button i en länk, a. Jag ändrade och lade istället knapparna i en form.
Valideringssidan tipsade mig också att ändra html lang="en" till html lang="sv" eftersom min hemsida är på svenska. 
Sedan när jag validerade min index sida fick jag upp meddelandet att section och article borde ha headers vilket jag inte hade. Jag tänkte innan att jag vill ha något som inneslutade bild och text och för att göra det semantiskt valde jag bara article, men det verkar inte fungera så. Så jag ändrade article till div eftersom jag vill göra .fakta delen responsiv men inte ha med headern. Det är enklast då att göra om det till en div. Och sedan ersatte jag den delen av webbsidan längst upp (på hem) som jag satte till section men som bara var en bild och knapp till figure. Som man tydligen kunde ha till självständiga bilder, diagram m.m. Sedan finns det inget annat problem med HTML:en.

Jag tog bort -ms-transform: translate(-50%, -50%); eftersom, om jag förstod det korrekt, är ms något man lägger till för att göra hemsida tillgänglig på äldre versioner av internet explorer, och det tro jag inte att jag behöver. Så jag tog bort den. I början när jag sökte hur man lägger in en knapp i en bild hade de den raden kod i tutorialen så jag lade in den men eftersom den inte har så stor betydelse tog jag bort den nu. Det är inte längre så många som använder internet explorer. Redan 2013 slutade Microsoft utvecklingen av IE.
Inget annat problem finns med CSS:en heller.

När jag testade att använda lighthouse fick jag ett väldigt dåligt resultat på performance, bara 47. Det är mina PNG bilder troligen som gör att min hemsida laddas vädigt långsamt. Därför tänker jag följa lighthouse:s råd och byta bilderna till WebP som är snabbare. 
Jag ska göra bilderna lite mindre, vissa är för stora även fast man inte behöver se bilden så noggran och klar. 
Nu har jag gjort bilderna mindre och testade igen och fick ett score på performance på 82, märkvärt förbättring för första gången.
Jag har ändrat alla bilder till webp och fick scoret 92.
Lade till meta description på alla sidor eftersom lighthouse sa åt mig att göra det. Liten beskrivning som användare ser om den söker på ex google och får upp min sida.
Jag bestämde mig för att inte ha någon fallback image eftersom det är svårt att testa om det fungerar sedan, när jag sökte stod det att 96.3% webbläsare stödjer webp. Så jag tror att webp är idag stödd av nästan alla webbläsare och därför är det inte nödvändigt att ha en fallback img, det blir bara krånligare.

Lade till kommentarer på html och css.