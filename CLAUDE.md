# Projekt: "Mit tanulhatsz nálunk?" demóoldal 8. osztályosoknak

## Cél
Egy ~15 perces iskolabemutatóhoz készült, telefonbarát, magyar nyelvű weboldal, amit a 8. osztályos diákok QR-kóddal nyitnak meg. A bemutató nagy része beszéd az iskoláról, az oldal ezt támogatja. A diákok legfeljebb 1–2 dolgot próbálnak ki. Az oldal ingyenes GitHub Pageson fut, a változtatások git push után 1–2 percen belül élesednek (ezt a bemutatón is meg lehet mutatni "élő frissítésként").

## Felhasználó
Informatikatanár (magyarul kommunikál). Tanít: Python (10. évf.), SQL (11.), C# szoftvertesztelés xUnit-tal, 9. évfolyam. Az iskolában AI-nagykövet. Az oldal és minden szöveg magyarul legyen.

## Tanterv (a felhasználó adata)
- **9. évf.:** HTML és CSS (ágazati alap, mindenki)
- **10. évf.:** Python (ágazati alap, mindenki)
- 9–10. évfolyamon az összes informatikás diák ugyanazt tanulja az ágazati alapvizsgáig. A hivatalos alapoktatásban emellett hardver, operációs rendszerek, hálózat, elektronika és AI-betekintés is van (a KKK szerint).
- **Az alapvizsga után két szakma.** Nem az alapvizsga után választanak: a diák már a jelentkezéskor eldönti a szakmát, és az alapvizsga után abban folytatja. A bemutató csak a szoftveres ágat mutatja be részletesen.
  - **Szoftverfejlesztő és -tesztelő:** a programozás folytatódik.
    - 11. évf.: JavaScript, adatbázisok (SQL)
    - 12. évf.: C# asztali alkalmazások, objektumorientált programozás, tesztelés
    - 13. évf.: frontend, backend, REST API
  - **Informatikai rendszer- és alkalmazás-üzemeltető technikus:** itt már nincs programozás (a tartalma még nincs megadva).

## Tartalmi döntések
- A 8.-osoknak szóló szövegek legyenek **egyszerűek, szakkifejezések nélkül** (hasonlatok: ház a HTML/CSS-hez, étterem a frontend/backend/REST API-hoz).
- A **React nevet ne írd ki**, a 13. évfolyamnál "Frontend, backend és REST API" szerepel.
- Az üzemeltetős ágnál csak annyi áll, hogy nincs programozás, és erről külön mesélnek. Részletek: a felhasználó még megadja.
- Nem szerepel (nem tudjuk, tanítják-e): mobilalkalmazás-fejlesztés, WordPress/CMS.

## Felépítés
- `index.html`: az egész oldal (HTML, CSS, JS egy fájlban)
  - 9. évf. demó: CSS-labor, csúszkákkal állítható kártya és élő CSS-kód
  - 10. évf. demó: Python (Skulpt turtle) névből rajzolt egyedi minta, szerkeszthető kóddal
  - szakirányválasztó rész, majd 11–13. évfolyam csempék
- `lib/skulpt.min.js`, `lib/skulpt-stdlib.js`: a böngészőben futó Python (Skulpt 1.2.0), **helyben tárolva** (nem CDN), hogy az iskolai wifin is működjön.

## Műszaki tudnivalók
- Skulptban nincs `turtle.bgcolor()`, helyette `turtle.Screen().bgcolor("black")` kell.
- A rajzterület (`#rajz-in`) fix 420 px, CSS `transform: scale()` igazítja a képernyő szélességéhez.
- Tesztelés: `python3 -m http.server`, majd Playwright (mobil nézet, 390 px szélesség) vagy a böngésző. Ellenőrizd, hogy a `#hiba` elem üres marad.
- Nincs buildlépés: a fájlokat közvetlenül tölti fel a GitHub Pages.

## Teendők
1. GitHub Pages bekapcsolása (public repo, `main` ág, `/` mappa), élő cím rögzítése ide.
2. QR-kód készítése az élő címből (kivetíthető kép).
3. Üzemeltetős ág tartalmának kitöltése, ha a felhasználó megadja.
4. Opcionális: SQL-nyomozó vagy AI-kamera mini-demó, C#-projekt képernyőképe a 12. évfolyamhoz.

## Élő cím
(ide kerül: https://FELHASZNALONEV.github.io/REPO/)
