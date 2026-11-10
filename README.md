# EPF Studio • Addio Fleet Logic & CAN Matrix Explorer

An interactive visualizer, logic engine analyzer, and CAN bus signalbank matrix decoder for Addio EPF vehicle control profiles and systems.

---

## 🚀 Quick Start (Single-File / Zero Installation)

Open `index.html` in any modern web browser (Edge, Chrome, Firefox, Safari).  
Everything is self-contained with no local node/server or build dependencies.

---

## 🌟 Key Features

1. **Universal Addio EPF XML Decoder & Runtime Visualizer**:
   - Clean, neutral startup state: drop any `.epf` or `.xml` file to automatically decode hardware modules, pinouts, and logic trees.
   - Dynamic hardware node reconstruction for Master, Slave, Switch Panels (MP 1–4), and Input Units.
   - Built-in on-demand demo: click **`⚡ Demo`** in the top bar to test with the bundled multi-node fleet sample.
   - Live drag-and-drop file zone allowing you to load multiple profile configurations simultaneously.
   - **Full Support for 4-Output and 8-Output Centrals**: DRB1612-4 (Nano 12V/24V Adv), DRB5012-4-ADV, DRB3012, DRB4012, SCRE och DRB9012-8.
   - **Autodetektering av Manöverpaneler (MP 1 – MP 4)**: Avkodar automatiskt knappkonfiguration, växlande/momentana funktioner, reflekterade utgångar och knappfärger när fordon använder manöverpanel istället för handkontroll (t.ex. ID.Buzz m.fl.).

2. **🌲 VU Logic Port Tree (`Hotkey: V`) — 100% Dynamisk**:
   - **Profilanpassad logikrekonstruktion**: Bygger automatiskt upp alla virtuella grindar (VU1–VU16) och portvillkor utifrån de profiler som laddats in (Master 91, Jour 2/3, Slavar etc.).
   - **Realtidsvillkor & Interlock Flow**: Portvillkor visar dynamiskt uppfyllda bockar (`✓ 1`) eller blockerade kryss (`❌ 0`), med riktningspilar och beräknade logikfunktioner (AND, NOT/Spärr, Buffert, XOR/Blixt, NOR, Vippa, Timer).
   - **Dynamisk Live Test-panel**: Test-toolbar för insignaler genereras automatiskt utifrån de styrsignaler som faktiskt används i profilens grindar (`MP1-4 B1-8`, `HK B1-B15`, `Plint In 1-8`, `Signalbank Slot 1-48`, `22ch IU`).
   - **Smarta filter & flödeskedjor**: Filtrera per box/nod (`Nod 91`, `Nod 92` etc.), visa dedikerade funktionskedjor eller filtrera direkt på aktiva vs spärrade grindar.

3. **⚡ Dynamisk Sidopanel & Driftlägen (Logikmotor & Inspektör)**:
   - **100% Profilstyrd Live Simulator**: Sidopanelens knappmatris i `LIVE LOGIC SIMULATOR` genereras dynamiskt efter vald fordonsfil (t.ex. Manöverpanel med `MP1 B1 Blixtljus`, `MP1 B2 Arbetsljus`, `MP1 B3 Extraljusramp`, `MP1 B4 Värmare` eller GBG Jour med `HK B1 Arb vanster` etc.).
   - **Dynamiska Driftlägen (`LIVE OPERATIONAL MODE TRACING`)**: Kretsar och förval genereras automatiskt utifrån bilens faktiska insignaler och vad de styr med passande ikoner (🚨 Blåljus, ⚠️ Varningsljus, 💡 Arbetsbelysning, 🔆 Extraljus, ⚡ 12V/Inverter, 🔋 Energisparläge).
   - **Omgående Uppdatering vid Namnbyte**: När en knapp eller utgång döps om i inspektören uppdateras sidopanelens knappar och förval i realtid.

4. **📄 Officiell Utskriftsrapport & Fordonsdokumentation (`Hotkey: P`)**:
   - **Exakt Addio-layout**: Återskapar det officiella utskriftsformatet från Addio Control Center (precis som i `11.rtf` / `11.pdf`).
   - **Färdiga Tabeller**: Egenskaper för utgångar (U1–U4 eller U1–U8 dynamiskt anpassat efter hårdvarumodell) med säkringar, ingångar, inversion, funktioner, fading och LED-färger; Manöverpaneler (MP1–4); Virtuella grindar (VU 1–16); Energibesparing (avstängningsstatus per utgång); Spänningsvakt (11–16V); Filter och multipla enheter.
   - **🖨️ Skriv ut / Spara PDF**: Ett klick öppnar webbläsarens utskriftsdialog med ren vit A4-styling, skarpa tabeller och sidbrytningar.
   - **Stöd för Anpassade Namn**: Växla enkelt mellan originalnamn och dina egna pedagogiska etiketter i utskriften.

5. **📡 CAN Signalbank Matrix (`Hotkey: M`)**:
   - Full 35-slot CAN ID broadcast map mellan Master Nod 91 och Slavar 92 & 93.
   - Live uppdatering av signalvärden under interaktiv simulering.
   - Flerprofilsjämförelse och rå XML-sektionsinspektör.

6. **🔋 Energisparläge & Spänningsvakt (`Hotkey: E`)**:
   - Avkodar Addio `PWR_MANAGEMENT` och `VOLT_MANAGEMENT` automatiskt från .epf XML-filer.
   - Dedikerad **`🔋 Energisparläge`**-toggle i toppmenyn och realtidssimulatorn.
   - Visar hur trigger-signaler (In 1-8 eller Signalbank Slot 1-48) är kopplade till utgångarna.
   - Klipper automatiskt kretsar visuellt i realtid vid sparläge så att förbrukare stängs av för att skydda fordonets startbatteri.

7. **🏷️ Egna Etiketter & Pedagogiska Förklaringar**:
   - Anpassa namn på knappar, VU-grindar, utgångar och boxar.
   - Exportera och importera inställningar som JSON.

8. **🌐 Full Bilingual Support**:
   - Växla sömlöst mellan **🇸🇪 Svenska** och **🇬🇧 English**.

---

## ⌨️ Tangentbordsgenvägar

| Shortcut | Action |
| :---: | :--- |
| **`P`** | Öppna **📄 Utskriftsrapport & Fordonsdokumentation** |
| **`E`** | Växla **🔋 Energisparläge (Eco Cutoff)** |
| **`V`** | Öppna/stäng **🌲 VU Port Tree** |
| **`M`** | Öppna/stäng **📡 CAN Matrix & Multi-File** |
| **`F`** | Öppna/stäng **🔍 Sektions- & Spårningsfilter** |
| **`Escape`** | Stäng aktiv modal eller panel |
| **`R`** | Återställ vy (pan och zoom) |
| **`0`** | Återställ alla insignaler och simuleringar |

---

## 🛠️ Stödda Hårdvarumodeller & Centraler

- **Addio Centraler**: 
  - DRB1612-4 (Nano 12V/24V Adv, 6 ingångar, 4 utgångar)
  - DRB5012-4-ADV / DRB4012 / DRB3012 / SCRE (4 ingångar, 4 utgångar)
  - DRB9012-8 ADV / CAN Master 8+8 / Slave 8+8 / Slave S / 22ch Input Unit
- **Styrenheter**:
  - Handkontroller (HK 1..15, Switch, Momentary, Service, PÅ/AV)
  - Manöverpaneler MP 1, MP 2, MP 3, MP 4 (8 knappar per panel, RGB LED, reflektionsutgångar)
- **Addio Firmware**: 1.3.17, 1.4.x, 1.8.x, 4.6.x, 4.7.x och nyare.
