# Veiledning

## Tegningsklargjører

### Formål

Verktøyet brukes til å standardisere filnavn for FDVU-dokumentasjon, generere XML for Asta-import og generere BAT-fil for omdøping av filer.

### Fremgangsmåte

1. Dra inn filer eller velg filer/mappe.
2. Fyll inn eller korriger metadata i tabellen.
3. Bruk kodeoppslagene ved behov.
4. Trykk **Generer alle nye filnavn**.
5. Kontroller resultatene.
6. Last ned:
   - XML for Asta-import
   - BAT-fil for omdøping

### Tips

- Arbeidsøkten lagres automatisk lokalt i nettleseren.
- Filnavn kan overstyres manuelt.
- Valideringsfeil markeres i tabellen.

---

## Filnavn til XML

### Formål

Verktøyet brukes når filene allerede har korrekt filnavn og man ønsker å generere XML til Asta uten manuell registrering.

### Fremgangsmåte

1. Legg inn filnavn ved:
   - dra-og-slipp
   - filvalg
   - innliming av filnavn
2. Verktøyet forsøker automatisk å tolke følgende mønster:

```text
[Eiendomsnummer]-[Bygningsnummer]-[Etasje]-[Fag]-[Systemkode]-[Tegningstype]-[Løpenummer]_[Beskrivelse].[filtype]
```

3. Kontroller metadataene i tabellen.
4. Legg inn arkivenhetid/mappeid.
5. Last ned XML.

### Tips

- Filnavn som ikke følger mønsteret vil få varsel.
- Alle felter kan redigeres manuelt før eksport.

---

## Oppslag

### Formål

Verktøy for søk i kodeverk og referansedata.

### Tilgjengelige oppslag

- Eiendommer
- Bygninger
- Fag
- Systemkoder (TFM)
- Tegningstyper
- Informasjonstyper

### Eiendomssøk

Ved søk på eiendom vises:

- Eiendomsnummer
- Eiendomsnavn
- Tilknyttede bygninger

### Byggsøk

Ved søk på bygning vises:

- Byggnummer
- Byggnavn
- Tilhørende eiendom

### Kodeverk

Søk kan gjøres på både:

- kode
- navn eller beskrivelse

---

## Oppdatering av kodeverk

Kodeverkene ligger som JSON-filer i repositoryet.

Aktuelle filer:

```text
eiendommer.json
bygninger.json
fag.json
systemkoder.json
tegningstyper.json
informasjonstyper.json
```

Etter oppdatering av filene trenger man normalt bare å laste siden på nytt.

---

## Feilsøking

### Kodeverk lastes ikke

Kontroller at:

- JSON-filene ligger i samme mappe som HTML-filene.
- GitHub Pages er publisert fra riktig branch og mappe.
- JSON-filene inneholder gyldig JSON.
- Tomme JSON-filer inneholder `[]` og ikke er helt blanke.

### Ingen treff i søk

Kontroller at:

- JSON-filen er lastet inn.
- Søket er skrevet riktig.
- Det finnes data i kodeverket.

### XML eksporteres ikke

Kontroller at:

- Tabellen inneholder minst én rad.
- Nødvendige metadata er fylt ut.
- Filnavnene er tolket korrekt.

---

## Datasett og publisering

Bygnings- og eiendomsdata skal kvalitetssikres før publisering. Datasettene kan derfor være midlertidig tomme eller fjernet fra den publiserte løsningen.

---

## Versjon og kontakt

Verktøyene er utviklet som nettleserbaserte HTML-verktøy og publiseres via GitHub Pages.

**Kontakt:** Sett inn kontaktinformasjon her.  
**Versjon:** Sett inn versjonsinformasjon her.
