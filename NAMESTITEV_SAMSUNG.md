# Medicofit PROM – Samsung Galaxy Tab A11+

Ta projekt je pripravljen kot **popolnoma offline Android aplikacija**.

## Delovanje
- vseh 27 vprašalnikov je vgrajenih v APK;
- aplikacija nima INTERNET dovoljenja;
- rezultati se hranijo samo lokalno na tablici;
- terapevt izbere vprašalnik in vnese pacienta;
- **Pacient način** skrije terapevtske rezultate, zgodovino in scoring;
- vrnitev v terapevtski način zahteva PIN;
- privzeti PIN je **2468** in ga je možno spremeniti v aplikaciji;
- CSV/JSON izvoz se shrani v `Prenosi/Medicofit PROM`;
- JSON backup je možno ponovno uvoziti;
- tisk/PDF uporablja Androidov sistemski print dialog;
- aplikacija med izpolnjevanjem ohrani zaslon prižgan.

## Namestitev APK na Samsung
Ko je APK zgrajen:
1. Kopirajte `app-debug.apk` na tablico.
2. Odprite ga v **Moje datoteke / My Files**.
3. Če Android vpraša, dovolite aplikaciji *Moje datoteke* namestitev neznanih aplikacij.
4. Potrdite **Namesti**.
5. Po namestitvi lahko to dovoljenje ponovno izklopite.

## Gradnja v Android Studio
1. Odprite celotno mapo projekta v Android Studio.
2. Počakajte, da se Gradle sinhronizira.
3. Izberite `Build > Build APK(s)`.
4. APK bo v `app/build/outputs/apk/debug/app-debug.apk`.

## Gradnja prek GitHub Actions
Projekt že vsebuje `.github/workflows/build-apk.yml`.
Če mapo objavite v GitHub repozitorij, workflow sam zgradi APK in ga ponudi kot artifact `Medicofit-PROM-APK`.

## Zasebnost
Lokalna hramba zmanjša prenos podatkov, vendar gre še vedno za zdravstvene podatke. Tablica naj bo zaščitena z zaklepanjem zaslona, šifriranjem naprave in omejenim dostopom. Pred servisom, zamenjavo ali odstranitvijo aplikacije naredite backup, saj odstranitev aplikacije izbriše lokalne podatke.


## v1.2
Po namestitvi posodobljene APK se aplikacija prikaže kot »Digitalni standardizirani vprašalniki«. Vključuje dropdown terapevtov in serijsko reševanje več vprašalnikov.


## Posodobitev na v1.3 brez izgube arhiva
Novo APK datoteko namestite ČEZ obstoječo aplikacijo in izberite Posodobi.
Aplikacije pred tem NE odstranite in ne izberite "Počisti podatke", sicer Android izbriše lokalni arhiv.
Pred večjo posodobitvijo priporočamo JSON varnostno kopijo.


## POMEMBNO: enkratni prehod na stabilno podpisano v1.3
Pred namestitvijo v1.3 v stari aplikaciji izberite **Varnostna kopija** in shranite JSON datoteko.
Poskusite nato namestiti novo APK kot posodobitev.

Če Android javi, da aplikacije ni mogoče posodobiti zaradi podpisa/paketa:
1. preverite, da imate JSON backup;
2. odstranite staro Medicofit PROM aplikacijo;
3. namestite v1.3;
4. v aplikaciji izberite **Uvozi** in izberite JSON backup.

Od v1.3 naprej je v projektu stabilen podpisni ključ, zato naslednjih verzij ne bo treba odstranjevati; namestite jih čez obstoječo aplikacijo.
