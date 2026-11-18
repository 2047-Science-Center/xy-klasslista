# X&Y · Valvet – gruppindelning inför besöket

Lärarverktyg för 2047 Science Centers X&Y-besök. Läraren lägger in klasslistan (Excel, CSV, inklistrad text,
skärmdump eller mobilfoto), bekräftar tjej/kille, får ett förslag på fyra testgrupper (sida A/B) och sparar en fil
som skickas till 2047.

**Öppna:** https://2047-science-center.github.io/xy-klasslista/

## Integritet
- Allt körs **i lärarens webbläsare**. Ingen server, ingenting laddas upp.
- Bilder och foton läses lokalt (Tesseract.js). iPhone-foton (HEIC) konverteras lokalt (heic2any).
- Filen som sparas innehåller **inga namn**, bara plats-kod, testgrupp, sida och tjej/kille per plats. Namnen finns
  bara på lärarens utskrift.

## Externa bibliotek (låsta versioner)
SheetJS `xlsx@0.18.5` (cdnjs) · `tesseract.js@5.1.1` + `@tesseract.js-data/swe@1.0.0` (jsdelivr) · `heic2any@0.0.4` (jsdelivr) ·
typsnitten VT323 och IBM Plex Mono (Google Fonts). OCR- och HEIC-biblioteken laddas först när en bild läggs in.

## Filformat → riggen
`xy-klasslista` version 2, se `testdata/exempel-export-8B.json`. Riggen läser in filen som en planerad körning
(`xy-rigg/xy-startkit/importera.py` eller uppladdning i incheckningen). Design och beslut: `xy-arkitektur/XY-KLASSLISTA.md`.

## Testdata
`testdata/` innehåller bara **påhittade** namn: en Excel-export (`klasslista-8B-mockup.xlsx`, ingen könskolumn),
CSV- och textvarianter, och en exempelexport.

*Prototyp 0.2. Könsgissningen bygger på en provlista med namn (byts mot SCB:s namnstatistik).*
