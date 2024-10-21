

# RENDSZERTERV.md

## Logikai rendszerterv

### 1. Üzleti folyamatok modellje

#### 1.1 Üzleti domain modell

A weboldal egy online Plinko játékot valósít meg, amely a népszerű televíziós műsor, a "The Price is Right" játékán alapul. A játék során a játékosok labdát dobnak le egy piramis alakú, tüskékkel teli táblán, és várják, hogy az melyik nyereményt tartalmazó rekeszbe esik. A labda gravitáció segítségével esik le, miközben a tüskékről lepattanva véletlenszerű útvonalat jár be. A játékos nyereménye attól függ, hogy a labda melyik rekeszbe érkezik.

#### 1.2 Üzleti szereplők

- **Regisztrált felhasználók**: Akik játszhatnak a Plinko játékkal, pénzt vagy pontokat nyerhetnek, megtekinthetik a ranglistát, és szerkeszthetik a profiljukat.
- **Vendég felhasználók**: Akik regisztráció nélkül kipróbálhatják a játékot, de nyereményeiket nem menti a rendszer.
- **Adminisztrátor**: Kezeli a felhasználókat, felügyeli a játékot, és karbantartja a rendszert.

#### 1.3 Üzleti entitások

- **Felhasználók**
- **Játékok**
- **Tétek**
- **Nyeremények**
- **Ranglisták**

### 2. Követelmények

#### 2.1 Funkcionális követelmények

- Felhasználói regisztráció és bejelentkezés.
- Plinko játék lejátszása animációval.
- Különböző kockázati szintek (alacsony, közepes, magas) választása.
- Sorok számának beállítása (8-16 sor).
- Tét összegének megadása.
- Nyeremények számítása és jóváírása.
- Ranglista megjelenítése a legjobb játékosokkal.
- Felhasználói profil megtekintése és szerkesztése.
- Játéktörténet megtekintése.
- Vendég módú játék lehetősége.

#### 2.2 Nemfunkcionális követelmények

- **Reszponzív design**: A weboldal mobil eszközökön is jól működik.
- **Teljesítmény**: Gyors betöltési idő és zökkenőmentes játékélmény.
- **Biztonság**: Biztonságos adatkezelés és tranzakciók.
- **Skálázhatóság**: Növekvő felhasználói bázis és tranzakciók kezelésére alkalmas.

| Funkció                           | Részletes leírás                                                                                                                                       |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Regisztráció lap**              | A felhasználó megadja a felhasználónevét, email címét és jelszavát.                                                                                    |
| **Bejelentkezés lap**             | A felhasználó bejelentkezik az email címével és jelszavával.                                                                                           |
| **Plinko játék felület**          | A játékos beállítja a kockázati szintet, a sorok számát, a tét összegét, majd elindítja a játékot.                                                     |
| **Kockázati szint választása**    | Három opció: alacsony, közepes, magas. A magasabb kockázat nagyobb nyereményt, de kisebb esélyt jelent.                                                |
| **Sorok számának beállítása**     | A játékos 8 és 16 sor között választhat. Több sor nagyobb nyereményeket, de kisebb esélyt jelent.                                                       |
| **Tét összegének megadása**       | A játékos megadja a fogadni kívánt összeget a megengedett minimum és maximum között.                                                                   |
| **Nyeremény kiszámítása**         | A labda leesése után a rendszer kiszámítja a nyereményt a tét és a szorzó alapján.                                                                     |
| **Pontszám mentése**              | A játék végeztével a rendszer elmenti a felhasználó nyereményét és frissíti az egyenlegét.                                                             |
| **Ranglista megjelenítése**       | A legjobb játékosok listájának megjelenítése a nyeremények alapján.                                                                                    |
| **Profil szerkesztése**           | A felhasználó módosíthatja a profilképét, felhasználónevét és jelszavát.                                                                               |
| **Játéktörténet megtekintése**    | A felhasználó megtekintheti korábbi játékait és nyereményeit.                                                                                          |
| **Vendég mód**                    | Regisztráció nélküli játék lehetősége, nyeremények mentése nélkül.                                                                                     |
| **Adminisztrációs felület**       | Az adminisztrátor felhasználókat kezelhet, ellenőrizheti a játékokat és a tranzakciókat.                                                               |

### 3. Feldolgozási folyamatok

#### 3.1 Használati esetek

- **Regisztráció**: A felhasználó megadja az adatait, és létrehoz egy fiókot.
- **Bejelentkezés**: A felhasználó bejelentkezik a rendszerbe.
- **Játék beállítása**: A felhasználó kiválasztja a kockázati szintet, sorok számát és megadja a tét összegét.
- **Játék indítása**: A felhasználó elindítja a Plinko játékot.
- **Labda leejtése**: A rendszer szimulálja a labda mozgását és megjeleníti az animációt.
- **Nyeremény kiszámítása**: A rendszer kiszámítja a nyereményt a tét és a szorzó alapján.
- **Nyeremény jóváírása**: A rendszer frissíti a felhasználó egyenlegét.
- **Ranglista megtekintése**: A felhasználó megtekinti a legjobb játékosok listáját.
- **Profil szerkesztése**: A felhasználó módosítja a profilját.
- **Játéktörténet megtekintése**: A felhasználó megtekinti korábbi játékait és nyereményeit.

#### 3.2 Aktivitási diagramok

**Játék folyamat**

```
[Felhasználó] --> [Bejelentkezés/Regisztráció] --> [Játék beállítása] --> [Játék indítása] --> [Labda leejtése és animáció] --> [Nyeremény kiszámítása] --> [Nyeremény jóváírása] --> [Ranglista frissítése]
```

**Profil szerkesztése**

```
[Felhasználó] --> [Bejelentkezés] --> [Profil oldal] --> [Adatok módosítása] --> [Mentés] --> [Visszaigazolás]
```

#### 3.3 Szekvencia diagramok

**Játék indítása és nyeremény jóváírása**

1. A felhasználó beállítja a játék paramétereit.
2. A felhasználó elindítja a játékot.
3. A rendszer ellenőrzi a felhasználó egyenlegét és levonja a tétet.
4. A rendszer szimulálja a labda mozgását és megjeleníti az animációt.
5. A rendszer kiszámítja a nyereményt.
6. A rendszer jóváírja a nyereményt a felhasználó egyenlegén.
7. A rendszer frissíti a ranglistát.

### 4. Funkcionális felépítés

#### 4.1 Komponensek

- **Front-end**: Blade sablonok, CSS (Bootstrap 5), JavaScript (pl. Vue.js vagy React), HTML5 Canvas az animációhoz.
- **Back-end**: Laravel keretrendszer, vezérlők, modellek, útvonalak.
- **Adatbázis**: MySQL vagy MariaDB.

### 5. Adatmodell

![Adatmodell ábra](../pic/plinko_adatmodell.jpg?raw=true "Adatmodell")

#### 5.1 Felhasználók

| Oszlopnév    | Típus          | Leírás                       |
|--------------|----------------|------------------------------|
| id           | INT (auto-incr)| Egyedi azonosító             |
| username     | VARCHAR(255)   | Felhasználónév               |
| email        | VARCHAR(255)   | Email cím (egyedi)           |
| password     | VARCHAR(255)   | Jelszó (hash-elve)           |
| balance      | DECIMAL(10,2)  | Felhasználó egyenlege        |
| avatar       | VARCHAR(255)   | Profilkép URL                |
| created_at   | TIMESTAMP      | Létrehozás dátuma            |
| updated_at   | TIMESTAMP      | Módosítás dátuma             |

#### 5.2 Játékok

| Oszlopnév    | Típus          | Leírás                       |
|--------------|----------------|------------------------------|
| id           | INT (auto-incr)| Egyedi azonosító             |
| user_id      | INT            | Felhasználó azonosítója      |
| bet_amount   | DECIMAL(10,2)  | Tét összege                  |
| risk_level   | ENUM           | Kockázati szint (alacsony, közepes, magas) |
| rows         | INT            | Sorok száma (8-16)           |
| payout       | DECIMAL(10,2)  | Nyeremény összege            |
| result_slot  | INT            | A rekesz, ahol a labda landolt |
| played_at    | TIMESTAMP      | Játék időpontja              |
| created_at   | TIMESTAMP      | Létrehozás dátuma            |
| updated_at   | TIMESTAMP      | Módosítás dátuma             |

#### 5.3 Ranglista

A ranglistát a **Játékok** tábla adatai alapján számítjuk, a felhasználók összesített nyereménye szerint.

### 6. Felhasználói felületek, menük

- **Főoldal**: Bejelentkezési és regisztrációs lehetőség, játék indítása vendég módban.
- **Játék felület**: Beállítások megadása (kockázati szint, sorok száma, tét), Plinko tábla megjelenítése, labda leejtése.
- **Profil oldal**: Felhasználói adatok megjelenítése és szerkesztése, egyenleg megtekintése.
- **Ranglista oldal**: Legjobb játékosok listája nyeremények alapján.
- **Játéktörténet oldal**: Korábbi játékok és nyeremények megtekintése.

### 7. Adatszótár, logikai adatmodell

Az adatszótár tartalmazza az adatbázis mezőit és azok jelentését, lásd az **Adatmodell** fejezetben.

### 8. Adatfolyam diagramok

Az adatfolyam a felhasználói interakcióktól indul, átmegy a vezérlőkön és modelleken, majd az adatbázison keresztül visszatér a felhasználói felületre.

### 9. Rendszer célja

A rendszer célja, hogy szórakoztató és izgalmas játékélményt nyújtson a felhasználóknak, lehetőséget adva a nyeremények megszerzésére és a versengésre, miközben modern webes technológiákat alkalmaz a legjobb felhasználói élmény érdekében.

## Fizikai rendszerterv

### 1. Osztály tervek

Az alkalmazás a Laravel MVC architektúrát követi.

#### 1.1 Modellek

- **User**: Felhasználói adatokat és egyenleget kezeli.
- **Game**: Játék adatokat, téteket és nyereményeket kezeli.

#### 1.2 Vezérlők

- **AuthController**: Regisztráció és bejelentkezés.
- **GameController**: Játék logika és játékhoz kapcsolódó műveletek.
- **ProfileController**: Profil megtekintése és szerkesztése.
- **LeaderboardController**: Ranglista megjelenítése.
- **BalanceController**: Egyenleg kezelése (befizetések, kifizetések).

### 2. Adatbázis terv

- **users** tábla: Felhasználói adatok és egyenleg tárolása.
- **games** tábla: Játékok, tétek és nyeremények tárolása.
- **transactions** tábla: Befizetések és kifizetések naplózása (opcionális).

### 3. Teszttervek

- **Egységtesztek**: Modellek és vezérlők tesztelése.
- **Integrációs tesztek**: Teljes folyamatok tesztelése (pl. játék indítása, nyeremény jóváírása).
- **Felhasználói tesztek**: Felület tesztelése különböző eszközökön és böngészőkben.
- **Biztonsági tesztek**: Bejelentkezés, adatvédelem és tranzakciók tesztelése.

### 4. Telepítési terv

- **Szerver**: PHP 8+, Laravel 10+, MySQL/MariaDB.
- **Lépések**:
  - Kód letöltése a verziókezelőből (Git).
  - Függőségek telepítése (`composer install`, `npm install`).
  - Környezeti változók beállítása (adatbázis kapcsolatok, API kulcsok).
  - Adatbázis migrációk és seederek futtatása (`php artisan migrate --seed`).
  - Alkalmazás kulcs generálása (`php artisan key:generate`).
  - Alkalmazás cache-ek generálása (`php artisan config:cache`, `php artisan route:cache`).

### 5. Rendszerspecifikációk

- **Fejlesztési környezet**: Laravel, PHP, MySQL/MariaDB, Node.js (front-end build eszközök).
- **Futtatási környezet**: Webszerver PHP támogatással (Apache, Nginx), SSL tanúsítvánnyal a biztonságos kapcsolatokhoz.

### 6. Szoftver architektúra

Az alkalmazás MVC architektúrát követ, a Laravel keretrendszer struktúrájával. A front-end interaktív elemeihez JavaScript és HTML5 Canvas technológiát használunk az animációk megvalósításához.

### 7. Adatspecifikációk/objektumspecifikációk

Az adatok objektumorientált módon kerülnek kezelésre az Eloquent ORM segítségével, amely megkönnyíti az adatbázis műveleteket és a modellek közötti kapcsolatokat.

### 8. Programspecifikációk

#### Modulvázak

- **AuthController**
  - `register()`: Felhasználó regisztrálása.
  - `login()`: Felhasználó bejelentkezése.
  - `logout()`: Kijelentkezés.
- **GameController**
  - `index()`: Játék felület megjelenítése.
  - `play(Request $request)`: Játék indítása, paraméterek fogadása, játék logika végrehajtása.
  - `calculatePayout()`: Nyeremény kiszámítása.
- **ProfileController**
  - `show()`: Profil megtekintése.
  - `edit()`: Profil szerkesztése.
  - `update(Request $request)`: Profil módosításainak mentése.
- **LeaderboardController**
  - `index()`: Ranglista megjelenítése.
- **BalanceController**
  - `deposit()`: Befizetés kezelése.
  - `withdraw()`: Kifizetés kezelése.

---

# KOVSPEC.md

## 1. Áttekintés

Ez a dokumentum a Plinko weboldal követelmény specifikációit tartalmazza. A cél egy modern, interaktív online Plinko játék fejlesztése, amely lehetővé teszi a felhasználók számára a játékot, tétek elhelyezését, nyeremények megszerzését és versengést a ranglistán.

## 2. Jelenlegi Helyzet

Jelenleg kevés olyan online platform létezik, amely a Plinko játékot valós pénzes tétekkel és nyereményekkel kínálja egy biztonságos és megbízható környezetben. A játékosok olyan platformot keresnek, ahol élvezhetik a játékot, és esélyük van nagy nyeremények elérésére.

## 3. Vágyálom rendszer

Egy reszponzív webalapú Plinko játék, amely lehetővé teszi a felhasználóknak:

- Regisztrációt és bejelentkezést.
- Valódi pénzes tétek elhelyezését.
- Különböző kockázati szintek és sorok számának beállítását.
- Nyeremények megszerzését a labda véletlenszerű mozgása alapján.
- Ranglistán való versengést.
- Profiljuk testreszabását.
- Befizetéseket és kifizetéseket biztonságosan lebonyolítani.

## 4. Funkcionális követelmények

- **Felhasználói regisztráció és bejelentkezés**.
- **Tét elhelyezése**: A felhasználó megadhatja a tét összegét a megengedett minimum és maximum között.
- **Kockázati szint választása**: Alacsony, közepes vagy magas kockázati szint kiválasztása.
- **Sorok számának beállítása**: 8 és 16 sor között.
- **Játék indítása és labda leejtése**.
- **Nyeremény kiszámítása és jóváírása**.
- **Egyenleg kezelése**: Befizetések és kifizetések lebonyolítása.
- **Ranglista megjelenítése**.
- **Profil szerkesztése**.
- **Játéktörténet megtekintése**.
- **Vendég mód**: Játék lehetősége regisztráció nélkül, nyeremények mentése nélkül.

## 5. Törvények

- **GDPR**: Megfelelés az adatvédelmi előírásoknak.
- **Szerencsejáték törvények**: Megfelelés a helyi szerencsejáték szabályozásoknak és engedélyeknek.
- **Pénzmosás elleni szabályozások**: KYC (Ismerd meg az ügyfeled) és tranzakciók ellenőrzése.

## 6. Jelenlegi üzleti folyamatok modellje

A játékosok különböző online kaszinó oldalakon játszanak, de ezek gyakran nem nyújtanak megfelelő biztonságot vagy nem kínálják a Plinko játékot.

## 7. Igényelt üzleti folyamatok modellje

- **Regisztráció és bejelentkezés**: A felhasználók létrehozhatják a fiókjukat és bejelentkezhetnek.
- **Egyenleg feltöltése**: Biztonságos befizetések kezelése.
- **Játék beállítása**: Tét összegének megadása, kockázati szint és sorok számának kiválasztása.
- **Játék indítása**: Labda leejtése és nyeremény kiszámítása.
- **Nyeremény jóváírása**: Nyeremények automatikus jóváírása a felhasználó egyenlegére.
- **Kifizetés kérése**: Nyeremények kifizetése a felhasználó számára.
- **Ranglista megtekintése**: A legjobb játékosok megtekintése.
- **Profil kezelése**: Felhasználói adatok szerkesztése.

## 8. Fogalomtár

- **Plinko**: Kaszinó játék, ahol a labdát leejtik egy piramis alakú, tüskékkel teli táblán, és a labda véletlenszerűen pattogva érkezik meg egy rekeszbe, amely meghatározza a nyereményt.
- **Kockázati szint**: A játék nehézségi szintje, amely befolyásolja a nyeremények mértékét és esélyét.
- **Sorok száma**: A tábla magassága, amely meghatározza a tüskék számát és a lehetséges útvonalak számát.
- **Tét**: Az a pénzösszeg, amelyet a játékos a játékba helyez.
- **Nyeremény**: A játékos által nyert pénzösszeg a tét és a szorzó alapján.

## 9. Követelménylista

| Funkció                         | Részletes leírás                                                                                         |
|---------------------------------|----------------------------------------------------------------------------------------------------------|
| **Regisztráció lap**            | Felhasználói fiók létrehozása felhasználónév, email és jelszó megadásával.                               |
| **Bejelentkezés lap**           | Bejelentkezés a rendszerbe email és jelszó megadásával.                                                  |
| **Egyenleg feltöltése**         | Befizetés bankkártyával vagy más fizetési móddal.                                                        |
| **Játék beállítása**            | Tét összegének, kockázati szintnek és sorok számának megadása.                                           |
| **Játék indítása**              | Labda leejtése és animáció megjelenítése.                                                                |
| **Nyeremény kiszámítása**       | Nyeremény meghatározása a labda végső pozíciója és a szorzó alapján.                                     |
| **Nyeremény jóváírása**         | Nyeremény automatikus hozzáadása a felhasználó egyenlegéhez.                                             |
| **Ranglista megtekintése**      | Legjobb játékosok listájának megtekintése a nyeremények alapján.                                         |
| **Profil szerkesztése**         | Felhasználói adatok és profilkép módosítása.                                                             |
| **Játéktörténet megtekintése**  | Korábbi játékok, tétek és nyeremények megtekintése.                                                     |
| **Kifizetés kérése**            | Nyeremények kifizetésének kezdeményezése.                                                                |
| **Vendég mód**                  | Játék lehetősége regisztráció nélkül, nyeremények mentése nélkül.                                        |
| **Jelszó visszaállítás**        | Elfelejtett jelszó esetén email alapú visszaállítás.                                                     |
| **Kilépés gomb**                | Kijelentkezés a fiókból.                                                                                 |

---

# FUNKSPEC.md

## 1. Bevezetés

### 1.1 Cél

A dokumentum célja a Plinko weboldal funkcionális specifikációjának részletes bemutatása, amely alapján a fejlesztők elkészíthetik a rendszert.

### 1.2 Jelenlegi Helyzet

Jelenleg kevés olyan online platform létezik, amely a Plinko játékot valós pénzes tétekkel kínálja egy biztonságos és felhasználóbarát környezetben. A játékosok olyan weboldalt keresnek, ahol élvezhetik a játékot, és esélyük van nagy nyeremények elérésére.

### 1.3 Hatály

A dokumentum a Plinko weboldal fejlesztésére vonatkozik, amelyet három fejlesztő valósít meg öt hét alatt, teszteléssel együtt.

## 2. Rendszerleírás

### 2.1 Rendszer célja

Az online Plinko játék lehetőséget biztosít a felhasználóknak a játékra, valódi pénzes tétek elhelyezésére, nyeremények megszerzésére és versengésre a ranglistán, mindezt egy biztonságos és megbízható környezetben.

### 2.2 Felhasználói esetek (Use-Case)

- **Regisztráció és bejelentkezés**
- **Egyenleg feltöltése**
- **Játék beállítása és indítása**
- **Nyeremény kiszámítása és jóváírása**
- **Ranglista megtekintése**
- **Profil szerkesztése**
- **Játéktörténet megtekintése**
- **Kifizetés kérése**
- **Vendég módú játék**

## 3. Funkcionális követelmények

### 3.1 Regisztráció/Bejelentkezés

- Felhasználói fiók létrehozása felhasználónév, email és jelszó megadásával.
- Email cím egyediségének ellenőrzése.
- Bejelentkezés után a felhasználó hozzáfér a teljes funkcionalitáshoz.
- Jelszó visszaállítás email alapján.

### 3.2 Egyenleg kezelése

- **Befizetés**: Bankkártya, PayPal vagy kriptovaluta használatával.
- **Kifizetés**: Kérelem benyújtása, tranzakciók ellenőrzése.

### 3.3 Játék beállítása

- **Tét megadása**: Minimum és maximum tét összegének betartása.
- **Kockázati szint kiválasztása**: Alacsony, közepes, magas.
- **Sorok számának beállítása**: 8 és 16 között.

### 3.4 Játék indítása és lejátszása

- A labda leejtése a tábla tetején.
- Animáció megjelenítése a labda mozgásáról.
- A labda véletlenszerű útvonalat jár be a tüskék között.

### 3.5 Nyeremény kiszámítása és jóváírása

- A nyeremény a tét és a rekeszhez tartozó szorzó szorzata.
- A szorzók a kockázati szint és a sorok száma alapján változnak.
- Nyeremény automatikus jóváírása a felhasználó egyenlegére.

### 3.6 Ranglista

- Legjobb játékosok megjelenítése a nyeremények alapján.
- Szűrési lehetőségek: napi, heti, havi, összesített.

### 3.7 Profil kezelése

- Felhasználói adatok és profilkép módosítása.
- Jelszó megváltoztatása.
- Egyenleg megtekintése.

### 3.8 Játéktörténet

- Korábbi játékok, tétek, nyeremények és játék paraméterek megtekintése.

### 3.9 Vendég mód

- Játék lehetősége regisztráció nélkül.
- Nyeremények és tétek nem kerülnek mentésre.

## 4. Nem-funkcionális követelmények

- **Reszponzív design** minden eszközön.
- **Teljesítmény**: Gyors betöltés és gördülékeny működés.
- **Biztonság**: Felhasználói adatok és tranzakciók védelme.
- **Skálázhatóság**: Növekvő felhasználói szám és tranzakciók kezelése.
- **Felhasználóbarát felület**: Könnyű navigáció és használat.
- **Megbízhatóság**: Stabil működés, hibamentes játékélmény.

## 5. Rendszer működése

### 5.1 Játék folyamat

1. A felhasználó bejelentkezik vagy vendég módban játszik.
2. Egyenleg feltöltése (ha szükséges).
3. Beállítja a játék paramétereit: tét, kockázati szint, sorok száma.
4. A "Játék indítása" gombra kattint.
5. A labda leejtése és animáció megjelenítése.
6. A labda megérkezik egy rekeszbe, nyeremény kiszámítása.
7. Nyeremény jóváírása a felhasználó egyenlegére.
8. Ranglista frissítése.

### 5.2 Nyeremény számítása

- **Szorzók**: A rekeszekhez tartozó szorzók előre meghatározottak a kockázati szint és sorok száma alapján.
- **Nyeremény**: Nyeremény = Tét * Szorzó.

## 6. Adatmodell

![Adatmodell ábra](../pic/plinko_adatmodell.jpg?raw=true "Adatmodell")

### 6.1 Felhasználók

| Oszlopnév  | Típus          | Leírás                    |
|------------|----------------|---------------------------|
| id         | INT (auto-incr)| Egyedi azonosító          |
| username   | VARCHAR(255)   | Felhasználónév            |
| email      | VARCHAR(255)   | Email cím (egyedi)        |
| password   | VARCHAR(255)   | Jelszó (hash-elve)        |
| balance    | DECIMAL(10,2)  | Felhasználó egyenlege     |
| avatar     | VARCHAR(255)   | Profilkép URL             |
| created_at | TIMESTAMP      | Létrehozás dátuma         |
| updated_at | TIMESTAMP      | Módosítás dátuma          |

### 6.2 Játékok

| Oszlopnév   | Típus          | Leírás                     |
|-------------|----------------|----------------------------|
| id          | INT (auto-incr)| Egyedi azonosító           |
| user_id     | INT            | Felhasználó azonosítója    |
| bet_amount  | DECIMAL(10,2)  | Tét összege                |
| risk_level  | ENUM           | Kockázati szint            |
| rows        | INT            | Sorok száma                |
| payout      | DECIMAL(10,2)  | Nyeremény összege          |
| result_slot | INT            | Rekesz száma               |
| played_at   | TIMESTAMP      | Játék időpontja            |
| created_at  | TIMESTAMP      | Létrehozás dátuma          |
| updated_at  | TIMESTAMP      | Módosítás dátuma           |

### 6.3 Tranzakciók (opcionális)

| Oszlopnév   | Típus          | Leírás                     |
|-------------|----------------|----------------------------|
| id          | INT (auto-incr)| Egyedi azonosító           |
| user_id     | INT            | Felhasználó azonosítója    |
| type        | ENUM           | Tranzakció típusa (befizetés, kifizetés) |
| amount      | DECIMAL(10,2)  | Összeg                     |
| status      | ENUM           | Tranzakció állapota        |
| created_at  | TIMESTAMP      | Létrehozás dátuma          |
| updated_at  | TIMESTAMP      | Módosítás dátuma           |

## 7. Megvalósítás

### 7.1 Használt Technológiák

- **Backend**: PHP 8+, Laravel 10+
- **Frontend**: HTML5, CSS3, Bootstrap 5, JavaScript, Vue.js vagy React, HTML5 Canvas
- **Adatbázis**: MySQL vagy MariaDB
- **Verziókezelés**: Git, GitHub

### 7.2 Fejlesztői eszközök

- **IDE**: Visual Studio Code vagy PHPStorm
- **Függőségkezelő**: Composer, NPM
- **Szerver**: XAMPP, MAMP vagy Docker
- **Egyéb**: Postman (API teszteléshez), PHPUnit (teszteléshez)

## 8. Üzleti folyamatok modellje

### 8.1 Jelenlegi üzleti folyamatok modellje

A játékosok különböző online kaszinó oldalakon játszanak, amelyek nem mindig nyújtanak biztonságos és megbízható szolgáltatást, vagy nem kínálják a Plinko játékot.

### 8.2 Igényelt üzleti folyamatok modellje

Egy megbízható, biztonságos és felhasználóbarát weboldal, ahol a felhasználók élvezhetik a Plinko játékot, valódi pénzes tétekkel játszhatnak, és esélyük van nagy nyeremények elérésére.

## 9. Fogalomtár

- **Plinko tábla**: A játék felülete, amely egy piramis alakú, tüskékkel teli tábla.
- **Labda**: A játékban használt elem, amelyet a játékos "leejt".
- **Rekesz**: A tábla alján található mezők, amelyek meghatározzák a nyereményt.
- **Tét**: A játékos által fogadott pénzösszeg.
- **Szorzó**: A nyeremény kiszámításához használt érték, amely a rekeszhez tartozik.
- **Kockázati szint**: A játék nehézségi szintje, amely befolyásolja a szorzókat és a nyerési esélyeket.

## 10. Követelménylista

| Funkció                         | Részletes leírás                                                                                         |
|---------------------------------|----------------------------------------------------------------------------------------------------------|
| **Regisztráció lap**            | Felhasználói fiók létrehozása.                                                                           |
| **Bejelentkezés lap**           | Bejelentkezés a rendszerbe.                                                                              |
| **Egyenleg feltöltése**         | Befizetés kezelése különböző fizetési módokkal.                                                          |
| **Játék beállítása**            | Tét, kockázati szint és sorok számának megadása.                                                         |
| **Játék indítása gomb**         | A játék elindítása.                                                                                      |
| **Plinko tábla megjelenítése**  | Játékfelület és animáció megjelenítése.                                                                  |
| **Labda leejtése**              | A labda mozgásának szimulációja a táblán.                                                                |
| **Nyeremény megjelenítése**     | Az elért nyeremény megjelenítése a játék végén.                                                          |
| **Nyeremény jóváírása**         | Nyeremény automatikus jóváírása az egyenlegre.                                                           |
| **Ranglista megtekintése**      | A legjobb játékosok listájának megtekintése.                                                             |
| **Profil szerkesztése**         | Felhasználói adatok és profilkép módosítása.                                                             |
| **Játéktörténet megtekintése**  | Korábbi játékok és nyeremények megtekintése.                                                             |
| **Kifizetés kérése**            | Nyeremények kifizetésének kezdeményezése.                                                                |
| **Kilépés gomb**                | Kijelentkezés a fiókból.                                                                                 |

---

A fenti dokumentáció alapján a rendszer érthetően és részletesen kidolgozott, így a fejlesztők számára egyértelmű a megvalósítandó feladat. A Laravel keretrendszer használatával és a megadott időkereten belül a projekt elkészíthető.
