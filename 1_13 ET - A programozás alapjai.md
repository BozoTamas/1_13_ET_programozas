# A programozás alapjai segédanyag
## Tartalomjegyzék
1. [Bevezetés](#introduction)
2. [A programozás alapjai](#basics)

    2.1 [Változók](#variables)
    
    2.2 [Operátorok](#operators)

    2.3 [Elágazások: if-else](#if-else)

    2.4 [Összetett feltételek](#expressions)

    2.5 [Ciklusok](#cycles)

    * 2.5.1 [While](#while)
    * 2.5.2 [For](#for)
    * 2.5.3 [Do-while](#do-while)


    
***
### 1. Bevezetés<a name = "bevezetés"></a>
A segédanyagban az eddig tanultak találhatóak meg, minden egyes héten az anyag kibővítésre kerül az órákon elhangzottakkal, valamint a hozzá tartozó példákkal.

Az anyagot kizárólag felkészüléshez lehet használni bármilyen kérdés van elérnek a **bozo.tamas.daniel@gmail.com** e-mail címen, vagy a személyes Facebook-omon **facebook.com/bozotamasdaniel**.
***
### 2. A programozás alapjai<a name = "basics"></a>
Az órán két lehetőség van programozási feladat elvégzésére:

1. Online programozó felület használata. (pl.: www.w3schools.com)
2. Integrált Fejlesztői környezet használata. (pl.: _Visual Studio_)

Ebben az anyagban a példák _Visual Studio_-ban vannak írva.

***
### **Változók**<a name = "variables"></a>

Mielőtt nekikezdenénk a programok írásának meg kell ismerkednünk a program legalapvetőbb egységével, ami nem más mint a változó.

A változók a programban azokat az adatokat tárolják, melyekre szükségünk van. A változókat elképzelhetjük egy dobozként. Bele tudunk rakni dolgokat és amikor szükségünk van rá, ki tudjuk venni belőle.

Egy változónak 3 fő része van:

1. Típus
2. Név
3. Érték

A változó típusa határozza meg azt, hogy a memóriában mekkora helyet foglal, illetve azt is, hogy milyen adatot tudunk tárolni benne.

A változó neve egy hivatkozás lesz, melynek segítségével a programból el tudjuk érni azt a nevesített memóriaterületet, melyen a változó adatot tárol.

A változó értéke az általa tárolt adat lesz.

Nézzünk egy példát változóra: `int szám1 = 15;`. Ebben az esetben a változónk típusa az **int**, azaz egész számot fogunk tárolni benne. A változónk neve **szám1**, a későbbiekben ezt felhasználva tudunk hivatkozni a számra. Értéke pedig **15**.

Természetesen nem csak egész számokat tudunk tárolni egy programban. Nézzünk néhány példát a valtozók típusaira, és arra, hogy ezek milyen értéket tárolnak.
| Típus  | Tárolt érték                | Példa    | Deklaráció                    |
| ------ | --------------------------- | -------- | ----------------------------- |
| int    | Előjeles egész szám         | 15 / -15 | `int a = 15;` / `int a = -15` |
| uint   | Előjel nélküli egész szám   | 15       | `uint a = 15;`                |
| float  | 6-9 karakterből álló tört   | 15.154f  | `float a = 15.154f;`          |
| double | 15-17 karakterből álló tört | 15.154   | `double a = 15.154;`          |
| char   | Egyetlen karakter           | 'a'      | `char a = 'a';`               |
| string | Karakterlánc / Szöveg       | "alma"   | `string a = "alma";`          |

Ezek a típusok lesznek azok, melyek az év során használni fogunk.
***
### **Operátorok**<a name = "operators"></a>
A programozásban operátorokat használunk arra, hogy változókkal/értékekkel műveleteket végezzünk. Egy művelet elvégzéséhez a következőkre van szükség:
> - legalább egy operandus
> - legalább egy operátor

Az operandusok lehetnek változó hivatkozások, vagy konkrét értékek, amikkel dolgozni szeretnénk. <br>
Az operátor az a művelet, melyet az operandusokon el szeretnénk végezni.

Pl.: 12 + 23;<br>
Ebben a példában az operandusaink a 12 és a 23 konkrét értékek és ezeken a összeadást szeretnénk elvégezni, melyet a '+' operátor jelez.

Lehetőség van egy operandusú művelet elvégzésére is, ezek olyan speciális esetek, amikor az operandusunk értékét növelni, vagy csökkenteni szeretnénk 1-el.

Pl.: Legyen adott egy `szam` nevű változónk, melynek értékét szeretnénk változtani.<br> Ha ezt az értéket növelni szeretnénk 1-el, akkor a ***szam++;***, ha csökkenteni, akkor pedig a ***szam--;*** parancsot kell használnunk.

Nézzük meg a C# nyelvben leggyakrabban használt operátorokat.<br>A példa során az operandusok `szam1` és `szam2`.
| Operátor | Elvégzett művelet          | Használat        | Példa (eredménnyel) |
| :--------: | :-------------------------- | :---------------- | :------------------- |
| `=`      | Értékadás                  | `szam1 = 10;`    | 10                  |
| `+`      | Összeadás                  | `szam1 + szam2;` | 10 + 20 -> 30       |
| `-`      | Kivonás                    | `szam1 - szam2;` | 10 - 5 -> 5         |
| `*`      | Szorzás                    | `szam1 * szam2;` | 10 * 2 -> 20        |
| `/`      | Osztás                     | `szam1 / szam2;` | 10 / 2 -> 5         |
| `++`     | Érték növelése 1-el        | `szam1++;`       | 10 -> 11            |
| `--`     | Érték csökkentése 1-el     | `szam1--;`       | 10 -> 9             |
| `+=`     | Aktuális érték növelése    | `szam1 += 10;`   | 10 -> 20            |
| `-=`     | Aktuális érték csökkentése | `szam1 -= 10;`   | 20 -> 10            |
| `*=`     | Aktuális érték szorzása    | `szam1 *= 2;`    | 10 -> 20            |
| `/=`     | Aktuális érték osztása     | `szam1 /= 2;`    | 20 -> 10            |
| `%`      | Maradékos osztás           | `szam1 % 2`      | 10 -> 0             |

Amennyiben több operandust használunk, a matematikai művelet végzési sorrend itt is teljesül.<br>Pl.: 10+(20-10)*2/2 = 20, mert (20-10) = 10 , 10 * 2 = 20 , 20 / 2 = 10 ,<br> 10 + 10 = 20.
***
### **Elágazások: if-else if**<a name = "if-else"></a>

A programozásban az elágazások a vezérlési szerkezetek azon részét képzik, melyek lényege, hogy egy feltétel alapján a program több féle módon futhat le. A legegyszerűbb elágazás az `if-else` szerkezet, melyet a következőképpen hozunk létre:
```csharp
    if(feltétel) //a feltétel vagy IGAZ vagy HAMIS lehet
    {
        //futtatandó kód, ha a feltétel IGAZ
    }
    else //akkor fog lefutni, ha a feltétel HAMIS
    {
        //futtatandó kód
    }
```
Amennyiben összetetteb vizsgálatot szeretnénk végezni hasnálhatunk if-else if-...-else szerkezetet, ahol tetszőleges számú feltételünk van, melyeket mindig az _'if'_ után fogunk írni, például:
```csharp
    if(feltétel1){ ... }
    else if(feltétel2){ ... }
    else if(feltétel3){ ... }
    ...
    else { ... }
```
Az ilyen módon megírt elágazások lényege, hogy egymás után több feltételt is meg tudunk vizsgálni és az a kódrészlet fog lefutni, amelyre szükségünk van.
***
Nézzünk egy egszerű példát az előzőekre.

```csharp
    int szam1 = 10; //létrehozunk egy 'int' típusú, 'szam1' nevű változó, melynek értéke 10
    int szam2 = 20; //létrehozunk egy 'int' típusú, 'szam2' nevű változó, melynek értéke 20

    //Vizsgáljuk meg, hogy a két szám közül melyik lesz a nagyobb.
    if(szam1 > szam2) //Amennyiben a szam1 értéke nagyobb, mint a szam2-é
    {
        Console.WriteLine("Az első szám a nagyobb");
    }
    else
    {
        Console.WriteLine("A második szám a nagyobb");
    }
```
Az előző kód első ránézésre teljesen rendben van, azonban van egy hiba benne.

Mi történik akkor, ha a két szám egyenlő? -- A válasz: A program az 'else'-ben lévő kódot fogja lefuttatni, azaz kiírja a képernyőre, hogy a szam2 a nagyobb, holott ez nem igaz.

Ahhoz, hogy ezt kijavítsuk a következőképpen kell a kódot átírni:
```csharp
    int szam1 = 10; /*létrehozunk egy 'int' típusú, 'szam1' nevű
    változó, melynek értéke 10*/
    int szam2 = 20; /*létrehozunk egy 'int' típusú, 'szam2' nevű
    változó, melynek értéke 20*/

    //Vizsgáljuk meg, hogy a két szám közül melyik lesz a nagyobb.
    if(szam1 > szam2) //Amennyiben a szam1 értéke nagyobb, mint a szam2-é
    {
        Console.WriteLine("Az első szám a nagyobb");
    }
    else if(szam1 < szam2)
    {
        Console.WriteLine("A második szám a nagyobb");
    }
    else
    {
        Console.WriteLine("A két szám egyenlő");
    }
```
Így a program már hibátlanul fog működni, valamint minden egyes lehetőséget le fogunk fedni, ugyanis két szám közül vagy az egyik nagyobb, vagy a másik, vagy a két szám egyenlő.
***

### ***Összetett feltételek***<a name = 'expressions'></a>
Az elágazások használatakor nem csak egy feltételünk lehet, hanem 2,3,...,n db. Ezeket valamilyen logikai kapcsolóval tudjuk egymáshoz kapcsolni és így egy nagy feltételt fogunk kapni, melyet a programunk kiértékel és ennek megfelelően fut le.<br>Logikai kapcsoló az ÉS (`&&`) és a VAGY(`||`). Ezek használatakor a következő szabályokra kell figyelni:
> - Két vagy több ÉS-el összekapcsolt feltétel eredménye akkor IGAZ, ha a feltételek mindegyike IGAZ
> - Két vagy több VAGY-al összekapcsolt feltétel eredménye akkor IGAZ, ha a feltételek közül legalább az egyik IGAZ

Az előzőeket úgynevezett 'igazságtábla' segítségével tudjuk ábrázolni. A feltételek legyenek **`A`**, **`B`** és **`C`**. 
|   A   |   B   |   C   | A && B | A II B | A && C | A&&B&&C | A II B II C |
| :---: | :---: | :---: | :----: | :----: | :----: | :-----: | :---------: |
|   0   |   0   |   0   |   0    |   0    |   0    |    0    |      0      |
|   0   |   0   |   1   |   0    |   0    |   0    |    0    |      1      |
|   0   |   1   |   0   |   0    |   1    |   0    |    0    |      1      |
|   0   |   1   |   1   |   0    |   1    |   0    |    0    |      1      |
|   1   |   0   |   0   |   0    |   1    |   0    |    0    |      1      |
|   1   |   0   |   1   |   0    |   1    |   1    |    0    |      1      |
|   1   |   1   |   0   |   1    |   1    |   0    |    0    |      1      |
|   1   |   1   |   1   |   1    |   1    |   1    |    1    |      1      |
***
### **A ciklusok alapjai** <a name = 'cycles'></a>
Az év során 3 ciklussal fogunk megismerkedni, ezek a `for`, a `while` és a `do-while`.<br> Ezt a három ciklust két kategóriába tudjuk sorolni, elöl-, illetve hátultesztelős. Minden ciklus addig fog futni, amíg egy megadott feltétel teljesül (hasonlóan az elágazásokhoz, melyek akkor futnak le, ha teljesül a feltétel), azonban ennek a feltételnek a vizsgálata történhet a ciklusmag lefutása előtt, vagy után is.<br>Egy ciklus magján azt a kódrészletet értjük, amely a feltétel teljesülásekor le fog futni. A ciklusmagban általában vagy ugyanaz a kód fut le újra és újra, vagy egy olyan kód, melyben minimális különbség van.<br>Például írhatunk olyan ciklust, mely egymás után kiírja 10-szer az 1-es számot (ekkor ugyanaz a kód fut le 10-szer), vagy egy olyan ciklust, amely 1-től 10-ig írja ki a számokat (ekkor a kódban minimális különbség van csak, mégpedig az, hogy aktuálisan melyik szám kerül kiírásra).

Az elöl- és hátultesztelős ciklusok közötti különbség, hogy az elöltesztelős ciklusoknál (**while, for**) a feltétel vizsgálata a ciklusmag lefutása előtt történik meg, ezért amennyiben a feltétel az első vizsgálat alkalmával HAMIS, a ciklusmag nem fog egyszer sem lefutni.

Ezzel szemben a hátultesztelős ciklusnál (**do-while**) a feltétel vizsgálata a ciklusmag lefutása után történik meg, ezért a ciklusmag legalább egyszer le fog futni, még akkor is, ha az első vizsgálatnál a feltétel HAMIS lesz.
***
#### ***Ciklusok: while***<a name = 'while'></a>
A while ciklus egy elöltesztelős ciklus, melynek feltétele egy IGAZ vagy egy HAMIS értéket fog visszaadni, ami meghatározza, hogy a ciklusmag lefut-e vagy sem.

Kódban ez a következőképpen néz ki:
```csharp
    while(<feltétel>)
    {
        //ciklusmag (akkor fut le, ha a feltétel igaz)
    }
```
Mivel a feltétel vizsgálata a ciklusmag lefutása előtt történik meg, előfordulhat olyan eset, hogy a ciklusmag egyszer sem fog lefutni.
***
#### ***Ciklusok: for***<a name = 'for'></a>

A 'for' ciklus feltétele egy intervallumot fog meghatározni egy ciklusváltozó segítségével, azaz valamettől-valameddig fut. Amikor deklarálunk egy 'for' ciklust létrehozzuk a ciklusváltozót (ez lesz a kezdőpont, azaz ettől fog futni a ciklus), valamint meghatározzuk azt is, hogy a ciklusváltozó maximális értéke mi lesz (ez lesz a végpont, azaz eddig fog futni a ciklus).

Kódban ez a következőképpen néz ki:
```csharp
    for(int i = 0; i < 10; i++)
    {
        //ciklusmag (akkor fut le, ha a feltétel igaz)
    }
    //Ez a ciklus 10-szer fut le, méghozzá 0-tól 9-ig
```
A ciklusváltozó deklarálása: `int i = 0;`

A végpont meghatározása: `i < 10;` (ez a ciklusunk feltétele)

A ciklus létrehozásakor az `i++` felel azért, hogy a ciklusunk léptetésre kerüljön, így a ciklusváltozó el fogja érni előbb-utóbb a végpontot.

Ha nem "`<`"-et használunk, hanem "`<=`"-t azzal azt fogjuk elérni, hogy a ciklusváltozónk legmagasabb értéke megegyezik a végponttal. Az előző példát ez úgy változtatná meg, hogy a ciklus 0-tól 10-ig futna.

Nézzünk meg két egyszerű példakódot a 'for' ciklusra, az egyik 10-szer fogja kiírni az 1-es számot, a másik pedig 1-től 10-ig fogja kiírni a számokat.
```csharp
for(int i = 0; i < 10, i++)
{
    Console.WriteLine(1); /*Minden alkalommal, amikor lefut a ciklus
    kiírjuk az 1-es számot. Mivel 10-szer fog lefutni a ciklus
    (0-tól 9-ig), ezért 10-szer írjuk ki.*/
}

for(int i = 1; i <= 10; i++)
{
     Console.WriteLine(i); /*Minden alkalommal, amikor lefut a
     ciklus az 'i' étékét írjuk ki. Ez az érték 1-től 10-ig minden
     alkalommal amikor lefut a ciklus 1-el fog nőni.*/
}
```
***
#### ***Ciklusok: do-while***<a name = 'do-while'></a>
A do-while ciklus egy hátultesztelős ciklus, azaz a ciklusmagja legalább egyszer le fog futni, mivel a feltétel a ciklusmag után kerül vizsgálatra.

A do-while ciklus létrehozása:
```csharp
    do
    {
        //ciklusmag (legalább egyszer lefut)
    }while(<feltétel>);
```
A következőkben néhány egyszerű ciklusra nézünk példát, magyarázattal együtt.

```csharp
    while(true)
    {
        Console.WriteLine("Hello!");
        /*Ez egy úgynevezett végtelen ciklus, mivel a
        feltétele midig az IGAZ értéket adja vissza.
        Az ilyen ciklusoknak a futása akkor áll meg,
        ha a programot leállítjuk, vagy valamilyen 
        esetben használjuk a "break;" utasítást.*/
    }
    ----------------------------------------------------------------
    int a = 10;
    do
    {
        Console.WriteLine(a);
        a++;
    }while(a <= 20);
    /*Ez a ciklus 10-től 20-ig fogja kiírni a számokat
    egyesével. Amikor a 20 kiírásra került az 'a'
    változó értékét növeljük 21-re, majd megvizsgáljuk a feltételt.
    Mivel a 21 <= 20 feltétel értéke HAMIS lesz, ezért a ciklusmag
    már nem fog mégegyszer lefutni.*/
    ----------------------------------------------------------------
    for(int i = 1; i > -10; i--)
    {
        Console.WriteLine(i);
    }
    /*Az előző 'for' ciklus példával ellentétben itt nem növeljük
    a ciklusváltozó értékét, hanem csökkentjük. Ezt az 'i--'
    operátor segítségével tudjuk elérni.*/