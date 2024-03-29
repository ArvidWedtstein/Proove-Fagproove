# Fagprøve
Forslaget er da som følger:
- 49,5 arbeidstimer for en handleliste app i Appframe 365 rammeverket med følgende mål:

## Målet med oppgaven:
1. Lage en handeliste app med registrering og innlogging for brukere.
2. Må være flere lister.
3. Må være lett for brukeren å vite hva som er handlet, og hva som gjenstår.

## Utstyr
- Omega 365 NT rammeverket / Vue.js fordi dette har brukerregistrering/innlogging integrert og er lett å komme igang med.
- DrawSQL for å tegne Tabellstruktur
- Fontawesome library for ikoner.
- SQL Server Management Studio/db-manager for redigering/oppretting av tabeller og views.
- Bootstrap
- Figma for skissing av layout

## Eventuelle informasjonskilder:
1. [Bootstrap docs](https://getbootstrap.com/docs/5.0/getting-started/introduction/)
2. [Stackoverflow](https://stackoverflow.com/)
3. Omega Ansatte

## Fremgangsmåte:
Begynner med å planlegge og lage tabellstruktur for å ha oversikt over målet.
Lager deretter tabellene og appene (hovedside og details) (mobile first)
Legger til planlagt funksjonalitet (se Skisse av løsningen).
Registrering og pålogging løses i appframe (NT) rammeverket da dette eksisterer her fra før.
Legger eventuelt til bonusfunksjonalitet, avhengig av tid til overs.
Tester gjennom appen(e) og dokumenterer dette.
Dokumenterer hva jeg har gjort.
Lager brukeranvisning.
Lager presentasjon.

## Arbeidsoppgaver:
- Planlegge, lage tabellstruktur.
- Lage tabeller, views og stored procedures.
- Inserte data i tabellene (tar meg friheten til å hente data og bilder for items fra mitt personlige prosjekt, ArkDashboard. Bildene her er lisensiert for non-commercial use, så i tilfelle dette hadde vært brukt til virkelig oppdrag, så hadde jeg gått for noe annet)
- Sette opp trigger security. Brukeren skal kun få redigere sine egne handleliste og de brukeren har fått delt
- Lage sider og dialoger
- Dokumentere dette underveis
- Lage brukerveiledning.
- Teste funksjonalitet, dokumentere testresultat
- Lage presentasjon


## Skisse av løsningen:

<details>
    <summary>Hoved Bilde (collapse for å se detaljer)</summary>

- Oversikt over brukerens handlelister
    - Oversikt over antall varer i hver liste.
    - Footer med mulighet for å lage ny handleliste
    - "3 dotter" meny på hver handeliste som gir mulighet til å redigere listens navn eller slette den.
    - BONUS:
          - Brukeren kan dele sine handlelister med andre i samme dialogen til "3 dotter" menyen. Dette gjøres via en grid for å legge til personen en ønsker å dele med lg vise/slette de som allerede har blitt delt med.
          - Søkemulighet for å la brukeren søke i handelister
      
</details>

<details>
  <summary>Details Side</summary>

  - Oversikt over innholdet i handlelisten.
  - Liste med antall av varen
      - "3 dotter" meny til høyre som gir mulighet for å slette varen, eller redigere den, ved redigering åpnes dialog for redigering av vare, antall, unit og slette varen fra handlelisten
            - Plus og minus knapp for kjapp redigering av antall
      - Click på item eller checkboxen, checker ut varen og markerer denne som "checked" / blir streket ut.
      - Sortert etter kategori for å gjøre handlingen enklere
      - Footer med oversikt over hvor mange varer som er igjen
      - BONUS:
        - Søkemulighet for varer i handlelisten.
        - Mulighet for å la brukeren bestemme hva som skal sorteres på
        - Brukeren kan lage custom items vis varen ikke eksisterer i varelisten. Disse custom varene blir da lagt til i items tabellen med referanse til brukeren som laget denne custom varen
        - Autocomplete når brukeren skriver inn item i dialogen, vis itemet ikke eksister i listen, så kan brukeren opprette item selv (også kalt FreeSolo autocomplete)

</details>

Grov [Figma Skisse](https://www.figma.com/file/Tx8VgFlesvwddki1t5iBjc/Handleliste?type=design&node-id=0%3A1&mode=design&t=GO6XAJTYVCoCmlUx-1) av tenkt layout

Tabeller: [Tabellstruktur](https://drawsql.app/teams/arvid/diagrams/tabellstruktur)


Innlogging og registrering løses i appframe rammeverket.

## Tidsskjema:

<details>
    <summary>Onsdag (6t)</summary>

- Planlegging (4.5t)
- Tabellstruktur (1t)
- Dokumentere dagens aktivteter (0.5t)
</details>

<details>
    <summary>Torsdag (8.5t)</summary>

- Dokumentere dagens aktivteter (0.25t)
- Lage tabeller, inserte data, og lage trigger security (2t)
- Lage views og stored procedures (2.25t)
    - LookupItems
          - BONUS: filter på hvilke items brukeren har fått tilgang til gjennom delt handleliste
    - Handelister
    - HandleListeItems
    - Stored Procedure for å lage ny handleliste og ny handlelistevare og for å redigere varen
- Lage Hoved Side (4t)
    - Dialog for ny liste (Bonus: Legge til mulighet for å dele denne med andre)
    - Sette opp datasources, sortering
</details>

<details>
    <summary>Fredag (8.5t)</summary>

- Dokumentere dagens aktivteter og systemdokumentasjon (0.5t)
- Lage details Details siden (6t)
  - Legge til liste med varer, legge til funksjonalitet for å checke ut varer.
  - Dialog for å redigere vare.
- Justere app(ene), tilrettelegge for eventuelle endringer i scopet. (2t)
</details>

<details>
    <summary>Lørdag (2t)</summary>

- Fikse eventuelle scope endringer som ikke kom i mål på fredag (2t)
</details>

<details>
    <summary>Mandag (7.5t)</summary>

- Dokumentere dagens aktivteter og systemdokumentasjon (0.5t)
- Lage plan for testing, tester løsningen og dokumentere resultat (4t)
- Finjustere eventuelle mangler og feil etter test (2t)
- Begynne på dokumentasjon (1t)
  
</details>

<details>
    <summary>Tirsdag (7.5t)</summary>

- Dokumentere dagens aktivteter (0.5t)
- Lage systemdokumentasjon (3.5t)
- Lage brukerveiledning (3.5t)
</details>

<details>
    <summary>Onsdag (7.5t)</summary>

- Dokumentere dagens aktivteter (0.5t)
- Lage presentasjon (7t)
</details>

<details>
    <summary>Torsdag (2t)</summary>

- Presentering (1t)
- Egenvurdering (1t)
</details>

