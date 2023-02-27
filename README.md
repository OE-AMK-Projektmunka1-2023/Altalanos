# Általanos információk

## Csapatok összeállítása

A félév elején a kurzus hallgatóiból 2-3 fős csapatokat állítunk össze. Ennek megszervezése alapvetően a hallgatók feladata. Ezt
[Ennek a táblázatnak](https://docs.google.com/spreadsheets/d/1BPvd-QJT9Fd2HLqn0v-txxHA3oMNaa7M44eLx-d2CMs/edit#gid=0)
a segítségével lehet megtenni. Értelemszerűen a "csapat sorszáma" oszlopba kell beírni
a csapat sorszámát. A táblázatot később letisztázom és a kimaradó emberekből (ha
lesznek) véletlenszerűen állítok össze csapatokat.

## Verziókövetés

A kurzus egyik célja a Git használatának elsajátítása. Ez azt jelenti, hogy ahelyett,
hogy a csapattagok a kódrészleteket például e-mailben, Messengeren stb. osztanák meg
egymással, a változásokat Git használatával követik. Ez egyben azt is jelenti, hogy
a Git repositoryban nem csak a kész, működő verziónak kell szerepelnie, hanem látszani
kell annak is, hogy a félév során mi történik.

A csapatoknak a készülő kód és az egyéb fájlok mellett a dokumentációt is ugyanebben a
GitHub repositoryban kell (verziókövetve) tárolniuk.

Ehhez mindenkinek regisztrálnia kell a GitHubra és a felhasználónevét be kell írnia a
feljebb már említett [táblázatba](https://docs.google.com/spreadsheets/d/1BPvd-QJT9Fd2HLqn0v-txxHA3oMNaa7M44eLx-d2CMs/edit#gid=0). Ha ez megtörtént, a csapattagokat meghívom a megfelelő repositoryba.
A meghívás után a csapattag nevét **sárgára** színezem a táblázatban.

A meghívóról a GitHub e-mail értesítést küld, ahol egy linkre kattintva el is kell azt fogadni.
Ezt rendszeresen ellenőrzöm. Ha minden rendben van, akkor a táblázatban az adott személyt
**zöldre** állítom. Erre a folyamatra egy hét áll rendelkezésre. Aki ennek nem tesz határidőre eleget,
azt szankcionálni fogom.

A repository linkje a következőhöz hasonló lesz:
[https://github.com/OE-AMK-Projektmunka1-2023/PL2023A_20](https://github.com/OE-AMK-Projektmunka1-2023/PL2023A_20)

### A fejlesztői környezet beállítása a Githez

A fejlesztés első (vagy inkább nulladik) lépése a fejlesztőrendszer beállítása a Githez. A legtöbb
IDE képes a Gittel együttműködni, azonban mindegyiket egy kicsit máshogy kell beállítani. Egy
további lehetőség akár egy grafikus, akár az alap parancssoros Git kliens használata.

Addig senki ne kezdjen hozzá a fejlesztéshez, amíg a Git használata nem megy rutinszerűen.

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
csak **NE** használjuk a "file upload" funkciót!

A csapatok a félév során **rendszeresen** kell, hogy commitokat készítsenek.
Mivel a "rendszeresen" szónak való megfelelést nehéz utólag elbírálni,
így a következő konkrét mérőszámok az irányadóak. Egy valós fejlesztés
során persze ennél minimum egy nagyságrenddel több commit szokott születni.

**A kurzus során elvárás, hogy legyen legalább 10 olyan hét, amikor ÉRDEMI
változás történik a repositoryban és ezt a commitok dátuma is tükrözi.**

**Szintén elvárás, hogy minden csapattag esetében legyen legalább 3-3 olyan hét,
amikor az adott csapattagnak ÉRDEMI commitja van.**

Érdemi commit lehet akár egy egyeztetésről szóló bejegyzés az előrehaladási
naplóban, vagy akár valamilyen, a projekthez kapcsolódó ötlet, vagy kísérlet nyoma
(fotó, rövid leírás stb) is.

# Témák

A következőkben néhány témajavaslat kerül felsorolásra. Ezek nagyrészt nem
konkrét, minden tekintetben kidolgozott feladatok, hanem inkább ötletek.
A pontos részleteket pontosan emiatt minden esetben egyeztessük.

## Képfeldolgozási algoritmusokon alapuló projekt Webkamerával, vagy Raspberry Pi kamerával

Lehetséges projekt irányok:

  * Arcfelismerés, objektumfelismerés
  * Számok, vagy szövegek felismerése
  * Vonalkódok, QR kódok felismerése
  * Fiduciális markerek felismerése
  * Testpóz, vagy kézpóz felismerés

A megvalósításhoz Python és OpenCV használata ajánlott.

## Tangram társasjáték számítógépes megvalósítása

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

A projekt célja egy (például breadboardon összerakott) Arduino alapú hardverösszeállítás
és egy rajta futtatható, élvezhető játék elkészítése.

A vezérlőegység lehet például egy Arduino Uno, vagy egy ESP32. Megjelenítőként 128x64 pixeles
OLED kijelző használható. Az irányítóeszköz nyomóbombokból állhat.

Magára a játékra sokféle lehetőség van. Például lehet valamilyen labirintus, vagy logikai játék.

A fizikai hardver helyett Wokwi szimulátor is használható

## Okos otthon megvalósítása NodeRed segítséglvel

## WiFi aktivitás mérése Raspberry Pi segítségével

## Beszélő óra, beszélő konyhai időzítő

## Beszélő műszer

## Tranziens jelek vizsgálata Arduinoval


