# InfoSec in de praktijk

## De infosec-praktijk

Aan de hand van theoretisch voorbeeld:

- Situatieomschrijving;
- Assessment
- Requirements;
- Oplossingsrichting;
- Implementatie;
- Resultaat!

We gaan de zaken die we tot dusverre besproken hebben bijeenbrengen aan de hand van een theoretisch scenario.

> **Caveat / Word to the Wise**
>
> Veel van wat we vandaag gaan bespreken is geïdealiseerd en theoretisch. De werkelijkheid is een stúk weerbarstiger!
> Dat gezegd hebbende: we hebben ons best gedaan om een zo realistisch mogelijk scenario te creëren.
>
> **LET OP: Dit IS EN BLIJFT theorie! Wat je hier te horen krijgt biedt op geen enkele wijze garanties aangaande “the real world”**

## Situatie

- Jij bent consultant;
- Nieuwe klant: ACME BV;
- Marketingbedrijf met +/- 100 medewerkers;
- Eigen ICT-voorzieningen gemanaged door drie systeembeheerders en een CTO.
- Nieuwe wetgeving (AVG) heeft ervoor gezorgd dat InfoSec ineens op de agenda staat;
- De CEO en CTO hebben besloten dat er een nieuwe firewall moet komen.

### Wat valt op?

De vraag om “een nieuwe firewall” afkomstig vanuit het MT is vreemd:

- Firewall = product
- MT = verantwoordelijk voor policies
- MT != producten

Dit duidt op het niet-volgen van de PDCA-cyclus. Er is dus sprake van een beleidsprobleem!
Een MT hoort zich niet bezig te houden met iets basaals als een firewall. Dit zaakje klopt niet... Hebben ze geen beleid?

### Een verhelderend gesprek…

Jij stelt twee vragen:
_“Waarom wordt er specifiek om een firewall gevraagd, en waarom zo specifiek dit model?”._

Het antwoord luidt:
_“Een firewall beveiligt ons systeem en de CTO heeft goede ervaringen met dit merk”._

Wat leert dit ons?
**Het antwoord geeft aan dat het MT in haast een beslissing heeft genomen en deze niet over durft te laten aan de systeembeheerders. Die hebben ze namelijk wel! Waarom?!**

### Now we're getting somewhere!

1. De opmerking over “beveiliging” duidt erop dat er géén adequate requirementanalyse is gedaan. Een firewall kan helpen om BEPAALDE aspecten van infosec te borgen, maar is geen panacea!
2. De CTO heeft al besloten wat de operationele oplossingsrichting zou moeten zijn. Dat betekent dat rollen/functies onvoldoende gescheiden zijn, want er zijn vele andere afhankelijkheden bij oplossingsselectie!

In combinatie met het ontbreken van een PDCA-cyclus duidt dit erop dat ACME geen sluitend infosec beleid heeft.

Denk “PDCA”! De CEO en CTO springen meteen naar de “ACT”-fase. Niet handig! Dus, als consultant moet je gaan bepalen waarom ze dat gedaan hebben. Er is kennelijk sprake van paniek…

### Risico-inschatting deel 2

… ACME vreest dat deze (nu failliet verklaarde) concurrent béter beveiligd was dan zij zelf!

> Er is een oude mop die zo luidt:
>
> Two men were out backpacking in the woods. Around a bend in the trail they came face to face with a bear. One of themdrops to his knee, fetches his running shoes from his backpack and begins the removing his hiking boots. The other guy just stares and says, "There is no way you can run faster than that bear."
> The kneeling guy stands up and replies, "I don't have to be faster than the bear. I only have to be faster than you.“.
>
> Als de harder rennende partij voor je ogen gepakt wordt zet dat je tot nóg grotere krachtsinspanningen aan.

### Assessment time!

ACME wil dus helemaal geen firewall aanschaffen. Ze willen hun bedrijf beveiligen!

Om een bedrijf te overtuigen dat ze hun gehele beleid aan moeten passen wanneer ze alleen hulp met een nieuwe firewall vroegen heeft nogal wat voeten in de aarde. Daar zullen we jullie verder niet mee vervelen.

### Maar het is gelukt! Requirements-tijd!

- **Requirements** identificeren adhv. wet, bestaande contracten en risicoinschatting;
- **Wet**: WBP/AVG, Wet op de Databanken, etc;
- **Contracten**: klant eist beleid volgens ISO-27001;
- **Risicoinschatting**: alle overige bedreigingen voor CIA.

**Conclusie**: er moet als de wiedeweerga een ISMS worden geïntroduceerd om PASSENDE maatregelen te definieren.

De sources of requirement, weten we nog? Wet, contract en Risicoanalyse. In dit geval was contract en risico eigenlijk gelijk: ISO 27001. Dus, er moest een Information Security Management System komen

### Threat Landscape

- **Threat** = oorsprong van risico;
- Resulteert uit **Risicoanalyse**;
- Iedere threat voorzien van **impact** en **risicoindicatie**;
- Usual suspects: Johnny Q. Hacker, de NSA/FSB/CIA/AIVD/C&A/verzin-een-acroniem, inside jobs, natuurrampen, terroristen, het Laatste Oordeel
- Kijk uit voor **FUD** (Fear, Uncertainty and Doubt)!

Om tot maatregelen te komen kun je ervoor kiezen om de bedreigingen in kaart te brengen. Dat was in dit geval handig want er was sprake van een hacker-bedreigedingetje. Deze komt voort vanuit de risk analysis en kent waarderingen op het gebied van risico (“hoe groot is de kans dat dit gebeurt?”) en impact (“hoe erg is het als dit gebeurt?”) toe aan iedere mogelijke bedreiging.
Federalnaja sloezjba bezopasnosti, de geheime dienst van de Russische Federatie
Het probleem met deze lijsten is dat ze vaak gebruikt worden om FUD te zaaien. Doe dat nooit, je geeft jezelf en de business een slechte naam.

### Oplossingsrichtingen/maatregelen

- Zoek deze in policies en producten!
- Oplossing moet op threat gericht zijn;
- Kosten versus beoogd risico (kans & impact);
- Effectief, efficiënt en elegant.

Vanuit de threat-board gaan we maatregelen zoeken die de organisatie nodig heeft. We wéten al dat er geen goed beveiligingsconcept bepaald is, dus laten we daar beginnen: Defense in Depth

### Defense in Depth

- Één is géén;
- Verdediging in lagen, waarbij iedere laag eigen maatregelen kent;
- Hoe belangrijker de informatie, hoe meer lagen er omheen bestaan;
- Dwingt onderscheid tussen gebruikers af!

Een kasteel heeft een buitenmuur, een binnenmuur en een centrale vesting of “donjon”. Dit is een schoolvoorbeeld van Defense in Depth. Maar, als mensen niet alleen “binnen of buiten” mogen zijn maar er ook tussenvormen bestaan moeten we meerdere niveaus van toegangsrecht gaan toekennen. Dat kan alleen als we onderscheid maken tussen verschillende medewerkers!

### Oplossingsrichting: taak- en functiescheiding

- Voorkomt “de slager die zijn eigen vlees keurt”, belangenverstrengeling en fraude;
- Dwingt het inregelen van toegangsrechten af;
- Kán een reorganisatie betekenen!!!!!!

Dit is één van de belangrijkste controls uit ISO-27001. Het italiaanse citaat komt uit La Divina Comedia van Dante en betekent “laat alle hoop varen gij die hier binnentreedt”. Een extern opgelegde reorganisatie is namelijk géén pretje!

### Identiteits- en authenticatiemanagement

- Of “IAM”;
- Identiteit – Wie je bent;
- Authenticatie – Hoe je bewijst dat je bent wie je zegt;

Als we er (hopelijk zonder reorganisatie) in zijn geslaagd om functies en rollen te scheiden moeten we IAM in gaan regelen.

#### Identiteitsmanagement

- Bij binnentreden en verlaten van organisatie (koppeling naar personeelszaken);
- Gaat om persoonsgegevens (AVG);
- Moet ingeregeld worden op computersysteem (systeembeheer);
- Controle obv. ID-bewijs? (arbeidsrecht)

Dus, nog niet zo makkelijk! Identificatie lijkt makkelijk maar er zijn nogal wat wetten en regels die bepalen hoe je met id-bewijzen en data om moet gaan. Dat valt niet altijd mee.

#### Authenticatiemanagement

- Door middel van factoren:
- Iets wat je weet;
- Iets wat je hebt;
- Iets wat je bent.

Password policies, SMS-codes, biometrie….

### Rechtenbeheer

Op basis van “Authorisation Object’s”.

- **Access Control Lists**:
  Ieder te beveiligen object heeft een eigen lijst van geauthoriseerde gebruikers en wát iedere gebruiker mag doen.

- **Role Based Access Control**:
  Ieder te beveiligen object wordt toegekend aan één of meerdere rollen, voorzien van een context en/of rechten. Gebruikers krijgen rollen toegewezen.

Als we IAM geregeld hebben moeten we rechten toe gaan kennen.

ACL en RBAC zijn twee voorbeelden van autorisatiemethoden die veel toegepast worden. ACL vinden we terug op \*nix filesystems, RBAC zie je bijvoorbeeld op Windows terugkomen.

### ACL vs. RBAC

- **ACL**:

  - _Pro_ - Simpel te begrijpen, makkelijk in te richten
  - _Con_ – Decentraal, moeilijk te onderhouden

- **RBAC**:
  - _Pro_ – Centraal te managen, gemakkelijk te onderhouden.
  - _Con_ – Complex, veel effort nodig voor inrichten.

### Kan het ook anders?

- ABAC – Attribute Based Access Control. Toegangscontrole op basis van context van de gebruiker.
- GBAC – Graph Based Access Control. Toegangscontrole op basis van workflow.
- En vele andere methoden!

_(Is het jullie trouwens opgevallen dat het verloop van Defense in Depth tot hier in één keer door ging? Dát is wat we eerder “elegant” noemden!)_

ABAC wordt gebruikt in SAP, Oracle ERP en andere business-toepassingen. GBAC is zeldzaam en zeer specifiek. Daarnaast zijn er vele methoden die aspecten of elementen van elkaar gebruiken.

> **Snelle recap**
>
> Om ACME BV te beveiligen hebben we een ISMS weten te implementeren;
>
> - Risicos en threats zijn geidentificeerd;
> - We hebben de organisatie gescheiden in rollen en functies;
> - We hebben de PZ en systeembeheerprocedures aangepast om identiteitsmanagement mogelijk te maken;
> - We hebben goede authenticatiemechanismen ingebouwd;
> - We hebben autorisaties ingeregeld.

## Plan, Do… en dan?

Tijd om te kijken hoe de werkvloer over ons project denkt!

### Veranderingsmanagement

- Verhoging van de beveiliging zal ALTIJD hogere complexiteit met zich meebrengen;
- Van te voren communiceren en afspraken vastleggen in procedures en instructies;
- Denk aan wachtwoord-policies, token-handling, aanvragen van rechten;
- Dit voorkomt een grote hoeveelheid geürineer.

Gebruikers zijn meestal niet blij met toegenomen regeldruk. Dit moet dan ook goed gemanaged worden! Zorg ervoor dat alle wijzigingen in interne processen en regels tijdig gecommuniceerd worden, vraag input van gebruikers en, for the love of god, bewaar je geduld!

### Hoe ziet de baas dit?

- Door sales begrote tijd voor installeren nieuwe vuurmuur: 2 dagen.
- Door jou gerealiseerde tijd voor implementeren ISMS én maatregelen: 9 maanden;

- Omzet: 35 X hoger dan begroot;
- Status ACME: verbaasd maar blij;
- Status van je baas: euforisch.

**En die firewall dan?**

### Firewall vs. IDS vs. IPS

- Firewall: blokkeert (ongewenst) netwerkverkeer obv. IP-adres en port.
- IDS: Detecteert en signaleert aanvallen obv. IP-adres, port en context (“IOC”).
- IPS: Detecteert, signaleert en voorkomt aanvallen obv. IP-adres, port, context en content (“DLP”).

Het bedrijf kreeg uiteindelijk het advies een enorm mooi apparaat aan te schaffen zodat ze naast vuurmuur ook IDS (Intrusion Detection System: op basis van indicators of compromise inbraken detecteren en melden) en IPS (Intrusion Prevention System, ook voorzien van actieve maatregelen om kwaadaardige sessies af te breken) met DLP (Data Loss Prevention) functies, waardoor alle uitgaande verkeer wordt gescand op gevoeligheid.

**“En zijn we dan veilig?”**

- Hackers? Check\*.
- APT’s (NSA, FSA, AIVD)? Sort-of-check\*.
- Inside jobs? Check\*.

* Ragnarok? Nee.
* Malware? OH HEEEEEELL NO, GIRL!

Serieus, veel C-level managers geloven dat een “firewall van merk XYZ” ze GE-GA-RAN-DEERD zal beschermen tegen malware.

\* Aangezien is gekozen voor een high-tech, state of the art supersone IPS met DLP, SPI, TNT, GHB en STFU-UNOOB functionaliteit.

\* = niet veilig maar “we hebben ons best gedaan”.

Sowieso helpt een firewall (of ids/ips) niet tegen alle bedreigingen. Malware is lastig tegen te houden met een vuurmuur.

DPL: Data Loss Preventiuon
SPI: Stateful Packet Inspection

### Enter the End(…point protection)

- Hoort (helaas?) bij de requirements van iedere Information Security standaard;
- Meestal een combinatie van antivirus en lokale firewall-toepassing;

Niet echt wat wij verstaan onder “beveiliging” en al helemáál geen vervanging voor gezond verstand, maar het creeërt business & daarmee banen, stimuleert zodanig de economie en houdt ook nog eens een hele hoop low-level programmeurs van de straat die anders alleen maar enge dingen gaan doen zoals lesgeven…

## Antivirus/malware

- Op basis van fingerprints virussen en andere malware herkennen;
- Geheugenruimte beschermen;
- In sommige (geavanceerdere) systemen staan uitsluitend aan de hand van een whitelist goedgekeurde programma’s toe (Fox-IT FoxGuard);
- Leuke aanvulling maar hoge beheerslast, duur en soms zelfs een acuut gevaar op zichzelf! (Kaspersky backdoor, ESET NOD32 en Sophos vulnerabilities…)

## ACME nu:

- Een hele hoop geld (en illusies) armer maar een ISMS (en ervaring, en maatregelen) rijker!
- Toen ze later alsnog gehacked werden hadden ze snel door dat er iets niet in de haak was. De schade bleef beperkt tot personeelsgegevens en er zijn maatregelen genomen om herhaling te voorkomen. Géén boetes!
- Nu één van de belangrijkste voorvechters van InfoSec en Responsible Disclosure in hun vakgebied;
- De consultant in kwestie is inmiddels met (dikverdiend!) pensioen.

Zoals eerder gezegd, dit alles is “based on a true story”. De consultant in kwestie is inmiddels met pensioen en gebruikt dit verhaal regelmatig om het verschil tussen maatregelen en beleid te illustreren.
