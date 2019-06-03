# Week 1

Informatiebeveiliging, waarom?

> "Worldwide spending on information security will reach \$86.4 billion in 2017, an increase of 7 percent over 2016, with spending expected to grow to \$93 billion in 2018, according to the latest forecast from Gartner, Inc."

Hierom:

- Meer dan 4000 ransomware aanvallen per dag
- 45% van de mensen klikt zonder na te denken op links in e-mails
- 58% van MKB niet voorbereid op dataverlies
- Boetes tot 20 miljoen euro

Informatie is enorm waardevol, en de bedreigingen zijn groot. Malware als virussen en trojans nemen hand over hand toe, veel mensen zijn zich niet bewust van hun verantwoordelijkheden (bedrijven evenmin) en dit terwijl een gebrekkig informatiebeveiligingsbeleid je als bedrijf op enorme boetes kan komen te staan. Het is soms werkelijk waar een “dumpster fire” (a complete disaster).

## Informatiebeveiliging als proces

- Initieel als verzameling technische maatregelen
- Later ook organisatorische maatregelen
- Nu: toevoeging aan bestaande bedrijfsprocessen

Hiervoor zijn nodig: **Standaardisatie, professionalisering, en meetbaarheid**

> InfoSec is lang gezien als alleen maar een pakketje technische maatregelen. Gedurende de jaren ‘80 werden organisatieaspecten toegevoegd. Dus, niet meer alleen een lang wachtwoord afdwingen maar gebruikers óók instrueren om hun wachtwoord regelmatig te wijzigen. Inmiddels komt informatiebeveiliging in iedere laag of ieder proces van een organisatie terug. Dat is mogelijk geworden door het standaardiseren van regels (wetgeving, normen, etc), professionaliseren van (IT)-personeel (certificeringen, vakken als dit op opleidingsinstituten) en het meetbaar maken van prestaties op het gebied van informatiebeveiliging (bijv. door geautomatiseerde rapportagemechanismen).

## De doelen van informatiebeveiliging

- **Confidentiality** - Vertrouwelijkheid
- **Integrity** - Onveranderlijkheid
- **Availability** - Beschikbaarheid

> Formeel gesproken kunnen we de doelen van het informatiebeveiligingsproces in de CIA-driehoek plaatsen: confidentiality, Integrity en Availiability. Dit zijn de drie primaire vereisten om informatie veilig te houden. De exacte oorsprong van dit model is in de annalen der tijd verloren gegaan, maar in de late jaren ‘80 werd dit model gemeengoed. Onthou dit model! “This is my model! There are many like it but this one is mine!”. Dit model is de BASIS van InfoSec!

### Confidentiality

- Vertrouwelijkheid
- Meest bekende doel
- Het beperken van toegang tot informatie
- Toegang wordt op basis van gebruiksrecht verschaft of ontzegd

Voorbeelden: geheimschrift, encryptie, toegangsbeperkingen

> Vertaling: VertrouwelijkheidDit is het doel waar iedereen direct aan denkt wanneer ze met informatiebeveiliging te maken krijgen en betreft het beperken van toegang tot informatie. Echter, niet-toegankelijke informatie had net zo goed niet kunnen bestaan, dus wordt gebruiksrecht toegekend of ontzegd al naar gelang iemand deze toegang nodig heeft. Voorbeelden hiervan zijn ouderwets geheimschrift, de moderne computer-versie hiervan (enncryptie) en het beperken van toegang tot informatie, bijvoorbeeld door deze in een kluis op te bergen.

### Integrity

- Onveranderlijkheid of integriteit
- Iets minder vanzelfsprekend
- Het garanderen dat informatie niet ongewenst verandert
- Registreren of voorkomen van wijzigingen, afhankelijk van de vereisten

Voorbeelden: redundante opslag, checksums, opslag op read-only media.

> Vertaling: Onveranderlijkheid of integriteitDit doel is iets minder vanzelfsprekend maar minstens net zo belangrijk. Integriteit betreft garanderen dat informatie niet ongewenst verandert – vernietiging is in deze context óók een wijziging. Dat kan betekenen dat wijzigingen aantoonbaar moeten zijn, of dat deze onmogelijk gemaakt moeten worden. Dit is afhankelijk van de vereisten die aan de informatie gesteld worden. Voorbeelden zijn redundante opslag, bijvoorbeeld door middel van backups, het maken van checksums (komen in een latere les aan bod) en opslag op alleen-lezen media zoals een DVD.

### Availability

- Vertaling: Beschikbaarheid
- Wordt vaak vergeten
- Informatie moet wanneer benodigd gebruikt kunnen worden door gerechtigde partijen;
- Heeft raakvlakken met IT-beheer

Voorbeelden: Fail-over, load-balancing, disaster recovery

> Vertaling is “Beschikbaarheid”. Dit doel wordt vaak vergeten. Wanneer benodigd moeten de beoogde gebruikers toegang tot de informatie kunnen krijgen, anders had de informatie het net zo goed niet kunnen bestaan natuurlijk! Het garanderen van de beschikbaarheid van informatie wordt in de praktijk vaak bij IT-beheerders gelegd maar vergis je niet – het is echt een informatiebeveiligingscomponent!Voorbeelden van maatregelen om Availability te borgen zijn fail-over systemen (waarbij een defect apparaat automatisch wordt vervangen door een werkend apparaat), load-balancing (waarbij meerdere apparaten aan elkaar worden geknoopt om meer capaciteit te krijgen) en disaster recovery (waarbij maatregelen worden genomen om ook na een grote ramp de IT-dienstverlening weer op orde te krijgen).

## 3-, 4-, 5-, of 6-hoek?

Er zijn nogal wat pogingen gedaan om het model uit te breiden met aanvullende vereisten – bijvoorbeeld identiteitsbeheer (mensen identificeren langs digitale weg), authenticatiebeheer (digitale inlogmiddelen beheren), rechtenbeheer en onweerlegbaarheid (ondubbelzinnig vastleggen wie een bepaalde handeling heeft uitgevoerd). Deze initiatieven zijn echter nog geen gemeengoed geworden en worden in de praktijk vaak onder de noemer “confidentiality” geschaard.

# Componenten van informatiebeveiliging

Zoals de doelen van informatiebeveiliging in drieën kunnen worden verdeeld kunnen ook de componenten van een werkbaar en effectief informatiebeveiligingsbeleid in drie groepen worden onderverdeeld. We maken hierbij onderscheid in:

- De Primitives – Wiskundige principes die vanuit een technisch oogpunt noodzakelijk zijn om de InfoSec-doelen op computeromgevingen te behalen;
- De Policies – Beleidsregels en –afspraken die vanuit een organisatorisch oogpunt noodzakelijk zijn de InfoSec-doelen op computeromgevingen te behalen;
- De Products – Combinaties van primitives & policies die op computeromgevingen toegepast kunnen worden om de InfoSec-doelen op computeromgevingen te behalen.

## Componenten: Primitives

- Term komt van “Cryptographic Primitives”
- De basisconcepten van cryptografie
- Uit het Grieks: “Kruptos” en “Grafein”
- Gewoon wiskunde dus

> Cryptografische primitieven zijn de basiscomponenten om cryptografie mogelijk te maken. De term “cryptografie” komt uit het Grieks via de woorden “Krupto”s” (verborgen) en “Grafein” (schrijven). Dus, “geheimschrift. “The Benefits of a Classical Education”, indeed! Computers zijn in beginsel wiskundige machines, dus moest “geheimschrift voor computers” ook op wiskundige leest gestoeld zijn. Vandaar dat de cryptografische primitieven allemaal wiskundig van aard zijn. We proberen de wiskunde in dit vak beperkt te houden, maar zullen er niet aan ontkomen om jullie ook hieraan te laten snuffelen.

## Componenten: Policies

- Policies = beleid
- De interne en externe spelregels voor bedrijven, overheid en andere organisaties
- Bronnen: wwet- en regelgeving, normeringen, certificeringen, "Common sense"
- Gewoon bedrijfskunde dus

> Beleid is het “regelboek” aan de hand waarvan een organisatie opereert. De regels die het beleid vormen hebben (natuurlijk) een oorsprong. Deze oorsprong kan verschillen: wetten, normenkaders waaraan een organisatie graag wil voldoen, certificeringen die behaald moeten worden en natuurlijk ouderwets boerenverstand (dit laatste vaak aan de hand van een risicoinschatting). We proberen de bedrijfskunde in dit vak beperkt te houden, maar zullen er niet aan ontkomen om jullie ook hieraan te laten snuffelen.

## Componenten: Products

- Products = implementatie van Primitives & Policies
- Software, hardware en gedrag
- Maken een organisatie veiliger
- Einddoel van informatiebeveiligingsproces

> Producten zijn het einddoel of de “eindbaas” (vandaar de plaatjes) van het informatiebeveiligingsproces. Ze kunnen verschillende vormen aannemen: software, hardware of gedrag van mensen (al dan niet geholpen door technische ingrepen). Producten zijn de implementatie of uitvoering van beleid én primitieven, de plek waar alles samenkomt. De uiteindelijk producten zijn wat een organisatie werkelijk “veiliger” maakt. We proberen de bedrijfskunde in dit vak beperkt te houden, maar zullen er niet aan ontkomen om jullie ook hieraan te laten snuffelen.
