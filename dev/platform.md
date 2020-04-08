 # Platform

A projekt működését több REST alapú szolgáltatás összessége teszi lehetővé amihez ebben a sávban lehet hasznos dokumentációt, leírásokat találni.

## API
Api dokumentáció az oldal sávon található meg egy postman oldal formájában.

## Modulok
A platform többféle modulból épül fel amik folyamatos fejlesztés alatt álnak. 

A projekt tartalmaz publikus és privát modulokat. A kategorizálás az alapján dől el hogy egy kliens milyen szinten interaktálhat egy modullal.

### Publikus

* **Gateway**

Elérhetővé teszi a többi modult, biztonsági és követési funkciókat lát el. Néha egyébb segéd funkciókat is ellát.

* **Auth modul**

Feladatkörébe tartozik a felhasználók alapvető kezelése beleértve a belépést, engedély kezelést, és törlést.

* **Házizz modul** 

A projekt főszolgáltását tartalmazza, feladata a feladatok, csoportok, és egyébb ezekhez kapcsolódó tartalmak kezelése.

* **Théra modul**

Théra modul feladata integrációs lehetőségeket kínálni külsős szolgáltatásokkal, és feladata ezeket megbízható módon a felhasználó számára elérhetővé tenni.

### Privát

* [**Kreta proxy modul**](https://github.com/hazizz/kreta-proxy) *nyilforráskódú*

Egy átjátszó modul ami a kréta szervereivel való kapcsolatfelvételt és adatmozgást kezeli.

* **Notificator modul** *preview*

Ez egy segéd modul ami időszakosan ellenőrzi a felhasználók állapotát, és ennek megfelelően értesítést küld a regisztrált klienseknek.



## Kapcsolat

Ha észrevételed van a platformal kapcsolatban nyugottan vedd fel a kapcsolatot velünk a weboldalon megadott módok egyikével.

Ha hibát találsz akkor légyszives ezt a még nem létező Github oldalon jelezd hogy biztos javításra kerüljön.