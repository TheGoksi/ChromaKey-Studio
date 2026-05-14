# 🎬 VFX Chroma Key & Color Grading Studio

> **Interaktívna webová aplikácia pre real-time odstránenie zeleného plátna, spájanie obrazu a filmový post-processing.**

Tento projekt slúži ako plne funkčné, klientske (client-side) vizuálne štúdio bežiace priamo vo webovom prehliadači. Bez potreby akéhokoľvek backendu dokáže v reálnom čase spracovávať fotografie a bežiace video, aplikovať na ne efekty a následne ich vyexportovať. Je navrhnutý tak, aby priniesol okamžitý vizuálny "WOW efekt" s dôrazom na kinematografickú estetiku.

---

## ✨ Kľúčové funkcie (Features)

* 🟢 **Real-time Chroma Keying:** Odstránenie zeleného (alebo iného) plátna nielen zo statických fotiek, ale aj z bežiaceho videa pomocou HTML5 Canvas.
* 🎯 **Smart Color Picker:** Možnosť vybrať si kľúčovaciu farbu jednoduchým kliknutím priamo na plátno (podpora pre Green Screen, Blue Screen a ďalšie).
* 🎛️ **Soft-Edge Tolerancia:** Precízny posuvník na nastavenie tolerancie s algoritmom na vyhladzovanie hrán (spill suppression), aby objekty nevyzerali umelo vystrihnuté.
* 🎨 **Filmový Color Grading:** Okamžitá aplikácia vizuálnych filtrov, ktoré zjednotia nasvietenie scény:
  * *Akčný Thriller* (Vysoký kontrast a saturácia)
  * *Neo-Noir* (Drsný čiernobiely vizuál)
  * *Sci-Fi / Matrix* (Ikonický zelený nádych)
  * *Post-Apo* (Temné, vyblednuté tóny)
* 💾 **Natívny Export:** Možnosť jedným kliknutím stiahnuť aktuálnu snímku (`.png`) alebo nahrať a vyexportovať upravené video (`.webm`) pomocou natívneho MediaRecorder API.

---

## 🚀 Ako spustiť projekt

Keďže aplikácia spĺňa prísne obmedzenia a nevyžaduje **žiadny bežiaci backend** (žiadny Flask, Node.js ani Java), jej spustenie je maximálne jednoduché:

1. Stiahni si tento repozitár (alebo použi `git clone`).
2. Otvor súbor `index.html` v akomkoľvek modernom webovom prehliadači (Chrome, Edge, Firefox, Safari).
3. Aplikácia je okamžite pripravená na použitie.

---

## 🛠️ Návod na použitie

1. **Nahraj objekt (Video/Obraz):** Klikni na prvé tlačidlo a nahraj svoj zdrojový súbor s jednofarebným pozadím (odporúča sa zelené plátno). *Podporované sú obrázky aj .mp4 videá.*
2. **Nahraj nové prostredie:** Klikni na druhé tlačidlo a nahraj obrázok pozadia (napr. filmovú scénu, pódium alebo abstraktný priestor), do ktorého chceš objekt zasadiť.
3. **Doladenie kľúčovania:** Posúvaj slider "Tolerancia", kým pôvodné pozadie úplne nezmizne. Ak má tvoj objekt iné ako zelené pozadie, **klikni myšou priamo na video/obrázok** na farbu, ktorú chceš vymazať.
4. **Color Grading:** Vyber si z rolovacieho menu filmový filter, ktorý najlepšie prepojí atmosféru objektu s novým pozadím.
5. **Export:** * Pre obrázok klikni na `💾 Snímka`.
   * Pre záznam videa klikni na `🔴 Nahrávať video`, nechaj scénu chvíľu bežať a potom klikni na `⏹️ Zastaviť a stiahnuť`.

---

## ⚙️ Technické pozadie

Aplikácia je postavená výlučne na moderných webových štandardoch:
* **HTML5 & Vanilla JavaScript:** Žiadne externé knižnice ani frameworky.
* **Canvas API:** Real-time analýza pixelov a výpočet euklidovskej vzdialenosti farieb (RGB kanály a manipulácia s Alpha kanálom).
* **MediaStream Recording API:** Zachytávanie dynamického canvasu a kódovanie videa priamo na grafickej karte používateľa.
* **CSS Filters:** Hardvérovo akcelerovaný post-processing obrazu.
