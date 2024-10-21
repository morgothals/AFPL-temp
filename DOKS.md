



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
