# Speciális funkciók

## Modellenkénti paraméterek

A SuperSlicerrel egyszerre több modell nyomtatható ki, mindegyik kissé eltérő beállításokkal. Például más kitöltési vagy rétegmagassággal.

Kattintson a jobb gombbal \(Speciális mód\) egy modellre, és válassza a következőket:

* **Kerületek és héj**
* **Kitöltés**
* **Támaszték**

A **Szakértő** módban egy további **Beállítások hozzáadása** opció áll rendelkezésre, amely lehetővé teszi az olyan paraméterek beállítását, mint a sebesség, az extrudálás szélessége, a kitöltés/perem átfedés és így tovább.

![Jobb gomb a modellen](../.gitbook/assets/advanced_functionality_001.png)

Az objektumlistában a jobb gombbal kattinthat a szerkesztés ikonra is.

![Objektumlist&#xE1;ba](../.gitbook/assets/advanced_functionality_002.png)

A jobb oldali panelen egy új ablak jelenik meg **A módosítandó objektum beállításai** címmel. Ezeknek a beállításoknak a módosítása **csak az adott objektumot és annak példányait** érinti. A kicserélt beállításokat a piros kereszt ikonra kattintva törölheti. Ha így tesz, a globális beállítások ismét alkalmazásra kerülnek.

## Színváltás

A SuperSlicer lehetővé teszi, hogy egy bizonyos rétegnél ütemezze a szálcserét. Ez alapvető többszínű modellek nyomtatására használható. A nyomtató automatikusan leállítja a nyomtatást, amint a G-kódban \(M600 parancs\) a színváltozást olvassa, és felszólítja a felhasználót a szálcserére.

1. A színváltoztatás a [**szeletelés előnézet**](../felhasznaloi-feluelet/user_interface.md#szeleteles-elonezet) ablakból illeszthető be.
2. Húzza a **réteg csúszkát** jobbra a célréteg kiválasztásához.
3. Ön vagy 
   1. Kattintson a bal gombbal a **kék plusz ikonra** a színváltoztatáshoz \(véletlenszerű előnézeti szín\).
   2. Kattintson a jobb gombbal **a kék plusz ikonra,** és válassza a **Színváltás** hozzáadása lehetőséget. Megjelenik egy színválasztó ablak, amely lehetővé teszi a kívánt szín kiválasztását a pontosabb előnézethez.
4. Ha megismétli, annyi színváltozást adhat hozzá, amennyit csak akar.

![K&#xE9;p: Sz&#xE1;lv&#xE1;lt&#xE1;s egy bizonyos r&#xE9;tegn&#xE9;l](../.gitbook/assets/advanced_functionality_003.jpg)

A színváltozást **eltávolíthatja**, ha a kurzort a célréteg fölé mozgatja, és a szürke kereszt ikonra kattint a bal gombbal.

A színváltoztatás előnézetét **szerkesztheti**, ha a kurzort a célréteg fölé mozgatja, és a jobb gombbal a szürke kereszt ikonra kattint.

Azonnal megjelenik egy előnézet, így pontosan láthatja, hogyan fog kinézni a modellje a színváltoztatással.

Ne feledje, hogy **azonos típusú** szálakat kell használnia, mindig keverje a PLA-t a PLA-val, a PETG-t a PETG-vel és így tovább. A különböző típusú anyagok keverése valószínűleg sikertelen nyomtatást eredményez, mivel nem tapadnak jól egymáshoz.

**A színváltozások idejének becslése**

Ha egy vagy több színváltozást ad hozzá, a szeletelési információs panel tartalmazza az egyes színváltozásokig tartó nyomtatási idő becsült értékét. Így megtervezheti, hogy mikor ellenőrizze a nyomtatót a színváltoztatáshoz.

![A sz&#xED;nv&#xE1;ltoz&#xE1;sok id&#x151;becsl&#xE9;se](../.gitbook/assets/advanced_functionality_004.jpg)

**Kapcsolja ki a színváltó hangjelzőt**.

Ha a színváltás becsült ideje éjszaka vagy más kényelmetlen időpontban következik be, akkor a nyomtató hangjelzését _\[Néma\]_, vagy _\[Egyszer\]_ hangjelzésre állíthatja. Ez a _beállítások_, az LCD menüben található.

## Módosítók

Bizonyos esetekben előfordulhat, hogy **más beállításokat csak a modell egy bizonyos szakaszán szeretne megváltoztatni**. Például előfordulhat, hogy a modell egy részének sűrűbb kitöltést vagy több kerületet szeretne a nagyobb merevség érdekében. Ezeket a beállításokat azonban nem érdemes globálisan beállítani, mert az rengeteg anyagot pazarolna, és megnövelné a nyomtatási időt.

Többféleképpen is megadható, hogy a modell mely szakaszára legyenek hatással az egyéni beállítások. Használhat egy magassági tartomány módosítót, egy egyszerű módosító háló primitívet \(például egy kockát\) vagy egy egyéni modell módosító hálót.

### Magassági tartomány módosító

Kattintson a **jobb gombbal** egy sablonra, és válassza a **Magassági tartomány módosító** parancsot a felugró menüben.

![Magass&#xE1;gi tartom&#xE1;ny m&#xF3;dos&#xED;t&#xF3;](../.gitbook/assets/advanced_functionality_005.jpg)

A jobb oldali panelen egy új ablak jelenik meg **Magassági tartományok** néven. Itt olyan intervallumokat határozhat meg, amelyek között különböző beállításokat alkalmazhat. Amikor meghatároz egy tartományt, az megjelenik a jobb oldali panel objektumlistájában.

A kék **plusz** és **mínusz** ikonokkal intervallumokat adhat hozzá vagy távolíthat el.

Ha az intervallum melletti fogaskerék ikonra kattint, választhatja a konfigurálást:

**Haladó mód** - egyéni kitöltés, rétegek és peremek vagy médiumok

**Szakértő mód** - egyéni kitöltés, rétegek és kerület, támaszok, extrudálás szélessége, sebesség és számos más paraméter.

![Magass&#xE1;gi tartom&#xE1;nyok meghat&#xE1;roz&#xE1;sa](../.gitbook/assets/advanced_functionality_006.jpg)

Az intervallumbeállításnak van egy **rétegmagasság bemeneti értéke** is. Alapértelmezés szerint a globális rétegbeállítás kerül alkalmazásra, de választhatja, hogy a modellt más rétegmagassággal szeletelje, és ez a változás csak a modellt érinti. Ne feledje, hogy ha az egész modellre más rétegmagasságot állít be a magasságintervallumon, akkor azt ez az érték felülírja.

![Egy magass&#xE1;gi tartom&#xE1;ny m&#xF3;dos&#xED;t&#xF3;t haszn&#xE1;ltunk, hogy a fels&#x151; &#xE9;s als&#xF3; r&#xE9;teget 0-ra &#xE1;ll&#xED;tsuk, &#xE9;s a modell als&#xF3; \(fekete\) r&#xE9;sz&#xE9;nek kit&#xF6;lt&#xE9;si mint&#xE1;j&#xE1;t h&#xE1;romsz&#xF6;gekre v&#xE1;ltoztattuk.\(Prusa k&#xE9;p\)](../.gitbook/assets/advanced_functionality_007.jpg)

### Módosító hozzáadása

A módosító háló egyéni beállításokat alkalmaz a módosító háló és a modell metszéspontjára.

Kattintson a jobb gombbal egy modellre, és válassza a **Módosító hozzáadása - \[Módosító típusának kiválasztása\]** lehetőséget. Az objektumlista panelen a jobb gombbal a fogaskerék ikonra is kattinthat.

![M&#xF3;dos&#xED;t&#xF3; hozz&#xE1;ad&#xE1;sa](../.gitbook/assets/advanced_functionality_008.jpg)

#### _A módosító háló formája_

4 primitív - kocka, henger, gömb és blokk - közül választhat.

Ezenkívül szakértői módban egy **egyéni alakzatot módosító hálóként** is használhat, ha a háló kiválasztásánál kiválasztja a **Betöltés...** parancsot. Ez a háló általában olyasmi, amit korábban már modellezett egy 3D-s modellező programban.

![Egy t&#xE9;glalap alak&#xFA; m&#xF3;dos&#xED;t&#xF3; h&#xE1;l&#xF3;, amely elt&#xE1;vol&#xED;tja a fels&#x151; &#xE9;s als&#xF3; szil&#xE1;rd r&#xE9;tegeket, &#xE9;s egy m&#xE1;sik s&#xED;k alak&#xFA; h&#xE1;l&#xF3;, amely &#xFA;jra aktiv&#xE1;lja &#x151;ket, &#xE9;s megv&#xE1;ltoztatja az extruder 2-es sz&#xE1;m&#xFA;ra \(az MMU2S-sel nyomtatva\) \(Prusa k&#xE9;p\)](../.gitbook/assets/advanced_functionality_009.jpg)

Ha kiválasztja a módosító alakzatot \(például a kockát\), az megjelenik a 3D nézetben és a jobb oldali panel objektumlistájában.

A módosítási háló átalakításához a már ismert Mozgatás, Forgatás és Méretváltoztatás eszközöket használhatja.

#### _A módosító háló paramétereinek módosítása_

A kiválasztáshoz **jobb egérgombbal kattinthat a módosítóra** a 3D nézetben, vagy az objektumlista panelen a **fogaskerék ikonra** kattintva:

* **Haladó mód** - egyéni kitöltés, rétegek és kerületek vagy támasztékok
* **Szakértői mód** - egyéni kitöltés, rétegek és kerületek, támasztékok, extrudálás szélessége, sebesség és sok más paraméter

![A m&#xF3;dos&#xED;t&#xF3; h&#xE1;l&#xF3; param&#xE9;tereinek m&#xF3;dos&#xED;t&#xE1;sa](../.gitbook/assets/advanced_functionality_010.jpg)

Ha átméretezi a modellt, a modell és a módosító háló mérete is változik. A módosító háló megtartja méretét és a modellhez viszonyított helyzetét.

#### _Tegye a módosítót a lemezre_

Ha egy módosítót áthelyezett a nyomtatási lemez fölé, akkor a Tárgy módosító panel segítségével visszateheti azt a nyomtatási lemezre.

![T&#xE1;rgy m&#xF3;dos&#xED;t&#xF3; panel haszn&#xE1;lata](../.gitbook/assets/advanced_functionality_011.jpg)

### Támaszték kényszerítő hozzáadása

**A támaszték kényszerítő lehetővé teszik, hogy a kívánt helyeken hozzáadja támasztékot.**

Kattintson a jobb gombbal egy modellre, és válassza a **Támaszték kényszerítő hozzáadása** lehetőséget.

### Támaszték blokkoló hozzáadása

**A támaszték blokkoló lehetővé teszik, hogy a kívánt helyeken ne generáljon automatikusan támasztékokat.**

**Kattintson a jobb gombbal** egy modellre, és válassza a **Támaszték blokkoló hozzáadása** lehetőséget. A támaszblokkoló megakadályozza a támasz kialakulását azon a területen, ahol elhelyezték.

### Adja hozzá a csatlakozás pozícióját

**Az illesztési pozíció gömbökkel megadhatja, hogy az illesztések hol helyezkedjenek el.**

**Kattintson a jobb gombbal** egy modellre, és válassza a **Csatlakozási pozíció hozzáadása** parancsot.

Létrejön egy gömb, amelyet az illesztés kívánt területén lehet elhelyezni. Az illesztések a gömb közelében jönnek létre. A gömb létrehozása után a Rész kezelőpanel lehetővé teszi a gömb helyzetének módosítását a részhez képest.

A gömb által meghatározott illesztési pozíció elsőbbséget élvez a többi illesztési beállítással szemben.

![G&#xF6;mb hozz&#xE1;ad&#xE1;sa az illeszt&#xE9;s pozicion&#xE1;l&#xE1;s&#xE1;hoz](../.gitbook/assets/advanced_functionality_012.png)

## Újratöltés lemezről

Ez a funkció ideális, ha létrehozott egy **újabb verziót a modelljéből**, és a SuperSlicerben szeretné kicserélni a régi verziót anélkül, hogy újra be kellene állítania az olyan dolgokat, mint az egyéni támaszok vagy a módosító hálók.

**Jobb egérgombbal kattintson** egy modellre a 3D nézetben, és válassza a kontextusmenüben a **Töltse be újra a lemezről** parancsot.

![Jobb eg&#xE9;rgombos m&#xF3;dszer](../.gitbook/assets/advanced_functionality_013.jpg)

Az objektumlistában \(jobb oldalon\) a _szerkesztés_ ikonra is kattinthat.

![Objektumlist&#xE1;s m&#xF3;dszer](../.gitbook/assets/advanced_functionality_014.jpg)

A lemezről történő újratöltés még **egyéni módosító hálószemek** esetén is működik, amelyeket szakértői módban adhat hozzá.

### Újratöltés lemezről 3MF fájlok esetén

A 3MF projektfájl újbóli megnyitásakor választhatja az egyik modell újratöltését is.

Alapértelmezés szerint a 3MF projektfájlok nem mentik el a forrás modell teljes elérési útvonalát, mivel ez biztonsági kockázatot jelenthet egy ilyen fájl megosztásakor. Ha a teljes elérési útvonal nincs elmentve, és a **Betöltés lemezről** funkciót kéri, a SuperSlicer megkérdezi a forrásfájl helyét.

**Miért van alapértelmezés szerint letiltva a teljes elérési útvonal naplózása?**

A 3MF formátum lényegében egy zip-archívum, amely ember által olvasható XML-fájlokat, egy miniatűr képet és néhány egyéb fájlt tartalmaz. A 3MF fájlformátum egyik előnye, hogy az XML-fájlok ember által olvashatóak. Bizonyos esetekben azonban előfordulhat, hogy nem szeretné felfedni a modellfájlok helyét, például : _C:\Masociété\MonProjetSecret\MonAmis\_son\_cadeau.stl_

## Szünet vagy egyéni G-kód beillesztése a rétegbe

### Szünet beillesztése egy rétegbe

A szünet bizonyos magasságban történő beillesztésével mágneseket, súlyokat vagy anyákat helyezhet be a nyomatokba. Amikor folytatja a nyomtatást, ezeket a beillesztett objektumokat a következő rétegek fogják fedni.

1. A szünet beilleszthető [**a szeletelés előnézet**](../felhasznaloi-feluelet/user_interface.md#szeleteles-elonezet)
2. * Húzza a **réteg csúszkát** jobbra a célréteg kiválasztásához.
   * Kattintson a jobb gombbal\*\* a kék plusz ikonra
3. Válassza ki a **Nyomtatási szünet beillesztése \(M601\)** lehetőséget.
   1. A szünet **a kiválasztott réteg nyomtatása előtt** kerül beillesztésre.
4. A nyomtatás szüneteltetésekor a nyomtató LCD-képernyőjén megjelenő rövid üzenet beillesztése.
   1. Például: "_Helyezze a betéteket a nyílásokba, és folytassa a nyomtatást._"
5. Erősítse meg az **OK** gomb megnyomásával.

![Sz&#xFC;net beilleszt&#xE9;se egy r&#xE9;tegbe](../.gitbook/assets/advanced_functionality_015.jpg)

A szünetet **eltörölheti**, ha a kurzort a szünet réteg fölé mozgatja, és a szürke kereszt ikonra kattint a bal gombbal.

A kék fogaskerék ikonra jobb gombbal kattintva **szerkesztheti** a szünetüzenetet.

![Szerkeszt&#xE9;si funkci&#xF3;k](../.gitbook/assets/advanced_functionality_016.jpg)

A SuperSlicer 2.2 vagy újabb verzióra van szükség a Szünet beillesztése és az Egyéni G-kód beillesztése funkciók eléréséhez.

Ha a nyomtatási szünetek beillesztésével újra szeleteli a nyomtatást, akkor **becsült időt kap az egyes szünetekig**. A nyomtató a szünetet egy hangjelzéssel is jelzi.

A **mágnesek** behelyezésekor azokat szilárdan be kell helyezni a nyílásukba. Ellenkező esetben a nyomtatófejhez tapadnak, amikor az áthalad rajtuk. Vagy tervezze a nyílásokat szűk tűréshatárral, vagy használjon egy kis **csepp szuperragasztót**, hogy a helyükön tartsa őket.

### Egyéni G-kód beillesztése egy rétegbe

Az egyéni G-kód beillesztése hasznos lehet **haladó felhasználók** számára, amikor kalibrációs G-kódot hoznak létre **mint például egy hőmérséklet-torony**.

"A nagy hatalom nagy felelősséggel jár": ellenőrizze kétszer is, hogy a megfelelő G-kódokat illesztette-e be, és hogy érti-e, mit csinálnak. Egyes G-kódok esetében például véletlenül felülírhatja az EEPROM-ban lévő értékeket, vagy elmozdíthatja a fúvókát a nyomtatólemezen.

1. Egyéni G-kódot lehet beilleszteni [**a szeletelés előnézet**](../felhasznaloi-feluelet/user_interface.md#szeleteles-elonezet)
2. * Húzza a **réteg csúszkát** jobbra a célréteg kiválasztásához.
   * Kattintson a jobb gombbal\*\* a kék plusz ikonra
   * Válassza a **Egyéni G-kód hozzáadása** lehetőséget.
     1. Az egyéni G-kód **a kiválasztott réteg nyomtatása előtt** kerül beillesztésre.
   * Szúrja be az egyéni G-kódot az újonnan megnyitott ablakba.
   * Erősítse meg a **OK** megnyomásával.

![Egy&#xE9;ni G-k&#xF3;d beilleszt&#xE9;se egy r&#xE9;tegbe](../.gitbook/assets/advanced_functionality_017.jpg)

Az egyéni G-kódot **törölheti**, ha a kurzort a célréteg fölé mozgatja, és a bal gombbal a _**szürke kereszt ikonra**_ kattint.

Az egyéni G-kódot a _**kék kereszt ikonra**_ jobb gombbal kattintva **szerkesztheti**.

![Egy&#xE9;ni G-k&#xF3;d szerkeszt&#xE9;se/t&#xF6;rl&#xE9;se](../.gitbook/assets/advanced_functionality_018.jpg)

## Szerszámpályák exportálása OBJ formátumban

A kivágott modell OBJ-ként történő exportálása hasznos lehet, ha ismeri a 3D modellező és renderelő programokat. Amikor kivág egy modellt, válassza a **Fájl - Exportálás - Útvonalak exportálása OBJ-ként** lehetőséget. Ezt a fájlt aztán importálhatja egy tetszőleges 3D programba, például a Blenderbe, és fotórealisztikus előnézetet vagy akár animációt is készíthet a nyomatról.

Az exportálás tartalmazza mindazt, amit jelenleg az előnézetben lát. Ez azt jelenti, hogy ha a réteg csúszkával a modell egy keresztmetszetének előnézetét használja, az exportált fájl csak az előnézetben látható rétegeket fogja tartalmazni.

Ha csak a vágott modell külső részét kívánja renderelni, javasoljuk, hogy kapcsolja ki teljesen a kitöltést, a rétegmagasságot tartsa 0,15 mm felett, és a poligonok számának csökkentése érdekében csökkentse a kerületek számát 2-re. Azonban modellenként több millió poligonnal számolhat.

![A Blender 2.8-ban k&#xE9;sz&#xED;tett export&#xE1;lt szersz&#xE1;mp&#xE1;lya renderel&#xE9;se](../.gitbook/assets/advanced_functionality_019.jpeg)

