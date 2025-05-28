# Tesztautomatizálási kérdések

## Tesztelési alapok (ISTQB-hez kapcsolódó)
<img src="https://www.mindsmapped.com/wp-content/uploads/2016/06/ISTQB.jpg" alt="image" width="300" height="220">

#### ✅ Mi a tesztelés célja? Mi nem az?
- A munkatermékek, mint például a követelmények, felhasználói történetek, műszaki tervek és kód hibamegelőzés céljából történő kiértékelése

- Annak igazolása, hogy az összes meghatározott követelmény teljesült-e

- Annak ellenőrzése, hogy a teszt tárgya teljes mértékben implementálásra került, továbbá annak, validálása, hogy a felhasználók, illetve más érintett felek elvárásainak megfelelően működik.

- A teszt tárgyának minőségébe vetett bizalom kiépítése

- A meghibásodások és hibák megtalálása és ezáltal a nem megfelelő szoftverminőség kockázati szintjének csökkentése

- Megfelelő információ biztosítása az érintett feleknek, hogy ezáltal megalapozott döntést hozhassanak különösen a teszt tárgyának minőségi szintjére vonatkozóan

- A szerződésben foglalt, jogi vagy szabályozott követelményeknek, szabványoknak való megfelelés biztosítása, és/vagy igazolni a teszt tárgyának ezen követelményeknek, szabványoknak való megfelelőségét

#### ✅ Mik a tesztelési alapelvek?

1. A tesztelés a hibák jelenlétét mutatja, nem a hiányukat

    _A tesztelés kimutathatja a hibák jelenlétét, de azt nem képes igazolni, hogy nincsenek hibák. A teszteléssel csökken annak az esélye, hogy a szoftverben felfedezetlen hibák maradnak, de ha nem találnak hibát, az nem bizonyítja, hogy a rendszer helyes._

2. Nem lehetséges kimerítő teszt

    _Kimerítő teszt, azaz a mindenre (a bemenetek és előfeltételek minden kombinációjára) kiterjedő tesztelés a triviális eseteket leszámítva nem lehetséges. Ahelyett, hogy megkísérelnénk a kimerítő tesztelést, kockázatelemzés, tesztelési technikák használata és priorizálása szükséges a tesztelési erőforrások összpontosításához._

3. A korai tesztelés időt és pénzt spórol

    _A hibák korai megtalálásának érdekében a szoftverfejlesztési életciklus során mind a statikus, mind a dinamikus teszttevékenységeket a lehető legkorábban el kell kezdeni. A korai tesztelésre az angol szakirodalomban néha shift left-ként utalnak. A szoftverfejlesztési életciklus alatti korai tesztelés segít a költséges változtatások csökkentésében vagy eliminálásában (lásd: 3.1-es fejezet)._ 

4. Hibafürtök megjelenése

    _A kiadást megelőző tesztelés során megtalált hibák többsége rendszerint néhány modulban van, vagy ezen modulok felelősek a működési meghibásodások többségéért. A megjósolt hibafürtök és a tesztelés vagy működés során ténylegesen megfigyelt hibafürtök fontos bemenetként szolgálnak a tesztelési erőforrások összpontosítása érdekében alkalmazott kockázatelemzés számára (ahogy a 2. elvben említettük)_ 

5. Kísérd figyelemmel a féregirtó paradoxont 

    _Ha ugyanazokat a teszteket hajtjuk végre újra és újra, akkor ezen tesztek egy idő után nem fognak új hibákat találni. Ahhoz, hogy új hibákat találjunk, a létező teszteket és tesztadatokat módosítani kell, illetve új teszteket kell írni. (A tesztek egy idő után már nem hatékonyak a hibák megtalálásában csakúgy, ahogyan egy idő után a féregirtók sem hatékonyak a rovarok elpusztításában.) Néhány esetben például az automatikus regressziós tesztelés esetében a féregirtó paradoxonnak egy előnyös kimenete is van, ami a regressziós hibák viszonylag alacsony száma._  

6. A tesztelés függ a körülményektől

    _A tesztelést különböző körülmények esetén különbözőképpen hajtják végre. Például egy biztonságkritikus ipari irányító szoftvert másképp tesztelnek, mint egy e-kereskedelmi mobilalkalmazást. Egy másik példában, a tesztelés egy Agilis projektben különbözik egy szekvenciális szoftverfejlesztési életciklust alkalmazó projekt tesztelésétől (lásd: 2.1-es fejezet)._

7. A hibamentesség egy téveszme

    _Néhány szervezet azt várja el, hogy a tesztelők minden lehetséges tesztet le tudjanak futtatni és minden lehetséges hibát megtaláljanak, de az 1. és a 2. alapelv kimondja, hogy ez lehetetlen. Továbbá téveszme (téves meggyőződés) azt várni, hogy csupán azzal, hogy sok hibát találnak meg és javítanak ki, biztosítják a rendszer sikerességét. Például a meghatározott követelmények teljeskörű tesztelése és az összes talált hiba kijavítása még mindig eredményezhet egy nehezen használható rendszert, ami nem elégíti ki a felhasználók összes igényét és elvárását, vagy más hasonló rendszerekhez képest silányabb minőségű._


#### ✅ Mi az egységtesztelés (unit testing)? Ki felelős az egységtesztek írásáért?

Íme a válaszod Markdown formátumban:

---

## 🧪 Mi az egységtesztelés (unit testing)?

Az **egységtesztelés** a szoftvertesztelés egyik alapvető formája, amely során a program **legkisebb, önállóan tesztelhető egységeit** — például függvényeket vagy metódusokat — külön vizsgáljuk, hogy megbizonyosodjunk helyes működésükről.

### 🎯 Fő jellemzői:

* **Izoláltan** teszteli a kód egységeit, függetlenül más komponensektől.
* Automatizált tesztekkel gyors visszajelzést ad a fejlesztőknek.
* Segít a hibák **korai felismerésében** és a regressziók elkerülésében.
* Javítja a kód **minőségét**, **érthetőségét** és **karbantarthatóságát**.

### 🔧 Egyszerű példa (Python):

```python
def osszead(a, b):
    return a + b

def test_osszead():
    assert osszead(2, 3) == 5
    assert osszead(-1, 1) == 0
```

---

## 👨‍💻 Ki felelős az egységtesztek írásáért?

Az egységtesztek írásáért **elsősorban a fejlesztők** a felelősek.

### Miért?

* Ők ismerik legjobban az általuk írt kódot.
* Az egységtesztelés gyakran a fejlesztési folyamat szerves része.
* Gyakori módszer a **tesztvezérelt fejlesztés (TDD)**, ahol először a tesztet írják meg, majd a kódot.

---

## ✅ Összefoglalás

| Szempont      | Részletek                                                      |
| ------------- | -------------------------------------------------------------- |
| **Cél**       | A kód kis egységeinek tesztelése izoláltan                     |
| **Írja**      | Fejlesztők                                                     |
| **Haszon**    | Gyors hibafelismerés, jobb kódminőség, egyszerűbb karbantartás |
| **Gyakorlat** | Automatizált tesztfuttatás fejlesztés vagy build során         |

---


#### ✅ Mik a tesztszintek, és mi a különbség köztük?

- komponenstesztelés
- integrációs tesztelés
- rendszertesztelés
- elfogadási tesztelés

#### ✅ Mi a különbség a verifikáció és a validáció között?


A **verifikáció** és **validáció** két alapvető, de különböző fogalom a szoftverfejlesztés és tesztelés világában. Mindkettő a szoftverminőség biztosítását szolgálja, de más célra és időpontban használjuk őket.

---

### 🔍 **Verifikáció** (Verification)

> „A szoftver **helyesen lett-e megvalósítva**?”

* **Célja:** Annak ellenőrzése, hogy a szoftver megfelel-e a **tervezett specifikációnak vagy követelményeknek**.
* **Mikor történik:** A fejlesztés közben, vagy közvetlenül utána (pl. kódellenőrzés, egységtesztek során).
* **Fókusz:** A **belső működés**, a "hogyan".
* **Kérdés, amit felteszünk:**
  – *A szoftver úgy működik, ahogyan megterveztük?*
* **Módszerei:**

  * Egységtesztelés
  * Kódfelülvizsgálat (code review)
  * Statikus analízis
  * Modul- és integrációs tesztek

---

### ✅ **Validáció** (Validation)

> „A szoftver **megfelel-e a felhasználói igényeknek**?”

* **Célja:** Annak biztosítása, hogy a kész rendszer **valóban azt csinálja**, amit a **felhasználó elvár**.
* **Mikor történik:** A fejlesztési ciklus **végén** (pl. rendszer- vagy felhasználói tesztelés során).
* **Fókusz:** A **külső megfelelés**, az "elérendő cél".
* **Kérdés, amit felteszünk:**
  – *A szoftver megfelel az elvárt céloknak és üzleti igényeknek?*
* **Módszerei:**

  * Funkcionális tesztek
  * Rendszertesztek
  * Felhasználói elfogadási teszt (UAT)
  * Beta tesztelés

---

### 🧩 Összehasonlító táblázat

| Szempont     | Verifikáció                      | Validáció                                |
| ------------ | -------------------------------- | ---------------------------------------- |
| **Kérdés**   | „Jól építettük meg a rendszert?” | „A megfelelő rendszert építettük meg?”   |
| **Fókusz**   | Specifikáció követése            | Felhasználói elvárások teljesítése       |
| **Időzítés** | Fejlesztés közben                | Fejlesztés után, átadás előtt            |
| **Eszközök** | Egységteszt, kódelemzés          | UAT, rendszerteszt, felhasználói tesztek |

---

### 🧠 Rövid emlékezetes mondat:

> **Verifikáció:** *„Build the system right.”*
> **Validáció:** *„Build the right system.”*

---


#### ✅ Mik a tesztelési típusok, és mi a különbség köztük?

- A funkcionális minőségi jellemzők kiértékelése, mint például a teljesség, a helyesség és a megfelelőség
- A nemfunkcionális minőségi jellemzők értékelése, mint például a megbízhatóság, a teljesítmény hatékonyság, a biztonság, a kompatibilitás és a használhatóság
- Annak értékelése, hogy a komponens vagy a rendszer struktúrája, illetve architektúrája helyes, teljes és a specifikációnak megfelel
- A változások hatásainak értékelése, például annak megerősítése, hogy a hibákat javították (ellenőrző tesztelés), illetve a szoftver vagy a környezet változásaiból eredő nem kívánt hatások keresése (regressziós tesztelés)


#### ✅ Mi a különbség a fehér doboz, szürke doboz és fekete doboz tesztelés között?

Íme a **fehér doboz**, **szürke doboz** és **fekete doboz** tesztelési módszerek közötti különbség áttekinthető formában:

---

## 🎭 Doboz alapú tesztelési típusok összehasonlítása

| Jellemző                              | **Fehér doboz tesztelés**             | **Szürke doboz tesztelés**                          | **Fekete doboz tesztelés**                           |
| ------------------------------------- | ------------------------------------- | --------------------------------------------------- | ---------------------------------------------------- |
| **Tesztelő ismeri a belső működést?** | ✅ Igen                                | ⚠️ Részben (korlátozott rálátással)                 | ❌ Nem                                                |
| **Fókusz**                            | Belső logika, kódszerkezet            | Külső viselkedés + bizonyos belső ismeret           | Funkcionalitás, felhasználói elvárások               |
| **Kinek a feladata?**                 | Fejlesztő                             | Tesztmérnök vagy technikai tesztelő                 | Tesztelő, QA vagy felhasználó                        |
| **Mikor használják?**                 | Egység- és integrációs teszteknél     | Rendszer- és integrációs teszteknél                 | Funkcionális, elfogadási teszteknél                  |
| **Példák**                            | Kódfedettség, elágazási tesztek       | API tesztek, biztonsági tesztek                     | Gombok, űrlapok, hibakezelés tesztelése              |
| **Előny**                             | Alapos, hibátlan logika ellenőrizhető | Hatékony a technikai és üzleti logika ellenőrzésére | Felhasználó-központú, specifikációra fókuszál        |
| **Hátrány**                           | Drága, időigényes                     | Nehéz kiegyensúlyozni a két szemléletet             | Nem fed le belső hibákat vagy optimalizációs hibákat |

---

## 🔍 Rövid definíciók

### 🧱 Fehér doboz tesztelés (White-box testing)

* A tesztelő **látja és ismeri a kódot**.
* Ellenőrzi az algoritmusok logikai működését, például ciklusokat, elágazásokat, függvényhívásokat.
* Tipikus teszttípusok: **egységteszt, kódfedettség teszt**.

### ⚪ Szürke doboz tesztelés (Gray-box testing)

* A tesztelő **részleges ismeretekkel rendelkezik a rendszer belső működéséről**.
* Használja ezeket az ismereteket a **hatékonyabb tesztesetek** kialakításához.
* Tipikus példa: API tesztelés, ahol ismert az adatstruktúra, de nem a teljes implementáció.

### 📦 Fekete doboz tesztelés (Black-box testing)

* A tesztelő **nem látja a kódot**, csak a bemenettel és kimenettel dolgozik.
* A cél: **meggyőződni arról, hogy a rendszer a specifikációnak megfelelően működik**.
* Tipikus példa: felhasználói felület, űrlapok, gombok, funkcionális tesztek.

---

## 🧠 Összegzés

> * **Fehér doboz**: *"Teszteld, hogy hogyan működik."*
> * **Fekete doboz**: *"Teszteld, hogy mit csinál."*
> * **Szürke doboz**: *"Teszteld, mit csinál, de használd ki, amit tudsz róla."*

---


#### ✅ Mi a különbség a felhasználói elfogadási teszt (UAT) és a rendszerteszt között?

Íme a **felhasználói elfogadási teszt (UAT)** és a **rendszerteszt** közötti különbség részletesen és áttekinthető formában:

---

## 🧪 UAT vs. Rendszerteszt – Mi a különbség?

| Jellemző                 | **Rendszerteszt (System Testing)**                                | **Felhasználói elfogadási teszt (UAT)**                                |
| ------------------------ | ----------------------------------------------------------------- | ---------------------------------------------------------------------- |
| **Cél**                  | Az egész rendszer működésének ellenőrzése a specifikációk alapján | Annak ellenőrzése, hogy a rendszer megfelel-e az **üzleti igényeknek** |
| **Kinek a feladata?**    | Tesztelők, QA szakemberek                                         | Végfelhasználók, megrendelők, üzleti képviselők                        |
| **Fókusz**               | Teljes rendszer technikai és funkcionális ellenőrzése             | Felhasználói elvárások, üzleti folyamatok működése                     |
| **Tesztelés típusa**     | Funkcionális és nem-funkcionális is lehet                         | Funkcionális, üzleti szempontú                                         |
| **Tesztelési környezet** | Tesztkörnyezet (QA, staging)                                      | Éleshez közeli környezet, UAT környezet                                |
| **Dokumentum alapja**    | Rendszerterv, specifikációk                                       | Üzleti követelmények, elfogadási kritériumok                           |
| **Tesztelés eredménye**  | Hibák, hiányosságok feltárása                                     | Döntés a rendszer **elfogadásáról vagy elutasításáról**                |

---

## 🧩 Rövid magyarázatok

### 🧰 **Rendszerteszt (System Testing)**

* Teljes rendszer viselkedését ellenőrzi különféle szempontok alapján.
* Célja, hogy megtalálja a hibákat még **azelőtt**, hogy a felhasználók tesztelnék.
* Tipikus ellenőrzések:

  * Funkcionális működés
  * Teljesítmény
  * Biztonság
  * Kompatibilitás

### 👥 **Felhasználói elfogadási teszt (UAT – User Acceptance Testing)**

* A **végső tesztelési fázis**, közvetlenül az élesítés előtt.
* A felhasználók ellenőrzik, hogy a rendszer **az ő valós igényeiket kielégíti-e**.
* Ha a teszt sikeres → a rendszer **elfogadható és bevezethető**.

---

## ✅ Összefoglalás

> * **Rendszerteszt**: „Minden funkció technikailag jól működik?”
> * **UAT**: „Ez a rendszer tényleg azt tudja, amire nekem szükségem van?”

Mindkettő kulcsfontosságú, de más célt szolgál:
🔧 A **rendszerteszt** a szoftver **minőségét** biztosítja,
👤 az **UAT** pedig a **használhatóságát és üzleti alkalmasságát**.

#### ✅ Sorolj fel különbségeket a regressziós tesztelés, a füsttesztelés és az újratesztelés között!

Íme a **regressziós tesztelés**, a **füsttesztelés** és az **újratesztelés** közötti főbb különbségek jól strukturált, áttekinthető formában:

---

## 🧪 Tesztelési típusok összehasonlítása

| Jellemző             | **Füsttesztelés** (Smoke Testing)                    | **Újratesztelés** (Re-testing)                            | **Regressziós tesztelés** (Regression Testing)                       |
| -------------------- | ---------------------------------------------------- | --------------------------------------------------------- | -------------------------------------------------------------------- |
| **Cél**              | Ellenőrizni, hogy a rendszer alapfunkciói működnek-e | Ellenőrizni, hogy a korábban talált hibát kijavították-e  | Ellenőrizni, hogy a módosítások nem okoztak új hibákat más részeken  |
| **Mikor történik?**  | Fejlesztés után, még a részletes tesztelés előtt     | Hiba javítása után                                        | Kódmódosítás, hibajavítás vagy új funkció hozzáadása után            |
| **Fókusz**           | Alapvető, kritikus funkciók                          | Egy adott hiba                                            | Teljes rendszer, vagy érintett funkciók                              |
| **Automatizálható?** | Igen (általában automatizált tesztcsomag)            | Nem mindig, inkább manuális                               | Igen, gyakran automatizálják                                         |
| **Tesztelők által?** | QA vagy automatizált pipeline                        | QA (hibajegyek alapján)                                   | QA (szélesebb tesztcsomag futtatás)                                  |
| **Példa**            | Be tudok-e jelentkezni? Elindul-e a főoldal?         | A „Számítás hiba” javítása után újra lefuttatom a tesztet | A bejelentkezés módosítása nem rontotta-e el a jelszó-visszaállítást |

---

## 🔍 Rövid definíciók

### 🔥 **Füsttesztelés** (*Smoke Testing*)

* „Működik egyáltalán az alkalmazás?”
* Alapvető funkciók gyors ellenőrzése, **mielőtt** részletes tesztelésbe kezdünk.

### ♻️ **Újratesztelés** (*Re-testing*)

* Az **egyedi hibák újrapróbálása**, miután azokat a fejlesztők kijavították.
* Arra fókuszál, hogy **az adott hiba** ténylegesen megszűnt-e.

### 🔁 **Regressziós tesztelés** (*Regression Testing*)

* Biztosítja, hogy a rendszer **korábban jól működő részei továbbra is jól működnek**, annak ellenére, hogy valamit módosítottunk.

---

## ✅ Emlékezetes példamondat:

> * **Füstteszt:** „Elindul az autó?”
> * **Újratesztelés:** „Megjavították a féket, most már működik?”
> * **Regresszió:** „A fékjavítás után még mindig működik a lámpa is?”

---

#### ✅ Mi a különbség a statikus és dinamikus tesztelés között?

Íme a **statikus** és **dinamikus tesztelés** közötti legfontosabb különbségek áttekinthető formában:

---

## 🧪 Statikus vs. Dinamikus tesztelés

| Jellemző                | **Statikus tesztelés**                                | **Dinamikus tesztelés**                               |
| ----------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| **Mit jelent?**         | A kód vagy dokumentum **elemzése futtatás nélkül**    | A program **futtatása közbeni viselkedés vizsgálata** |
| **Futtatás szükséges?** | ❌ Nem                                                 | ✅ Igen                                                |
| **Cél**                 | Hibák, hiányosságok azonosítása a kódban vagy tervben | A rendszer viselkedésének ellenőrzése működés közben  |
| **Mikor történik?**     | Fejlesztés korai szakaszában                          | Fejlesztés után, tesztelési fázisban                  |
| **Kinek a feladata?**   | Fejlesztők, tervezők, QA szakemberek                  | Tesztelők, QA szakemberek                             |
| **Példák**              | Kódfelülvizsgálat, statikus kódelemzés, lintelés      | Egységteszt, funkcionális teszt, felhasználói tesztek |
| **Automatizálható?**    | Igen                                                  | Igen (pl. automata tesztek, CI/CD)                    |
| **Fókusz**              | Hibák megelőzése a forrásban, dokumentációban         | Hibák felderítése a **futó rendszerben**              |

---

## 🔍 Rövid magyarázatok

### 🧱 **Statikus tesztelés**

* A kód vagy terv **áttekintése, elemzése** anélkül, hogy az lefutna.
* Segít **korán felfedezni** hibákat, például:

  * Szintaktikai hibák
  * Nem használt változók
  * Dokumentációs hiányosságok

**Példa:**

* Kódfelülvizsgálat (Code Review)
* `flake8`, `eslint`, `SonarQube` jellegű eszközök

---

### 🚀 **Dinamikus tesztelés**

* A szoftver **futása közben történik**.
* Célja, hogy megvizsgálja, valóban azt csinálja-e, amit kell.

**Példa:**

* Egységtesztek
* UI tesztek
* Használati esetek (use case) tesztelése

---

## ✅ Összefoglalás

> * **Statikus tesztelés**: *„Hibát keresek a kódban, mielőtt elindítom.”*
> * **Dinamikus tesztelés**: *„Megnézem, mit csinál a program, miközben fut.”*

Mindkét módszer fontos a **teljes körű szoftverminőség biztosításához**.

### ✅ Hasonlítsd össze a V-modellt, a vízesés modellt és az Agile megközelítést a tesztelés szempontjából!

Íme a **V-modell**, a **vízesés modell** és az **Agile megközelítés** összehasonlítása **tesztelési szempontból**:

---

## 📊 Összehasonlító táblázat

| Jellemző                           | **Vízesés modell**                                  | **V-modell**                                        | **Agile megközelítés**                                 |
| ---------------------------------- | --------------------------------------------------- | --------------------------------------------------- | ------------------------------------------------------ |
| **Tesztelés időzítése**            | Tesztelés a fejlesztés után, szinte **külön fázis** | Tesztelés **párhuzamosan** tervezve a fejlesztéssel | Tesztelés **folyamatosan** minden iterációban          |
| **Tesztelés típusa**               | Főleg **rendszer- és elfogadási tesztelés**         | **Minden szinten van teszt** (unit → UAT)           | **Automatizált és manuális tesztek** iterációkban      |
| **Rugalmasság a változásokra**     | ❌ Nagyon alacsony                                   | ⚠️ Alacsony, de jobb tervezett visszacsatolás       | ✅ Nagyon magas – változások gyorsan kezelhetők         |
| **Tesztelés szerepe**              | Tesztelők főként a végén kapcsolódnak be            | Tesztelés már a specifikációk tervezésénél is jelen | Tesztelők a **csapat szerves részei**, már az elejétől |
| **Dokumentáció igénye**            | 📄 Nagyon magas                                     | 📄 Nagyon magas                                     | 📝 Könnyebb, „just enough” dokumentáció                |
| **Hibajavítás költsége**           | 💸 Magas (későn derülnek ki a hibák)                | 💸 Magas, de a korai tesztelés csökkenti            | 💰 Alacsonyabb – a hibák gyorsan észlelhetők           |
| **Tesztelési megközelítés**        | **Szekvenciális**, utólagos                         | **Párhuzamos** fejlesztés-tesztelés struktúrában    | **Iteratív és folyamatos**                             |
| **Példa a tesztelési módszerekre** | Rendszerteszt, UAT                                  | Unit teszt → integrációs → rendszerteszt → UAT      | TDD, BDD, automatizált regressziós tesztek             |

---

## 🔍 Rövid összefoglalások

### 💧 **Vízesés modell**

* Szekvenciális fejlesztési modell.
* A tesztelés **a fejlesztés végén kezdődik**, ami növeli a hibák javításának költségét.
* **Tesztelés = külön fázis.**

### ✅ **V-modell (Validation & Verification)**

* A vízesés modell továbbfejlesztett változata.
* A fejlesztési és tesztelési lépések **párhuzamosan tervezettek**.
* Minden fejlesztési szinthez tartozik egy **megfelelő tesztszint**.

### ⚡ **Agile**

* Iteratív és inkrementális fejlesztés.
* A tesztelés **folyamatos**, része a sprintnek.
* **Tesztelők aktívan együtt dolgoznak a fejlesztőkkel** – pl. TDD (Test-Driven Development), CI/CD tesztek, automatizált tesztelés.

---

## ✅ Összegzés

| Modell   | Tesztelés időzítése | Rugalmasság | Hibafelismerés ideje | Fejlesztés-tesztelés kapcsolata |
| -------- | ------------------- | ----------- | -------------------- | ------------------------------- |
| Vízesés  | Későn               | Alacsony    | Késői                | Szekvenciális                   |
| V-modell | Párhuzamosan        | Közepes     | Korai (de merev)     | Párhuzamos                      |
| Agile    | Folyamatosan        | Magas       | Korai és folyamatos  | Szoros együttműködés            |

---

🔔 **Kulcsmondat**:

> * **Vízesés**: „Teszteljük a végén.”
> * **V-modell**: „Tervezd meg a tesztet is, már a kezdetektől.”
> * **Agile**: „Tesztelés azonnal, folyamatosan, együtt a fejlesztéssel.”

<img src="https://t4.ftcdn.net/jpg/03/90/15/65/360_F_390156585_8w1lsOyICIAOvDCU8tExXW2QwLCOFwXD.jpg" alt="image" width="550" height="400">


<img src="https://i.imgur.com/S38EBJw.png" alt="image" width="550" height="400">   <img src="https://segedletek.level14.hu/assets/img/modszertan-vizeses.svg" alt="image" width="550" height="400">


<img src="https://promanconsulting.hu/wp-content/uploads/2022/03/agilis-modszertanok-optimized.jpg" width="550" height="400">





## Reporting, Bugs
<img src="https://moolya.com/blog/wp-content/uploads/2023/05/Bug-Report.png" alt="image" width="300" height="220">

#### ✅ Milyen lépéseket követnél egy hiba megtalálásakor?
Amikor egy hibát találsz egy szoftverben, fontos, hogy **strukturált módon** járj el. Az alábbi lépések segítenek a hiba **hatékony azonosításában, dokumentálásában és kezelésében**:

---

## 🪲 Hiba kezelési lépések

### 1. 🔍 **A hiba azonosítása**

* Figyeld meg a hibajelenséget.
* Ellenőrizd: valóban hiba, vagy helytelen használat, környezet, adat?
* Győződj meg róla, hogy a hiba **ismételhető**.

### 2. 📸 **Reprodukálás**

* Lépésről lépésre hajtsd végre azokat a műveleteket, amelyek a hibát előidézik.
* Jegyezd fel: bemenetek, környezet, előfeltételek.

### 3. 📄 **Dokumentálás**

* Rögzítsd a hibát egy hibajegyben (issue, bug ticket).
* Írd le pontosan:

  * Hiba leírása
  * Reprodukciós lépések
  * Várt eredmény vs. tényleges eredmény
  * Képernyőkép / hibaüzenet (ha van)
  * Környezet (pl. böngésző, verzió, adatbázis)

### 4. 🧪 **Súlyosság és prioritás meghatározása**

* Értékeld: mennyire kritikus a hiba?

  * Blokkoló / súlyos / közepes / kisebb
* Hatása az üzleti folyamatokra vagy felhasználókra?

### 5. 📬 **Kommunikáció**

* Jelentsd a hibát a megfelelő csapatnak (fejlesztők, QA, PO).
* Kövesd a csapat hibakezelési protokollját (pl. Jira, Azure DevOps, Trello).

### 6. 🔧 **Hibajavítás nyomon követése**

* Figyeld a státuszt: *Open → In Progress → Resolved*.
* Kommunikálj, ha új információ merül fel vagy a hiba súlyosbodik.

### 7. ✅ **Újratesztelés (Re-testing)**

* Amint a fejlesztő kijavítja a hibát, futtasd újra a tesztet.
* Győződj meg róla, hogy a hiba **valóban megszűnt**.

### 8. 🔁 **Regressziós tesztelés**

* Ellenőrizd, hogy a javítás **nem okozott új hibát** más részekben.

### 9. 📦 **Lezárás**

* Ha minden rendben működik, zárd le a hibajegyet.
* Jegyezd fel a tapasztalatokat, ha szükséges (pl. tanulságként).

---

## ✅ Példa röviden:

> 1. Találok egy hibát: nem működik a bejelentkezés.
> 2. Újra megpróbálom: minden alkalommal sikertelen.
> 3. Dokumentálom a hiba részleteit: képernyőkép, log, lépések.
> 4. Hibajegyet nyitok a fejlesztőknek.
> 5. Visszajelzést várok, majd újratesztelek.
> 6. Ha jó, regressziós teszttel ellenőrzöm a kapcsolódó funkciókat is.

---

Ez a folyamat biztosítja, hogy a hibák **gyorsan, hatékonyan és átláthatóan** legyenek kezelve.


#### ✅ Beszélj a gyakori tesztjelentésekről és részleteikről!

Természetesen! Íme egy összefoglaló a **gyakori tesztjelentésekről** és azok főbb részeiről:

---

## 📝 Gyakori tesztjelentések és főbb részeik

### 1. **Tesztelési előrehaladási jelentés (Test Progress Report)**

* **Cél:** Nyomon követni a tesztelés aktuális állapotát.
* **Tartalom:**

  * Összes tervezett teszt esetszám
  * Elvégzett tesztek száma
  * Sikertelen, sikeres és függőben lévő tesztek
  * Kiemelt hibák száma és státusza
  * Kockázatok, problémák, akadályok
  * Következő lépések

---

### 2. **Hibajelentés (Bug Report / Defect Report)**

* **Cél:** Egy-egy konkrét hiba részletes dokumentálása.
* **Tartalom:**

  * Hibaazonosító (ID)
  * Hiba leírása
  * Lépések a hiba reprodukálásához
  * Várt és tényleges eredmény
  * Prioritás és súlyosság
  * Környezet, verziószám
  * Hiba státusza (open, in progress, resolved, closed)
  * Megjegyzések, képernyőképek, logok

---

### 3. **Tesztzáró jelentés (Test Summary Report)**

* **Cél:** A tesztelési ciklus végén összefoglalni a teljes tesztelés eredményeit.
* **Tartalom:**

  * Tesztelési célok és lefedettség
  * Elvégzett tesztek statisztikái (sikeres, sikertelen)
  * Talált hibák összesítése és állapotuk
  * Minőségi értékelés (pl. a rendszer megfelel-e az elvárásoknak)
  * Kockázatok és nyitott problémák
  * Ajánlások az élesítéshez vagy további fejlesztésekhez

---

### 4. **Teszt eszköz riportok**

* **Cél:** Automatizált tesztelési eszközök által generált jelentések.
* **Tartalom:**

  * Tesztek futási eredményei (pass/fail)
  * Futási idő, lefedettség
  * Hibák és logok automatikusan összegyűjtve

---

## 🔑 Fontos szempontok a tesztjelentésekhez

* **Átláthatóság:** Világos, könnyen érthető legyen minden érintett számára.
* **Pontosság:** Legyen részletes és megbízható.
* **Időzítés:** Jelentések rendszeresek legyenek, az aktuális állapotot tükrözzék.
* **Cselekvésre ösztönzés:** Tartalmazzanak javaslatokat, következő lépéseket.

---


#### ✅ Mit tartalmaz egy hibajelentés?
Egy **hibajelentés** (bug report) részletesen dokumentálja a talált hibát, hogy a fejlesztők pontosan megértsék, reprodukálják és kijavíthassák azt.

---

## 🐞 Hibajelentés tartalma

| Elem                            | Leírás                                                                                  |
| ------------------------------- | --------------------------------------------------------------------------------------- |
| **Hibaazonosító (ID)**          | Egyedi azonosító a hibajegyhez (pl. BUG-1234)                                           |
| **Cím / Rövid leírás**          | Több szavas, tömör összefoglaló, pl. „Bejelentkezés sikertelen érvényes adatokkal”      |
| **Részletes leírás**            | A hiba pontos leírása, mi a probléma, milyen viselkedést tapasztalunk                   |
| **Lépések a reprodukáláshoz**   | Pontos, lépésről-lépésre leírás, hogyan idézhető elő a hiba                             |
| **Várt eredmény**               | Mi történt volna, ha a rendszer jól működne                                             |
| **Tényleges eredmény**          | Mi történt valójában, a hiba megnyilvánulása                                            |
| **Súlyosság (Severity)**        | Mennyire kritikus a hiba (pl. kritikus, magas, közepes, alacsony)                       |
| **Prioritás (Priority)**        | Milyen gyorsan kell kijavítani (pl. magas, normál, alacsony)                            |
| **Környezet**                   | Rendszer, verzió, operációs rendszer, böngésző, adatbázis stb., ahol a hiba jelentkezik |
| **Képernyőkép / logok**         | Hiba illusztrációja képpel, hibaüzenetettel, naplófájlokkal                             |
| **Hiba státusza**               | Jelenlegi állapot (pl. új, megnyitott, folyamatban, javított, lezárt)                   |
| **Hibát találó személy**        | Ki jelentette a hibát                                                                   |
| **Dátum**                       | Mikor lett a hiba jelentve                                                              |
| **Megjegyzések / Kommunikáció** | További információk, fejlesztői vagy tesztelői megjegyzések                             |

---

#### ✅ Hogyan rangsorolnál egy hibát?
A hiba rangsorolása a **súlyosság (severity)** és a **prioritás (priority)** alapján történik. Ezek segítenek eldönteni, hogy **milyen gyorsan és milyen módon kell a hibát kezelni**.

---

## 🔥 Hogyan rangsorolnál egy hibát?

### 1. **Súlyosság (Severity)**

* Milyen **hatással van a hiba a rendszer működésére**?
* A hibák típusai és súlyosságuk például:

| Súlyosság               | Leírás                                                   | Példa                        |
| ----------------------- | -------------------------------------------------------- | ---------------------------- |
| **Kritikus (Critical)** | A rendszer összeomlik, vagy alapvető funkció nem működik | Rendszerleállás, adatvesztés |
| **Magas (Major)**       | Fontos funkció nem működik, de a rendszer fut            | Bejelentkezési hiba          |
| **Közepes (Moderate)**  | Hibás működés, de van megkerülő megoldás                 | Hibás adatmegjelenítés       |
| **Alacsony (Minor)**    | Kisebb problémák, esztétikai hibák                       | Elírás, UI igazítások        |
| **Triviális (Trivial)** | Apróbb hibák, nem befolyásolja a működést                | Szöveghiba, formázási gond   |

---

### 2. **Prioritás (Priority)**

* Milyen **gyorsan kell javítani** a hibát a fejlesztési vagy üzleti célok miatt?
* Példák:

| Prioritás           | Leírás                                                              |
| ------------------- | ------------------------------------------------------------------- |
| **Magas (High)**    | Azonnali javítás szükséges, blokkolhatja a kiadást vagy használatot |
| **Normál (Medium)** | Fontos, de nem kritikus, a következő iterációban javítandó          |
| **Alacsony (Low)**  | Nem sürgős, későbbi fejlesztési ciklusban javítható                 |

---

### 3. **Rangsorolás döntése**

* **Kritikus + magas prioritás** → azonnali javítás
* **Közepes súlyosság + normál prioritás** → következő sprintben/javítási ciklusban
* **Alacsony súlyosság + alacsony prioritás** → későbbi időpontban

---

### 4. **További tényezők, amiket figyelembe veszek:**

* Üzleti hatás (pl. ügyfél elégedettség)
* Előfordulás gyakorisága
* Környezeti tényezők (pl. csak bizonyos verziókban van)
* Egyéb kapcsolódó hibák, kockázatok

---

## Test Automation, Selenium
<img src="https://media.licdn.com/dms/image/C4D12AQE3GOyVsZazOw/article-cover_image-shrink_600_2000/0/1583830696602?e=2147483647&v=beta&t=bYHbKyhMoWsMgtEug6eSf3m0db5ZtGEl437TeS1qkfI" alt="image" width="320" height="220">

#### ✅ Melyik teszteseteket érdemes automatizálni és melyiket nem?
Nagyon jó kérdés! Az automatizált tesztelés hatékonyabbá teheti a tesztfolyamatot, de nem minden teszteset alkalmas automatizálásra. Íme egy összefoglaló arról, **milyen teszteseteket érdemes automatizálni, és melyeket nem**:

---

## ✅ Tesztesetek, amiket érdemes automatizálni

| Jellemzők                                               | Példa                                         |
| ------------------------------------------------------- | --------------------------------------------- |
| **Ismétlődő, gyakran futtatott tesztek**                | Regressziós tesztek, füsttesztek              |
| **Nagy mennyiségű adat vagy kombináció**                | Tömeges adatbevitel, több platform tesztelése |
| **Stabil és ritkán változó funkciók**                   | Alapvető üzleti folyamatok, login funkció     |
| **Egységtesztek, ahol könnyű mockolni a függőségeket**  | Kódrészletek, függvények, metódusok           |
| **Automatizálható, egyértelműen ellenőrizhető kimenet** | Kalkulációk, válaszok, UI elemek megléte      |
| **Időigényes manuális tesztek**                         | Komplett adatbázis feltöltés és ellenőrzés    |

---

## ❌ Tesztesetek, amiket nem érdemes automatizálni

| Jellemzők                                            | Példa                                             |
| ---------------------------------------------------- | ------------------------------------------------- |
| **Gyakran változó, fejlesztés alatt álló funkciók**  | Prototípusok, UI gyors iterációk                  |
| **Explorációs, felfedező tesztelés**                 | Kézi, intuíció alapú tesztelés                    |
| **Felhasználói élmény és használhatóság vizsgálata** | UX, UI design, vizuális elemek érzékelése         |
| **Nehéz vagy drága automatizálni**                   | Különleges hardver vagy integrációk               |
| **Nem determinisztikus tesztek**                     | Például időzítés, hálózati késleltetés tesztelése |
| **Ritkán használt funkciók**                         | Kevésbé fontos, alkalmi funkciók                  |

---

## 📝 Összefoglaló

* **Automatizáld:** Gyakran ismétlődő, jól definiált, stabil teszteseteket.
* **Ne automatizáld:** Olyan teszteket, ahol az emberi megítélés, kreativitás vagy gyakori változás miatt nem hatékony az automatizáció.

---


#### ✅ Írj le egy jó automatizált tesztet!
Persze! Íme egy példa egy jól megírt, egyszerű **automatizált tesztre** Pythonban, a **Selenium** könyvtár használatával, ami egy weboldal bejelentkezési funkcióját teszteli.

---

## Példa: Automatizált bejelentkezési teszt Selenium-mal (Python)

```python
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys
import unittest

class LoginTest(unittest.TestCase):

    def setUp(self):
        # Böngésző megnyitása
        self.driver = webdriver.Chrome()
        self.driver.get("https://example.com/login")

    def test_valid_login(self):
        driver = self.driver

        # Felhasználónév mező megtalálása és kitöltése
        username_input = driver.find_element(By.ID, "username")
        username_input.send_keys("valid_user")

        # Jelszó mező megtalálása és kitöltése
        password_input = driver.find_element(By.ID, "password")
        password_input.send_keys("valid_password")

        # Bejelentkezés gomb megnyomása
        login_button = driver.find_element(By.ID, "login-button")
        login_button.click()

        # Ellenőrzés: sikeres bejelentkezés után megjelenik a dashboard
        welcome_message = driver.find_element(By.ID, "welcome-message")
        self.assertIn("Welcome, valid_user", welcome_message.text)

    def tearDown(self):
        # Böngésző bezárása
        self.driver.quit()

if __name__ == "__main__":
    unittest.main()
```

---

## Miért jó ez a teszt?

* **Automatikusan futtatható**: Nem igényel manuális beavatkozást.
* **Ismételhető**: Bármikor lefuttatható ugyanazzal az eredménnyel.
* **Egyértelmű elvárás**: Ellenőrzi, hogy a bejelentkezés után a megfelelő üzenet megjelenik.
* **Karbantartható**: A teszt jól strukturált, `setUp` és `tearDown` metódusokkal.
* **Konkrét teszteset**: Csak egy konkrét, jól definiált funkciót tesztel.

---

#### ✅ Mi a Selenium, Selenium IDE és Selenium WebDriver?
Természetesen! Íme egy áttekintés a **Selenium**, **Selenium IDE** és **Selenium WebDriver** fogalmakról:

---

## Selenium

* Egy **nyílt forráskódú tesztelési eszközcsomag**, amely elsősorban webalkalmazások automatizált tesztelésére szolgál.
* Lehetővé teszi a böngészők vezérlését különböző programozási nyelveken (pl. Java, Python, C#, Ruby).
* Célja a webes alkalmazások funkcionális és regressziós tesztelése.

---

## Selenium IDE

* **Integrated Development Environment** — egy böngésző kiegészítő (plugin), ami elsősorban **record & playback** funkciót nyújt.
* Használata egyszerű: felveszi a felhasználó interakcióit a böngészőben, majd lejátszható tesztként menti el.
* Jó kezdőknek vagy gyors prototípusokhoz, de korlátozottabb a komplex tesztek és testreszabás terén.
* Csak a Firefoxban és Chrome-ban érhető el bővítményként.

---

## Selenium WebDriver

* Egy **programozási API**, amely lehetővé teszi, hogy a tesztelők kód alapján vezéreljék a böngészőt.
* Támogatja a legtöbb modern böngészőt (Chrome, Firefox, Edge, Safari).
* Sokkal **rugalmasabb és erősebb**, mint az IDE, alkalmas komplex, skálázható automatizált tesztek készítésére.
* Használható különböző programozási nyelvekkel (Java, Python, C#, JavaScript stb.).
* Közvetlenül kommunikál a böngészővel, nem igényel manuális rögzítést.

---

## Összefoglaló táblázat

| Eszköz                     | Leírás                                    | Előnyök                      | Hátrányok                     |
| -------------------------- | ----------------------------------------- | ---------------------------- | ----------------------------- |
| **Selenium IDE**           | Böngésző plugin, record & playback        | Gyors, egyszerű használat    | Kevésbé rugalmas, korlátozott |
| **Selenium WebDriver**     | Programozási API böngészővezérléshez      | Nagy rugalmasság, skálázható | Kódolást igényel              |
| **Selenium (általánosan)** | Teljes keretrendszer, mindkettő tartozéka | Széleskörű támogatás         | —                             |

---

#### ✅ Hogyan lehet azonosítani a webes elemeket?
Nagyon fontos kérdés a webes automatizált tesztelésnél! A **webes elemek azonosítása** az alapja annak, hogy a teszt automatikusan megtalálja és kezelje az oldal elemeit (pl. gombok, űrlapmezők, linkek).

---

## 🕵️‍♂️ Hogyan lehet azonosítani a webes elemeket?

### 1. **ID (azonosító)**

* Egyedi azonosító az oldalon.
* A legjobb választás, mert egyedi és gyors.

```html
<input id="username" type="text" />
```

```python
driver.find_element(By.ID, "username")
```

---

### 2. **Name (név)**

* Gyakran használatos, főleg űrlapmezőknél.
* Nem mindig egyedi, ezért körültekintően használjuk.

```html
<input name="email" type="text" />
```

```python
driver.find_element(By.NAME, "email")
```

---

### 3. **Class Name (osztálynév)**

* CSS osztály alapján azonosít.
* Több elem is lehet ugyanazzal az osztállyal, így listát ad vissza.

```html
<button class="btn-primary">Submit</button>
```

```python
driver.find_elements(By.CLASS_NAME, "btn-primary")
```

---

### 4. **Tag Name (címke neve)**

* HTML elem típusa, pl. `input`, `button`, `div`.
* Ritkán egyedi, inkább lista visszaadására jó.

```python
driver.find_elements(By.TAG_NAME, "input")
```

---

### 5. **Link Text / Partial Link Text (link szöveg)**

* A link teljes vagy részleges szövege alapján keres.

```html
<a href="/logout">Kijelentkezés</a>
```

```python
driver.find_element(By.LINK_TEXT, "Kijelentkezés")
```

---

### 6. **CSS Selector**

* Nagyon rugalmas, bármilyen CSS szabály használható.
* Gyors és hatékony, jól használható összetett elemekhez.

```html
<div class="menu"><a href="/profile">Profil</a></div>
```

```python
driver.find_element(By.CSS_SELECTOR, "div.menu > a")
```

---

### 7. **XPath**

* XML útvonal kifejezés, nagyon rugalmas és erőteljes.
* Lehetővé teszi az elemek pozíció, attribútumok és szülő-gyermek kapcsolatok alapján történő keresést.
* Kicsit lassabb és nehezebben olvasható, de komplex struktúráknál hasznos.

```html
<input type="text" id="email" />
```

```python
driver.find_element(By.XPATH, "//input[@id='email']")
```

---

## 📝 Tippek az elemazonosításhoz

* Mindig próbálj **egyedi és stabil azonosítót** használni (pl. ID, CSS Selector).
* Kerüld az olyan azonosítókat, amelyek gyakran változnak (dinamikus osztályok, indexek).
* Használj fejlesztői eszközöket (pl. Chrome DevTools), hogy megtaláld az elemeket és azonosítóikat.
* Teszteld az XPath vagy CSS szelektorokat konzolból, mielőtt kódba írod.

---

#### ✅ Hogyan lehet várni az elemekre, és mi lehet a probléma? Gyűjtsd össze a lehetséges hibákat és okokat!
Nagyon fontos téma az automatizált tesztelésnél! A **várakozás az elemekre** (waiting) nélkül a tesztek gyakran instabillá válnak, mert az elem még nem töltődött be, vagy nem interaktív, mikor a kód hozzáférne.

---

## 🕰️ Hogyan lehet várni az elemekre Selenium-ban?

### 1. **Implicit Wait (Implicit várakozás)**

* Beállít egy időt, ameddig a WebDriver folyamatosan próbálkozik megtalálni az elemet, mielőtt hibát dobna.
* Példa:

```python
driver.implicitly_wait(10)  # maximum 10 másodpercig vár
```

### 2. **Explicit Wait (Explicit várakozás)**

* Egy adott feltételre vár egy adott időtartamig.
* Pl. az elem megjelenésére, kattinthatóságára.

```python
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC

wait = WebDriverWait(driver, 10)
element = wait.until(EC.element_to_be_clickable((By.ID, "submit-button")))
```

### 3. **Fluent Wait (Rugalmas várakozás)**

* Explicit wait egy továbbfejlesztett változata, ami figyelembe veszi az ismétlődő próbálkozások és kivételek kezelését.

---

## ⚠️ Lehetséges problémák és okok várakozáskor

| Hiba / Probléma                      | Lehetséges okok                                                                                                        |
| ------------------------------------ | ---------------------------------------------------------------------------------------------------------------------- |
| **NoSuchElementException**           | - Elem nem létezik a DOM-ban (pl. helytelen locator) <br> - Elem később töltődik be, de nincs megfelelő várakozás      |
| **TimeoutException**                 | - Várakozás lejárt, de az elem nem jelent meg vagy nem vált kattinthatóvá <br> - Rossz feltétel vagy helytelen locator |
| **ElementNotInteractableException**  | - Az elem látható, de nem interaktív (pl. el van takarva) <br> - Az oldal még nem teljesen töltődött be                |
| **StaleElementReferenceException**   | - Az elem eltűnt vagy frissült a DOM-ban a keresés után <br> - Az oldal dinamikusan módosul (pl. AJAX)                 |
| **ElementClickInterceptedException** | - Egy másik elem (pl. modal vagy tooltip) takarja az elemet, így nem lehet rákattintani                                |

---

## 🛠️ Tippek a problémák kezelésére

* Használj **explicit wait**-et, hogy csak akkor lépj tovább, amikor az elem tényleg használható.
* Ellenőrizd az elemek **lokátorait**, legyenek stabilak és egyediek.
* Figyeld az oldal dinamikus viselkedését (pl. AJAX, JavaScript események).
* Ha `StaleElementReferenceException` jön elő, próbáld újra lekérni az elemet.
* Ha `ElementClickInterceptedException` jelentkezik, várj, amíg a zavaró elem eltűnik (pl. modal bezáródik).

---

#### ✅ Hasonlítsd össze a POM és a Keyword Driven Testing megközelítéseket!
Persze! Íme egy összehasonlító áttekintés a **Page Object Model (POM)** és a **Keyword Driven Testing (KDT)** megközelítések között, amik mindkettő népszerű automatizált tesztelési stratégia:

---

## 🔍 Összehasonlítás: POM vs. Keyword Driven Testing

| Jellemző               | Page Object Model (POM)                                                            | Keyword Driven Testing (KDT)                                                                                      |
| ---------------------- | ---------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| **Fogalom**            | OOP alapú tervezési minta, ahol minden weboldal vagy oldalrész egy osztály         | Tesztelési megközelítés, ahol a tesztesetek kulcsszavak (parancsok) alapján épülnek fel                           |
| **Fókusz**             | Weboldal elemeinek és műveleteinek absztrakciója (objektumként)                    | Funkciók és műveletek absztrakciója kulcsszavakkal                                                                |
| **Megvalósítás**       | Kód alapú: osztályok és metódusok reprezentálják az oldalakat és műveleteket       | Kulcsszavak, melyeket egy motor értelmez, és ezek végrehajtják a műveleteket                                      |
| **Tesztírás módja**    | Tesztkód írása, ahol a teszt hívja meg a POM osztályokat és metódusokat            | Tesztesetek írása táblázatokban vagy fájlokban kulcsszavakkal, kód nélkül vagy kevés kódolással                   |
| **Előnyök**            | - Jobb karbantarthatóság<br>- Kód újrahasznosítás<br>- Tiszta, moduláris szerkezet | - Könnyű tesztírás nem programozóknak<br>- Átlátható, táblázatos formátum<br>- Könnyű bővíthetőség kulcsszavakkal |
| **Hátrányok**          | - Programozói ismereteket igényel<br>- Magasabb kezdeti fejlesztési költség        | - Kulcsszó motor fejlesztése szükséges<br>- Nagyobb komplexitás esetén bonyolultabb lehet<br>- Nehéz hibakeresés  |
| **Használati terület** | Főként fejlesztők és automatizálók körében, komplex UI tesztekhez                  | Gyakran használják üzleti felhasználók vagy kevés programozói tapasztalattal rendelkezők                          |

---

## 📝 Röviden

* **POM**: Objektum-orientált modell, ahol az oldalakat kód formájában modellezzük, ami segíti a karbantartást és az újrahasznosítást.
* **KDT**: Kulcsszavakra épülő tesztelés, ahol a teszt lépéseket egyszerű, előre definiált parancsokkal írjuk le, így nem szükséges mély programozói tudás.

---

#### ✅ Mi a különbség a TDD és BDD között?
Szívesen! Íme a **TDD (Test-Driven Development)** és a **BDD (Behavior-Driven Development)** közötti fő különbségek összefoglalója:

---

## TDD vs BDD – Fő különbségek

| Jellemző         | TDD (Test-Driven Development)                                                       | BDD (Behavior-Driven Development)                                                                                      |
| ---------------- | ----------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| **Fókusz**       | A kód működésének helyessége, egységtesztek írják a kódot                           | A szoftver viselkedése, funkcionális követelmények                                                                     |
| **Teszt típusa** | Egységtesztek (unit tests)                                                          | Funkcionális tesztek, elfogadási tesztek (acceptance tests)                                                            |
| **Teszt írása**  | Fejlesztők írják, programozási nyelven                                              | Fejlesztők, tesztelők és üzleti oldali szereplők közösen írják, természetes nyelvhez közel álló formában (pl. Gherkin) |
| **Módszertan**   | "Red-Green-Refactor" ciklus: először sikertelen teszt, aztán kód, majd refaktorálás | Sztorik, felhasználói történetek leírása, tesztek a viselkedés alapján                                                 |
| **Kommunikáció** | Fejlesztő-központú                                                                  | Csapat- és üzletközpontú, jobb együttműködés a nem technikai szereplőkkel                                              |
| **Eszközök**     | JUnit, NUnit, pytest stb.                                                           | Cucumber, SpecFlow, Behave stb.                                                                                        |
| **Cél**          | Biztosítani, hogy a kód megfeleljen a specifikációnak                               | Biztosítani, hogy a szoftver viselkedése megfeleljen az üzleti elvárásoknak                                            |

---

## Rövid magyarázat

* **TDD**: Először írsz egy tesztet, ami eleinte nem fut le (fail), majd megírod a kódot, hogy sikeres legyen a teszt, végül javítasz a kódon. Ez a fejlesztési folyamat szerves része.
* **BDD**: Inkább az üzleti értékekre és viselkedésre fókuszál, a teszteket gyakran természetes nyelvhez közeli szintaxissal (pl. Given-When-Then) írják, hogy minden érintett megértse.

---

#### ✅ Mi az API tesztelés és miért hasznos?
Persze! Íme egy áttekintés az **API tesztelésről** és annak hasznosságáról:

---

## Mi az API tesztelés?

* **API (Application Programming Interface)** egy interfész, amely lehetővé teszi különböző szoftverek vagy rendszerek közötti kommunikációt.
* Az **API tesztelés** azt jelenti, hogy ellenőrizzük ezeket az interfészeket, hogy megbizonyosodjunk arról, hogy az API megfelelően működik, helyes adatokat ad vissza, és kezeli a hibákat.
* Ez a tesztelés általában nem a felhasználói felületet érinti, hanem a háttérben futó funkciókat, szolgáltatásokat.

---

## Miért hasznos az API tesztelés?

* **Gyorsabb és stabilabb tesztek:** Az API tesztek általában gyorsabban futnak, mert nem kell a GUI-t betölteni vagy kezelni.
* **Korai hibafelismerés:** Az API réteg hibái gyakran a legkorábbiak, így korán javíthatók.
* **Független a UI-tól:** Az UI változásai nem befolyásolják az API teszteket, így megbízhatóbbak.
* **Biztosítja az adatcserét:** Ellenőrzi, hogy az adatok helyesen kerülnek átvitelre és feldolgozásra a rendszerek között.
* **Automatizálható:** Könnyen automatizálható, így támogatja a CI/CD folyamatokat.
* **Funkcionalitás, biztonság és teljesítmény tesztelése:** Nemcsak a helyes működés, hanem a jogosultságok, jogosultsági szintek és válaszidők is tesztelhetők.

---

## Tipikus API tesztelési feladatok

* Helyes válasz visszakapása (status code, body)
* Hibakezelés vizsgálata
* Adatvalidáció (inputok és outputok)
* Hitelesítés és engedélyezés
* Teljesítmény és terhelés tesztelése

---

#### ✅ Mi az adatvezérelt tesztelés és miért hasznos?
Persze! Íme egy összefoglaló az **adatvezérelt tesztelésről** és annak előnyeiről:

---

## Mi az adatvezérelt tesztelés?

* Az **adatvezérelt tesztelés** (Data-Driven Testing, DDT) egy olyan automatizált tesztelési megközelítés, ahol a tesztesetek logikája ugyanaz marad, de különböző bemeneti adatokkal futtatjuk őket.
* A tesztadatokat általában külső forrásból olvassuk be, például táblázatokból (Excel, CSV), adatbázisból vagy JSON/XML fájlokból.
* Ez lehetővé teszi, hogy ugyanazt a tesztet többször, különböző adatkombinációkkal hajtsuk végre.

---

## Miért hasznos az adatvezérelt tesztelés?

* **Újrahasznosítható tesztesetek:** Nem kell minden adatkombinációhoz külön tesztet írni.
* **Könnyű bővíthetőség:** Csak új adatokat kell hozzáadni, nem a tesztkódot módosítani.
* **Hatékony hibakeresés:** Egy teszt több adat esetén is lefut, így könnyebb megtalálni, mely adatok okoznak problémát.
* **Karbantarthatóság:** A tesztlogika és az adatok szétválasztása átláthatóbbá teszi a tesztkódot.
* **Jobb lefedettség:** Több adatkombinációval alaposabb tesztelés érhető el.

---

## Példa

Ha például egy bejelentkezési funkciót tesztelsz, az adatvezérelt teszt egyetlen kódot használ, ami különböző felhasználónév/jelszó párokat tesztel:

| Felhasználónév | Jelszó    | Várható eredmény         |
| -------------- | --------- | ------------------------ |
| user1          | pass1     | Sikeres bejelentkezés    |
| user2          | wrongpass | Sikertelen bejelentkezés |

---

#### ✅ Mik a kihívások és ajánlott eljárások a dinamikusan betöltött webes elemekkel?

#### ✅ Mik a mobil tesztautomatizálás kihívásai?

## Haladó témák
<img src="https://www.softwaretestinghelp.com/wp-content/qa/uploads/2020/05/DevOps-in-a-Selenium-Testing.png" alt="image" width="320" height="220">

#### ✅ Mi a különbség a CI és CD között?
#### ✅ Írj le egy Continuous Delivery folyamatot!
#### ✅ Hasonlítsd össze két népszerű CI rendszert, ezek közül az egyik legyen a Jenkins!
#### ✅ Mi a Docker és miért hasznos?