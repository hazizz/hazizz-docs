# Belépés és regisztrálás menete

## Motiváció
A projekt a fiókkezelés problémás részeit (értsd: elfelejtettem a jelszavam) delegálja az általunk használt fiók szolgáltatókra, mint például a Facebook és Googlere. Ezt úgy érjük el hogy a fiók létrehozásához szükséges az egyik általunk választott szolgáltatónál egy már létező fiók használata. Ez a megközelítés lehetővé teszi hogy a felhasználóknak soha ne kelljen elfelejtett jelszavakkal bajlódnia a mi rendszerünkön keresztül, és ha mégis ilyen természetű problémájuk lenne akkor a lehető legmagasabb élményben legyen részük egy nagy szolgáltatónál.

## Bejelentkezés
A bejelentkezés a következő módszerekkel lehetséges:

### Natív bejelentkezés felhasználónév és jelszó használatával

Ez az opció azután válik elérhetővé, hogy a felhasználó hozzárendelt egy jelszót a fiókjához.

**Ezen bejelentkezési módot nem ajánljuk a kliensek létrehozásánál**.

### Refresh token

Ha már a felhasználó egyszer belépett, akkor a megszerzett refresh token használatával újra be lehet lépni.

### Google OpenID
A bejelentkezéshez egy Google OpenID Tokent használunk aminek a helyességét a [Google API Client](https://developers.google.com/identity/sign-in/web/backend-auth#using-a-google-api-client-library) library ellenőrzi.

Következő konfigurációval ellenőrizzük: 
#### Issuers:
- https://accounts.google.com
- accounts.google.com
 
#### ClientIds:
- 425675787763-flqjv0n2nlcublglnonf795oul80feeg.apps.googleusercontent.com
- 425675787763-751dukg0oookea8tltaeboudlg0g555q.apps.googleusercontent.com

### Facebook Login
Ennek működési elve hogy a küldött tokent ellenőrzi a [Facebook Graph](https://graph.facebook.com/v4.0/) használatával, és lekérdezi az email címét.

#### FIGYELEM
Ez nem működik ha a facebook fiókhoz nincs hozzárendelve egy email cím.

## Regisztráció

### Menete
Azt ajánljuk az implementációnál, hogy a felhasználó csak belépési gombokat lásson, és ha a szerver úgy reagál hogy a felhasználó még nem regisztrált, akkor koncenzus ellenében tegyük meg ezt a lépést.

Minden regisztrálásnál el kell fogadtatni a felhasználóval az általános szerződést és adatkezelést. ITT GERI

### Technika 
Regisztrálni Google OpenID-val és Facebookal lehet a bejelentkezéssel megegyező módon.