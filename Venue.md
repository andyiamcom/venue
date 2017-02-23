1. Regamine

1. Kasutajad-huvid: Kõik kasutajad. Tahavad ennast süsteemis registreerida. 

2. Primaarne kasutaja (kui on):

3. Üleüldine kirjeldus: Läbi facebooki, google’i, linkedin API’i VÕI registeerib manuaalselt. Selleks on alustuseks vaja emaili. Sisestatakse landing page’l.

4. Infovaade (kus toimub protsess): 

    1. sign up view (punkt 13.2) 

    2. sealt edasi spetsiaalsed vaated täiendava info küsimiseks.

5. Käivitav sündmus: subjekt soovib registreerida

6. Eeltingimused: kasutajal on olemas isiklik email VÕI sotsiaalmeedia konto

7. Järeltingimused: kasutaja on registeeritud, avatakse library vaade.

8. Erinõudmised: 

9. UX-UI tips:

10. UML,mockupid

11. Näited: 

    3. slack.com

    4. [https://blog.hubspot.com/marketing/landing-page-examples-list#sm.00018tqvatadsfkeynp27kz3a2wol](https://blog.hubspot.com/marketing/landing-page-examples-list#sm.00018tqvatadsfkeynp27kz3a2wol)

12. Kasutusjuhu esinemissagedus*:* igapäevaselt

13. Stsenaarium:

    5. Subjekt soovib ennast registeerida landing page’il, vajutades "sign up" nupule.

    6. Süsteem pakub valikut, kas registeerida API’de kaudu või emaili kaudu. (sign up view)

    7. Kasutaja valib emaili teel regamise, sisestades emaili.

    8. Systeem kontrollib, et email poleks eelnevalt võetud. (võimalik, et vaja lisada funktsioon, mis kontrollib, et kasutaja poleks robot).

        1. Kui email on olemas, siis systeem annab teate, et kasutaja on antud emailiga on juba olemas.

    9. Kasutajale saadetakse süsteemi poolt geneeritud 6-kohaline kood emailile.

    10. Süsteem palub sisestada kasutajale saadetud 6-kohaline kood.

    11. Süsteem kontrollib koodi korrektsust.

        2. Kui sisestatud kood on vale, kuvatakse süsteemi poolt teade, et sisestatud kood on vale ja kasutajat ei registeerita.

    12. Järgmisel vormil palutakse sisestada eesnimi, perekonnanimi ja password. Check box võiks olla selleks (by default täidetud), et kasutaja soovib saada infot ridline’i tegemiste kohta.

        3. Password peab olema min 6 kohaline.

        4. Passwordi keerukust kontrollitakse. Selleks annab süsteem tagasisidet 4-kohalisel skaalal.

![image alt text](image_0.png)

    13. Järgmisel vormil süsteem küsib kasutajalt tema peamise rolli kohta (Main role (sound engineer, organizer, artist, venue owner, other). Kasutaja saab antud skippida vajadusel.

    14. Järgmisel formil küsitakse kasutaja eesnime ja perenime (vaja, et kasutajat teistele kasutajatele arusaadavalt display’ida).  Kasutaja saab antud skippida vajadusel.

    15. Süsteem registeerib kasutaja. Süsteem logib kasutaja sisse library vaatesse. Süsteem kuvab teate edukast registreerimisest (modal). 

14. Laiendused (API kaudu registeerimine):

    16. Kasutaja valib API kaudu registeerimise.

    17. Süsteem liidestab kasutaja valitud API’ga (OP.1.4)

    18. Kasutaja sisestab API’le oma kasutajanime, parooli

    19. Süsteem ootab positiivset vastet API kaudu regisreerimisel.

        5. Kui volitus on positiivne JA antud kasutaja pole eelnevalt kasutanud registeerimisel teist API’t, siis jätkatakse punktis 13.9.

        6. Kui volitus on negatiivne, kuvatakse teade, et ei suudetud kasutajat tuvastada ja registeerimine ebaõnnestus.

        7. Kui antud kasutaja on registeeritud teise kasutaja API’ga, siis kuvatakse teade, et kasutaja on juba registeeritud. 

            1. Kasutaja logitakse tema olemasolevasse kontosse library vaatesse.

15. Märkused:

    20.  kastutaja saab alati protsessi pooleli jätta. Selleks igas vaates cancel võimalus.

    21. Kasutaja jääb sisse logituks pärast rakendust väljumist (nt. brauseri akna sulgemisel). Teatud aja pärast rakendatakse automaatne väljalogimine (kasutusjuht "automatic logout")

16. Lahtised probleemid/testimiskohad:

    22. Kuidas kõige vähem kasutajat sisestusandmetega koormata?

    23. Kuidas teha registreerimisprotsessi kiiremaks?

    24. Kas on olemas vigade haldus (nt timeout API’dest jne)?

    25. Passwordi keerukuse kontroll

    26. Kuidas küsida kasutajalt tema peamise rolli kohta?

    27. Kuidas vältida topeltkontosid, kui kasutaja registeerib mitmekordselt erinevate apidega (millele lisaks võib tal olla email:pass meetod)?

    28. Kas captcha lisamine oleks vajalik?

    29. Kuidas vältida, et inimene registeerib erinevate apidega mitu korda?

## 2. Märkused regamise kohta, mida üleval polnud

* Regamine saab alguse ridline.com’st

* Kasutajad, kes määravad enda rolliks muu kui venue (pt. 13.9), viiakse staatilisele lehele sisuga "Under the progress" vms. Miks? Sellepärast, et kui süsteem saab avatuks venudele ja nad saavad hakata sisestama oma andmeid, siis teistel kasutajatüüpidel ei ole 100% töötavaid funktsionaalsusi. Poolikuid asju vist pole mõtet näidata? Variant on ka, et teised rollid praegu üldse välja jätta ja ainult venue jätta.

* Venue kasutajad suunatakse "venue" vaatesse pärast edukat regamist (vt. allpool edasi).

3. Kui kasutajad

* Kasutaja ehk venue esindaja läheb ridline.com lehele ning saab registreerida ennast kasutajaks.

* Venue kasutaja peab olema teistest kasutajatest, mida registreeritakse eraldatav, sest venue registreerijale kuvatakse hoopiski teistsugune infoväli kui sound engineerile vms

Ehk siis kasutaja valib kohe alugses, et registreerib kui venue? või mõni muu nipp?

* Kasutaja saab lisada oma andmed: asukoht, kontaktid (kelle poole pöörduda kontserdikorraldusega jms), nimetus  - vajadusel ka firma nimi. Mis võib veel vajalik olla infona lisada?

* Kasutaja ehk venue saab vaate, milles on tal tabel, kuhu saab lisada kõik vajaliku tehnika, mis on tal kohapeal olemas. 

    * Ta saab ka lisada, kas ese korrast ära või kasutatav. Samuti kas ese on rendiks väljas või mitte

    * Venue saab üles laadida enda CAD vms joonised

    * Venue saab lisada soovi korral mõned fotod oma lavast jms

* Infot saab jagada sellel kujul, mis me oleme juba kokku leppinud - PDF jms

### Venue listi loomine/muutmine

1. Kasutaja registreerib (rolliga venue)

2. Kasutaja logib sisse

3. Kasutaja moodustab uue venue raideri

    1. Selleks läheb ta "your profile" - > “venue” vaatesse 

    2. "Venue" vaade koosneb osadest:

        1. Üldosa: nimetus, asukoht, kontakt

        2. Fotod: lavast, majast, asukohast (võimalus uploadida)

        3. Tech list:

Näitetabel:

<table>
  <tr>
    <td>Sound technical specs</td>
    <td>Nimetus</td>
    <td>Kogus</td>
    <td>Kasutavad</td>
    <td>Rendiks</td>
  </tr>
  <tr>
    <td>PA</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td></td>
    <td>JBL Soundpower T771 high-mid speaker (flown)</td>
    <td>4 tk</td>
    <td>Jah</td>
    <td>Ei</td>
  </tr>
  <tr>
    <td>Monitors</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>FOH</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Microphones</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>DI boxes, cables, stands</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Light technical specs</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Back-truss lights</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Fx-lights</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Front-truss lights</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Control</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
</table>


NB! Siin kehtivad samad sisestamisviisid nagu raideri tabelis. NT. saab tab’iga liikuda.

1. "Iga elementi saab valida dropdown’ist, millele toeks input field, mis aitab tulemusi filteerida. Kasutaja sisestada ka vabas vormis (st. veergudes nagu “kogus, kasutatavad, rendiks) on vaikimisi väärtuseks vastavalt number, boolean, boolean, kuid vajadusel saab sinna lisada oma muu väärtuse.

2. Ükski veerg pole kohustuslik.

3. Tabelis olevaid ridu saab liigutada ülesalla üksida ja koos teiste ridadega. -  Juhul kui liigutan ühte eset, siis teised peavad sellega koos kaasa liikuma (näiteks saan valida kolm eset ja neid korraga liigutada). NB! Kui koos ridasid liigutada, siis saab liigutada ainult  järjestikku olevaid ridasid. 

4. Tabelisse saab lisada juurde ka uusi veerge. On olemas teatud standardveerud (kogus, kasutatavad, rendiks) koos vastavate andmetüüpidega.

5. saan tab’iga edasi liikuda, Enteriga uut rida tekitada. Juhul kui olen rea lõpus ja vajutab tab tekitatakse mulle uus rida uuesti juurde. Ei pea kasutama hiir, et tabelit täita!

6. Kogu protsessi jooksul toimub automaatne salvestamine. Küll aga on olemas undo võimalus. Kasutajaliideses selleks vastav funktsioon.

## USECASE: Venue andmete seostamine projektigaUSECASE: Venue listi jagamine

