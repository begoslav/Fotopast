### 1. Analýza požadavků
Na začátku bylo potřeba ujasnit si základní funkce zařízení:
- detekce pohybu v okolí pomocí senzoru,
- pořízení fotografie při detekci,
- uložení snímku,
- nízká spotřeba energie a autonomní provoz.

Zvažoval jsem, jaké komponenty budou cenově dostupné a zároveň snadno programovatelné. Rozhodl jsem se použít **Raspberry Pi**, protože je dobře zdokumentované, má přístup k GPIO a podporuje běh vlastního kódu i kamerových modulů.

---
### 2. Výběr hardwaru
- **Raspberry Pi 5** – hlavní výpočetní jednotka
- **RPi kamera** – pro pořízení snímků
- **PIR senzor** – pro detekci pohybu
- **MicroSD karta** – pro OS a úložiště

---
### 3. Návrh softwarového řešení
Navrhl jsem jednoduchou softwarovou architekturu:
- při spuštění se inicializuje senzor i kamera,
- systém neustále čeká na signál z PIR senzoru,
- při zaznamenání pohybu se pořídí fotografie a uloží do předem definované složky.

Vše bylo psáno v **Pythonu**, kvůli jeho jednoduchosti a rozsáhlé knihovní podpoře pro práci s GPIO i kamerou.

---
### 4. Testování funkčnosti jednotlivých částí
Během vývoje jsem každou část testoval samostatně:
- nejdříve detekce pohybu,
- poté integrace kamery,
- následně propojení obou funkcí dohromady,
- ladění načasování, stability a ošetření chyb

---
### 5. Integrace a optimalizace
Po ověření funkčnosti jednotlivých částí jsem celý systém spojil a začal testovat jako celek. Důraz byl kladen na:
- co nejnižší latenci mezi detekcí pohybu a pořízením snímku,
- správné ukládání souborů včetně názvů s časovým razítkem

---
### 6. Dokončení, automatické spouštění a dokumentace
Po otestování funkčního prototypu jsem doplnil skript pro **automatické spuštění při startu Raspberry Pi**, aby zařízení mohlo fungovat bez nutnosti manuálního zásahu. Následně jsem připravil dokumentaci projektu, včetně technického popisu, testovacích scénářů a možnosti budoucího rozšíření.
