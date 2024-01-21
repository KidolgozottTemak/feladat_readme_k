# Express.js + MySQL

1. Töltsük le a gépünkre a **Node.js** legutolsó stabil változatát a saját [Node.js](https://nodejs.org/en) oldalról.
   ![1. kép](./images/express_mysql/kep_001.png)
2. Hozzunk létre egy mappát **express_mysql** néven a hasonló nevű **GitHub repository**-ból. Nyissuk meg a **Visual Studio Code** segítségével. Nézzük meg a telepített **Node.js** verziószámát a **Git Bash** felületen. A verziószám legalább 18.18.0 legyen!
   ![2. kép](./images/express_mysql/kep_002.png)
3. Adjuk ki a következő utasítást, amellyel létrehozzuk a szükséges környezetet a gépünkön a szerveroldali alkalmazáshoz (**API**).
   `npm init -y`
   ![3. kép](./images/express_mysql/kep_003.png)
4. Telepítsük fel a szükséges **npm** csomagokat.
   `npm install dotenv ejs express mysql2`
   ![4. kép](./images/express_mysql/kep_004.png)
5. Szerkesszük a kapott **package.json** állományt. A **package-lock.json** állományhoz és a **node_modules** mappához ne nyúljunk, csak ha tudjuk mit csinálunk!
   ![5. kép](./images/express_mysql/kep_005.png)
6. Hozzuk létre a **public** és **views** mappákat, valamint a **.env**, **.gitignore** és **server.js** állományokat.
   ![6. kép](./images/express_mysql/kep_006.png)
7. Lépjünk be a **public** mappába és ott hozzuk létre a **css**, **images** és **js** mappákat. Ezután a **css** könyvtárba lépve alkossuk meg a **stilus.css** állományt. Majd menjünk vissza az alapmappába!
   ![7. kép](./images/express_mysql/kep_007.png)
8. Szerkesszük a **.env** és **.gitignore** állományokat.
   ![8. kép](./images/express_mysql/kep_008.png)
9. **server.js** kezdeti beállítása.
   ![9. kép](./images/express_mysql/kep_009.png)
10. Índítsuk el a szervert és nézzük az eredményét a böngészőben. Ehhez egyidejű lenyomás a **Git Bash** felületén.
    `ctrl + http://localhost:3500`
    ![10. kép](./images/express_mysql/kep_010.png)
11. Hozzunk létre **autok** néven egy **MySQL** adatbázist a **localhost phpmyadmin** felületén. Majd építsük ki az összeköttetést az adatbázis és a szerver között. Ehhez alkossunk meg egy **database.js** állományt az alapmappában és szerkesszük.
    ![11. kép](./images/express_mysql/kep_011.png)
12. Most a **server.js** állomány továbbfejlesztése következik.
    ![12. kép](./images/express_mysql/kep_012.png)
13. Lépjünk be a **views** mappába és hozzuk létre az **index.ejs**, az **egyedi.ejs** és a **feltolt.ejs** állományokat. Majd menjünk vissza az alapmappába!
    ![13. kép](./images/express_mysql/kep_013.png)
14. Szerkesszük az **index.ejs** állományt.
    ![14. kép](./images/express_mysql/kep_014.png)
15. Lehetséges **css** beállítások a **stilus.css** állományban.
    ![15. kép](./images/express_mysql/kep_015.png)
16. Eddig itt tartunk.
    ![16. kép](./images/express_mysql/kep_016.png)
17. Hozzuk létre az új autók feltöltésére alkalmas oldalt, azaz szerkesszük a **feltolt.ejs** oldalt.
    ![17. kép](./images/express_mysql/kep_017.png)
18. Látható, hogy az űrlap adatok kezeléséhez szükségünk lesz egy **autokezeles.js** javascript állományra a **public** mappa **js** almappájában. Hozzuk létre és szerkesszük.
    ![18. kép](./images/express_mysql/kep_018.png)
19. Mindezek működéséhez a **server.js** állományt is módosítani kell.
    ![19. kép](./images/express_mysql/kep_019.png)
20. Most foglalkozzunk az **egyedi.ejs** állománnyal. Ezt arra használjuk, hogy a listából kiválasztott autót külön oldalon be tudjuk mutatni. Ehhez először ismét a **server.js**-t kell módosítani.
    ![20. kép](./images/express_mysql/kep_020.png)
21. Nézzük mi került az **egyedi.ejs** állományba.
    ![21. kép](./images/express_mysql/kep_021.png)
22. Képileg így néz ki.
    ![22. kép](./images/express_mysql/kep_022.png)
23. Állítsuk be először a törlési funkciót. Ez törli az adatbázisból az adott autót, ha a **Töröl** gombra (valójában link) kattintunk. Ehhez ismét a **server.js** állományban kell dolgoznunk.
    ![23. kép](./images/express_mysql/kep_023.png)
24. Most próbáljuk meg módosítani a kijelölt elemet. Ehhez szükségünk lesz egy **modosit.ejs** állományra a **views** mappában.
    ![24. kép](./images/express_mysql/kep_024.png)
25. Látható, hogy egy **modosit()** függvényt kell létrehoznunk az **autokezeles.js** állományban. Nézzük.
    ![25. kép](./images/express_mysql/kep_025.png)
26. De, hogy mindez működjön, módosítani kell a **server.js** állományt is. Újra.
    ![26. kép](./images/express_mysql/kep_026.png)
27. Végül próbálkozzunk meg az autók márka szerinti szűrésével. Ehhez helyezzünk el a weboldalon egy legördülő lista elemet. Nézzük a hozzá tartozó kódrészletet az **index.ejs** állományban. Megjelent egy **if**-es kifejezés is, ami meg fogja jeleníteni az adott autótípus márkáját.
    ![27. kép](./images/express_mysql/kep_027.png)
28. A **szures()** függvény elég egyszerű.
    ![28. kép](./images/express_mysql/kep_028.png)
29. És végül a sokadjára átdolgozott **server.js**. Itt a **root-route**-ot dolgoztuk teljesen át.
    ![29. kép](./images/express_mysql/kep_029.png)

# Adatbázis

1. Az adatbázis felépítéséhez.
   ![30. kép](./images/express_mysql/kep_030.png)
2. Értékek. A képeket a **public/images** mappába helyezzük el.
   ![31. kép](./images/express_mysql/kep_031.png)

# Továbbfejlesztések

## Rendezés ár szerint.

1. Ha ár szerint szeretnénk rendezni az oldalunkat, akár márkára történt szűrés után is, akkor az **index.ejs** módosításával kell kezdenünk.
   ![32. kép](./images/express_mysql/kep_032.png)
2. A szükséges **novel()** és **csokken()** függvényeket az **autokezeles.js** állományban dolgozzuk ki.
   ![33. kép](./images/express_mysql/kep_033.png)
3. Természetesen a **server.js** szerkesztése sem maradhat ki.
   ![34. kép](./images/express_mysql/kep_034.png)
4. És az eredmény az egyik márkára szűrés után.
   ![35. kép](./images/express_mysql/kep_035.png)

## views/partials mappa

1. Hozzunk létre egy **.prettierignore** nevű állományt, ahová azokat a mappákat, állományokat írjuk, amelyekre nem szeretnénk, ha hatna a **Prettier** extension.
   ![36. kép](./images/express_mysql/kep_036.png)
2. A **views** mappában hozzunk létre egy **partials** nevű mappát. Lépjünk be és szúrjunk be két állományt **header_01.ejs** és **header_01.ejs** néven. Ezekben fogjuk a későbbiekben szerkeszteni az **ejs** állományok fejrészét. Létre lehet még hozni egy közös **footer.ejs** állományt is, de ez nem kötelező.
   ![37. kép](./images/express_mysql/kep_037.png)
3. A **.prettierignore** állományba írjuk be a következő sort. Tehát letiltottuk a **Prettier** használatát ebben a mappában.
   ![38. kép](./images/express_mysql/kep_038.png)
4. Másoljuk át a **headers_01.ejs** állományba az **index.ejs** első néhány sorát.
   ![39. kép](./images/express_mysql/kep_039.png)
5. Tegyük meg ugyanezt az utolsó néhány sorával a **footer.ejs**-be.
   ![40. kép](./images/express_mysql/kep_040.png)
6. Szerkesszük az **index.ejs** állományt. Hasonlóan tegyünk a **feltolt.ejs** állománnyal.
   ![41. kép](./images/express_mysql/kep_041.png)
7. A **header_02.ejs** csak minimálisan különbözik a **header_01.ejs**-től, de viszont ott lényegesen. Ezt az **egyedi.ejs** és **modosit.ejs** állományokba kell berakni.
   ![42. kép](./images/express_mysql/kep_042.png)
8. Utolsó feladatként a **server.js** állományban, minden **render** metódusban helyezzünk el **title** tulajdonságot (property).
   ![43. kép](./images/express_mysql/kep_043.png)
