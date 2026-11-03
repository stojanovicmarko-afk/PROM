# Medicofit PROM v1.3

## Arhiv rešenih vprašalnikov
- Vsaka nova meritev shrani celoten vprašalnik, surove odgovore in "snapshot" besedila vprašanj/odgovorov.
- V arhivu je mogoče odpreti posamezno meritev in videti:
  - pacienta in ID,
  - datum,
  - terapevta,
  - prizadeto stran,
  - končni rezultat,
  - vse domene/podlestvice,
  - vsak odgovor na vsako vprašanje.
- Stare meritve ostanejo dostopne; če vsebujejo surove odgovore, aplikacija jih prikaže s trenutno definicijo vprašalnika.

## Filtri in razvrščanje
- iskanje po imenu, priimku ali ID pacienta,
- filter po terapevtu,
- filter po vprašalniku,
- razvrščanje:
  - datum najnovejši → najstarejši,
  - datum najstarejši → najnovejši,
  - pacient A → Ž,
  - pacient Ž → A,
  - terapevt A → Ž.

## Lokalna hramba
Podatki se še naprej shranjujejo lokalno v aplikaciji na tablici. Application ID in storage key ostajata enaka, zato posodobitev APK-ja čez obstoječo aplikacijo ohrani lokalni arhiv, če aplikacije pred tem ne odstranite ali ne počistite njenih podatkov.

## Backup
JSON backup vključuje celotne zapise. CSV izvoz v v1.3 vključuje tudi celotne odgovore.


## Stabilno podpisovanje APK
Od v1.3 projekt vsebuje namenski Medicofit podpisni ključ in tako bodo vse prihodnje APK verzije podpisane enako. To omogoča običajne Android posodobitve brez brisanja lokalnega arhiva.

### Enkratni prehod iz stare v1.2
Stare GitHub debug gradnje so bile lahko podpisane z drugim začasnim ključem. Če Android v1.3 ne dovoli namestiti kot posodobitev:
1. v v1.2 naredite JSON varnostno kopijo;
2. kopijo varno shranite;
3. odstranite staro aplikacijo;
4. namestite v1.3;
5. uvozite JSON backup.
Od v1.3 naprej naj se aplikacija NE odstranjuje med posodobitvami.
