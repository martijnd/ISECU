# Week 4 - Policies

> “If you think technology can solve your security problems, then you don't understand the problems and you don't understand the technology.”
>
> — Bruce Schneier

Beleid is waarschijnlijk het belangrijkste component van informatiebeveiliging. Informatie bestaat niet alleen uit data op computer- of netwerksystemen maar in een multi-dimensionele ruimte waar tevens een hoop ellende rondzweeft. Om informatiebeveiliging in alle domeinen te borgen moet volgens een eenduidig, helder en bovenal verstandig beleid gewerkt worden.

## Raamwerken en kaders

- Telkens het wiel opnieuw uitvinden?
- Iedere controle anders?
- Geen overdraagbaarheid tussen organisaties?

Om ISMS’en te kunnen meten, borgen en vergelijken worden “normen” gedefinieerd. Deze bestaan op vele niveaus, van hoog (strategisch) tot laag (operationeel). Één van deze normen is dé gouden standaard voor informatiebeveiliging geworden…

## Information Security Management Systems (“ISMS”)

- Term afkomstig van de British Standards Institute of **“BSI”**
- **BSI** bepaalt standaarden voor nationaal gebruik (UK)
- Sommige van deze standaarden worden aangepast voor internationaal gebruik
- Internationale standaarden worden bepaald en beheerd door de International Standards Organisation: “ISO”

Informatiebeveiligingsbeleid valt of staat met het management ervan, wat aan normen gehouden kan worden. Dit wordt ISMS genoemd, een term die bij de BSI vandaan komt. De BSI is een engels instituut maar veel van hun normen en standaarden zijn internationaal geworden. Één specifieke, op ISMS gerichte norm is door het internationale standaardenbureau ISO overgenomen…..

## ISO

- Grootste standaardisatieorganisatie ter wereld
- Houdt zich bezig met uiteenlopende standaarden, van kwaliteitsmanagement tot ISO-3591 en ISO-3103

De standaard voor informatiebeveiliging is ISO-27000.
ISO heeft dus idd standaarden die “het standaard wijnglas” en “het standaard kopje thee” (de inhoud, niet het kopje!) beschrijven.

## ISO-27000 (en verder)

- Familie van standaarden, van **27000 tot 27042**
- Sluit naadloos aan op andere ISO-standaarden
- **27001** beschrijft de **eisen**, **27002** beschrijft de **controlepunten** uit 27001, **27018** gaat over **privacyinformatie** in cloud-services, **27032** over **cybersecurity** **richtlijnen**, etcetera…
  Belangrijkste eis: **Alles documenteren**

De ISO normen voor ISMS vinden we in de ISO-27XXX reeks. Deze reeks vormt de wereldwijde standaard, mede omdat ze zo goed aansluiten op andere ISO-normeringen als ISO 9001 “Kwaliteitsmanagement”.

De eerste 3 normen (27001 t/m 3) zijn algemeen van zin (toepasbaar voor iedere organisatie), in de verdere normen worden meer specifieke regels gedefinieerd.

De belangrijkste regel uit 27kX is dat alle, **ALLE** werkzaamheden volgens vastgestelde processen en procedures uitgevoerd moeten worden.

## ISO-27001 certificering

- Pre-audit: aan de hand van ISO-27001 controleren of er een ISMS is ingericht
- Verbeterpunten benoemen
- Audit: Aan de hand van ISO-27002-meetpunten de performance van het ISMS vaststellen

Op zichzelf betekenisloos maar toont aan dat de organisatie leert van haar “fouten”.

Het ISMS van een organisatie kan gecertificeerd worden volgens de ISO27001 normen. Goede PR, want dit toont aan dat een bedrijf hun informatiebeveiliging érg serieus neemt – ISO doesn’t come cheap! Dit proces behelst het uitvoeren van een pre-audit waarbij wordt gekeken of er uberhaupt sprake is van een ISMS. Zo ja, dan krijgt de te certificeren partij een paar maanden om hun processen te optimaliseren. Daarna vindt de “echte” audit plaats waarbij de prestaties van het ISMS worden gemeten aan de hand van de ISO-27002 norm.

## Deming-cyclus

- Bedacht door W. Edward Deming als kwaliteitsmanagement-methode
- Continue verbetering van processen
- Gebaseerd op de wetenschappelijke methode

![deming](images/deming.png "deming")

### Plan-fase

- Onderken problemen
- Identificeer verbeterpunten
- Definieer oplossingen

**Management**: Bepalen strategie, opzetten ISMS  
**Plan**: De eerste fase, waarbij de operaties worden geïnventariseerd en probleempunten worden geïdentificeerd.

### Do-fase

- Implementeer oplossingen
- Gebruik nieuwe methodes
- Experimenteer met vernieuwingen

**Operaties**: Development, systeembeheer  
**Do**: Het doorvoeren van verbeteringen op de werkvloer.

### Check-fase

- Meet performance
- Vergelijk met de oude methode
- Kwantificeer de verbeteringen

**Audits**: Pentesting, red-teams, toezichthouders  
**Check**: Het meten van de vernieuwde bedrijfsprocessen en vergelijken met de voorgaande manieren.

### Act-fase

- Bepaal de beste oplossing
- Leg de nieuwe inzichten vast
- Pas het geleerde toe in de dagelijkse praktijk

**Management**: Reorganisatie, wijzigingsmanagement  
**Act**: Keuzes maken en de beste optie doorvoeren in alle bedrijfsprocessen

## ISO 27000-requirements

- Iedere maatregel moet een reden hebben
- Deze redenen noemen we “requirements”
- 3 soorten:
  - Wettelijke vereisten
  - Contractuele vereisten
  - Risicoanalyse

ISO-2700X is gebaseerd op requirements. Vanuit wet, contracten en risicoanalyses worden verbeterpunten geïdentificeerd, welke resulteren in maatregelen.

## Requirements uit normen

- De meeste normen gaan meer op details in
- Smaken: technisch/operationeel, organisatorisch, juridisch
- Vaak per jurisdictie geregeld: NL, EU, VS…
- Maar kan ook per vakgebied: banken, zorg, ICT…

Requirements komen dus onder meer voort uit normen. We kunnen voor ieder wissewasje een risico-inschatting doen maar het is veeeeel makkelijker om ons aan normenkaders te houden – deze zijn (als het goed is) gedocumenteerd en worden breed gedragen. Sommige normen focussen op een specifiek domein, bijvoorbeeld de techniek (voorbeeld: Kiwa) of huishoudelijke materialen (Nederlandse Vereniging van Huisvrouwen). Soms zijn ze per rechtsgebied geregeld: alleen NL, heel Europa of juist de VS. Tot slot zijn er normen die alleen gelden voor een specifieke industrie of vakgebied.

## ETSI

- European Telecommunication Standards Institute
  Bepaalt EU standaarden
  - **EN/ES**: Europese (verplichte) standaard,
  - **EG**: Niet verplichte aanwijzing,
  - **TS**: technische specificatie,
  - **TR**: technisch verslag van informatieve aard.
- Voorbeeld: EN 319 411-1 “Electronic Signatures and Infrastructures (ESI) Policy and security requirements”

ETSI bepaalt alle telecom-standaarden voor Europa. Daarnaast houdt ETSI zich bezig met crypto- en technische normering voor ICT-toepassingen. Er zijn 4 soorten normen:

- verplichte standaard
- optionele aanwijzing
- technische specificatie
- informatief verslag.

Het voorbeeld omschrijft de manier waarop een certificatenserver voor digitale handtekeningen beheerd dient te worden. Nogal ambtelijk, nietwaar?

## FIPS

- Federal Information Protection Standards
- Bepaalt VS standaarden
- Bijna altijd erg technisch van aard
- Voorbeeld: FIPS 140-2 “Security Requirements for Cryptographic Modules”

De VS tegenhanger van ETSI. Véél meer op de techniek gericht en in dat opzicht dé standaard voor crypto-land. Bijgevoegd een klein stukje over de manier waarop een random number generator in een HSM (Hardware Security Module) dient te werken.

## Industrie-specifieke normen

- Vanuit risicoinschattingen, ervaringen en wettelijke disputen ontstaan
- Gericht op één bepaalde business
- Onderhouden door normeringsinstanties, beroepsorganisaties en/of overheden
- Voorbeelden: PCI-DSS, Thuiswinkel Waarborg, NEN-7510

Deze normen zijn specifiek voor één bepaalde doelgroep opgesteld. De logos onderop betreffen NEN-7510 “Informatiebeveiliging in de zorg”, het Thuiswinkel waarborg en PCI-DSS voor het afhandelen van creditcard betalingen.
