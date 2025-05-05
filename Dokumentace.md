# Anotace

Tato práce se zabývá vývojem a implementací fotopasti na platformě Raspberry Pi. Zařízení je schopné automaticky detekovat pohyb a pořizovat fotografie okolního prostředí, které může následně ukládat.

---
# Úvod

Projekt fotopasti vznikl jako ukázka využití Raspberry Pi. Hlavní funkcí zařízení je pořizování fotografií při detekci pohybu v monitorovaném prostoru. Za tímto účelem byl použit pohybový senzor PIR a kamera kompatibilní s Raspberry Pi. Cílem bylo vytvořit jednoduchý, spolehlivý a levný systém, který lze využít v různých situacích – zabezpečení objektu, nebo jako vzdělávací projekt.

Projekt klade důraz na jednoduchost implementace a snadnou rozšiřitelnost. Všechen kód je open-source a zařízení může být dále upraveno pro specifické potřeby. Výsledný systém je autonomní, napájený pomocí 5V / 3A napájecího adaptéru a podporuje ukládání snímků na SD kartu.

---

# Vývoj

## Použité technologie::
- Raspberry Pi 5 (8 GB RAM)
- RPi Kamera
- PIR pohybový senzor
- Napájení: 5V / 3A
- Programovací jazyk: Python

## Průběh vývoje:
Nejprve bylo navrženo základní zapojení. Následně byl napsán jednoduchý skript pro snímání pohybu.

---

## Architektura systému
1. PIR senzor detekuje pohyb.
2. Kamera pořídí snímek
3. Snímek je poté uložen na SD kartu v RPi

---
## Github

https://github.com/begoslav/Fotopast.git

---
# Závěr

Projekt fotopasti ukázal, že pomocí jednoduchých komponent lze postavit funkční a přizpůsobitelný bezpečnostní systém. Během vývoje jsem si osvojil práci s GPIO piny, programováním senzorů a správou souborů v prostředí Linuxu. Výsledkem je stabilní aplikace, kterou lze snadno nasadit a rozšířit. Projekt mi zároveň poskytl praktické zkušenosti s reálným nasazením zařízení a dokumentací softwarového řešení.