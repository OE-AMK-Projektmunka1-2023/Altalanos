# Általanos információk

## Csapatok összeállítása

A félév elején a kurzus hallgatóiból 2-3 fős csapatokat állítunk össze. Ennek megszervezése alapvetően a hallgatók feladata. Ezt
[Ennek a táblázatnak](https://docs.google.com/spreadsheets/d/1IrYP29BsdDP29CFXExsv_rgTbKuD0-In80B1lQNJsZ4/edit#gid=0)
a segítségével lehet megtenni. Értelemszerűen a "csapat sorszáma" oszlopba kell beírni
a csapat sorszámát. A táblázatot később letisztázom és a kimaradó emberekből (ha
lesznek) véletlenszerűen állítok össze csapatokat.

## Verziókövetés

A csapatoknak a készülő kódot és a dokumentációt egy GitHub repositoryban kell
verziókövetve tárolniuk. Ehhez mindenkinek regisztrálnia kell a GitHubra és
a felhasználónevét be kell írnia a feljebb már említett [táblázatba](https://docs.google.com/spreadsheets/d/1IrYP29BsdDP29CFXExsv_rgTbKuD0-In80B1lQNJsZ4/edit#gid=0).

Minden csapatnak létre fogok hozni egy repositoryt, aminek a linkje
például a következő lehet:
[https://github.com/OE-AMK-Projektmunka2-2022/PL2022B_20](https://github.com/OE-AMK-Projektmunka2-2022/PL2022B_20)

A GitHub használatát egy másik dokumentum tartalmazza.

### README.md

A repositoryban levő README.md fájl a projekt rövid összefoglalója.
Itt szerepelhet például:

 * A csapattagok névsora, Neptun kódja, esetleg elérhetősége
 * A projekt neve, elnevezése
 * A projektről néhány mondat, amiből képet kapunk arról, hogy mit csinál a csapat
 * A felhasznált technológiák, programnyelvek
 * Az előrehaladási napló (nagyobb mérföldkövek; mit csinált a csapat)

A README.md formátuma MarkDown, ami egy egyszerű szövegformázó (markup) nyelv.
Rövid leírás például [itt](https://www.markdownguide.org/basic-syntax/).

**A README.md naprakészen tartása elvárás a kurzus teljesítéséhez.**

### .gitignore

A .gitignore fájl arra való, hogy bizonyos fájlokat automatikusan figyelmen kívül
hagyjunk a verziókövetés során. Ezek például a projekt fordítása során létrejövő,
a forráskódból generált fájlok. Interneten számos példa lelhető fel ezzel kapcsolatban.
Egy kiindulási alap lehet például
[ez a gyűjtemény](https://github.com/github/gitignore).

**A .gitignore fájlnak az adott fejlesztőeszközhöz passzoló kitöltése elvárás
a kurzus teljesítéséhez.**

### Könyvtárstruktúra

A repositoryban külön könyvtárban kell elhelyezni a projekt forráskódját (és a
kapcsolódó egyéb fájlokat), a dokumentációt, illetve az egyéb állományokat.
Néhány példa:

 * **src**: A projekthez tartozó forráskódok
 * **firmware**: Az esetleges mikrovezérlős forráskódok
 * **docs**: Dokumentációk
 * **schematics**: Kapcsolási rajzok
 * **screenshots**: Képernyőképek

**A kurzus során elvárás a tiszta könyvtárszerkezet használata.**

### Commitok

A változásokat commitok formájában lehet a verziókövetőbe feltölteni. Minden
commithoz szükséges kitölteni a "commit message"-et is. A feltöltéshez
csak végső esetben használjuk a "file upload" funkciót!

**A kurzus során elvárás, hogy legyen legalább 10 olyan hét, amikor ÉRDEMI
változás történik a repositoryban és ezt a commitok dátuma is tükrözi.**

**Szintén elvárás, hogy minden csapattag esetében legyen legalább 3-3 olyan hét,
amikor az adott csapattagnak ÉRDEMI commitja van.**

Érdemi commit lehet akár egy egyeztetésről szóló bejegyzés az előrehaladási
naplóban, vagy akár valamilyen, a projekthez kapcsolódó ötlet, vagy kísérlet nyoma
(fotó, rövid leírás stb) is.

# Témák

A következőkben néhány témajavaslat kerül felsorolásra. Ezek egy része konkrét,
de vannak általános, sokféle irányba elvihető ötletek is.

## Rubik kocka kirakását segítő program

A projekt célja egy olyan program létrehozása, ami egy összekevert Rubik kockáról
webkamera segítségével különböző szögekből felvételeket készít, felismeri az
egyes elemek helyzetét, majd egy lehetséges kirakást generál.

Az egyes megvalósítandó elemek a következők:

 * Webkamera kezelésének megoldása, képek automatizált készítése
 * Kockaelemek színének azonosítása
 * Kockaállapotok és forgatások modellezése
 * Forgatási sorrend generálása

A megvalósításhoz Python és OpenCV használata ajánlott.

## Kártyák kombinálásán, mozgatásán alapuló társasjáték online megvalósítása

Az Imagine egy olyan tásasjáték, ahol valamilyen feladványt (például
egy szót, kifejezést, közmondást, film, vagy zenecímet) kell kártyák
segítségével elmagyarázni. Az átlátszó kártyákon valamilyen (sok esetben többértelmű,
vagy absztrakt) ábra van, amiket egymásra tehetünk, vagy akár mozgathatunk
(animálhatunk) is.

A projekt célja, hogy egy, az Imagine-hez hasonló játékot hozzunk
létre, amit online játszhatunk. Az eredeti játékhoz sem a feladványok,
sem a konkrét kártyák tekintetében nem feltétlenül ragaszkodni.

Az egyes megvalósítandó elemek a következők:

 * Kártyák és feladványok megszerkesztése
 * Kártyák kiválasztása és felrakása a játéktérre
 * Kártyák levétele a játéktárről
 * Kártyák mozgatása
 * Rámutatás, letakarás lehetőségének megoldása
 * Játéktér megjelenítése egyetlen számítógépen
 * Játéktér folyamatos szinkronizációja az egyes számítógépek között
(felhő szolgáltatáson, web backenden, centralizált szerveren keresztül stb.)
 * Az egyes játékosok összekapcsolásának megoldása, authentikáció

Az eredeti játékban lehetőség van a kártyák három dimenzióban való mozgatására is.
Ettől ebben az esetben el kell tekintenünk. Nincs szükség továbbá a játék közben
a hang átvitelének megoldására sem (erre már számos egyéb megoldás rendelkezésre
áll).

A játék akár webalkalmazásként, akár desktop programként elképzelhető.

## Kártya alapú társasjáték online megvalósítása

Számos olyan társasjáték létezik, amit nagyrészt, vagy teljes egészében kártyákkal
kell játszani. Míg a hagyományos kártyajátékokra (például poker, snapszer, ulti)
számos online megoldás létezik, az újabb típusú kártyajátékok közül ez csak
néhányról mondható el (például az Exploding Kittens-nek és az EladLak!-nak van
online változata, viszont a Travelin'-nek nincs).

Általában ezek a játékok a következő főbb játékelemekből építkeznek:

 * A játékosoknál levő lapok, amelyekből egy adott mennyiségű a játék elején
kerül kiosztásra
 * Húzópakli, amiből bizonyos alkalmakkor (például a játékos körének elején,
vagy bizonyos kártyák aktiválásakor) megadott mennyiségű lapot fel kell húzni
 * Dobópakli, ahova a felhasznált lapok kerülnek és azonnan bizonyos játékok
esetén szintén húzhatunk
 * Kijátszott kártyák (általában pontértékkel), amiket minden játékos maga előtt gyűjt
 * Kezdőjátékos kiválasztásának szabálya
 * A kör iránya (bizonyos játékoknál ez megfordítható)
 * Kártyatípusok (például akciókártyák, támadó és támadást kivédő kártyák, körön kívül
is felhasználhatunk
 * "Játék vége" feltétel
 * Nyertes kiválasztására vonatkozó szabály

Az egyes megvalósítandó elemek a következők:

 * Játék kiválasztása, vagy kigondolása
 * Kártyalapok elkészítése
 * Kártyák követése (melyik kártya hol van, húzópakli és dobópakli sorrendje, adatszerkezetek megtervezése
 * Játéktér kinézetének megtervezése (kezünkben levő lapok, kijátszott lapok stb.)
 * Aktuálisan következő játékos követése
 * Játékos körében elvégzendő feladatok végigkövetése, választási lehetőségek felajánlása
 * Felhasználói interakciók kidolgozása (hogyan tudunk kijátszani egy kártyát, hogyan tudunk akciókat összekombinálni, esetleg passzolni, támadás esetén támadott játékost kiválasztani stb.)
 * Akciók validálása (például ne tudjunk több lapot felhúzni, mint amennyit szabad,
ne tudjunk már kijátszott lapot újra kijátszani stb.)
 * "Játék vége" feltétel figyelése, győztes kiválasztása
 * Játéktér megjelenítése egyetlen számítógépen
 * Játéktér szinkronizációja az egyes számítógépek között
(felhő szolgáltatáson, web backenden, centralizált szerveren keresztül stb.)
 * Az egyes játékosok összekapcsolásának megoldása, authentikáció

A játék akár webalkalmazásként, akár desktop programként elképzelhető.

## Tangram társasjáték online megvalósítása

A tangram egy ősi kínai logikai játék, melynek célja, hogy egy,
a körvonalával meghatározott formát előre meghatározott síkidomokból
(kövekből) kirakjunk. Az eredeti játéktól kissé eltérő formájú
kövekből áll a magyar "Ezt rakd ki".

![Ezt rakd ki játék](images/eztrakdki1.jpg)

Az "Ezt rakj ki" néhány feladványa:

![Ezt rakd ki példák](images/eztrakdki1.jpg)

A cél akár a kínai, akár a magyar verzió megvalósítása
számítógépes program formájában.

Az egyes megvalósítandó elemek a következők:

 * Feladványok definícióinak leírása
 * Játékmező kialakítása, feladvány kiválasztása, megoldott
 feladványok számon tartása
 * Játék irányításának kidolgozása
 * Kövek mozgatásának megvalósítása
 * Megoldott feladat folyamatos ellenőrzése
 * Közös feladatmegoldás biztosítása (opcionális)

A játék akár webalkalmazásként, akár desktop programként, vagy mobil
allként elképzelhető.

## Játék Arduinoval és OLED kijelzővel

## Beszélő óra, beszélő konyhai időzítő

## Beszélő ellenállásmérő

