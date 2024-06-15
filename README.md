# Online-shop

## Tech Stack

### Backend

ASP.NET + mongo.db

### Frontend

Nue.js


### specification
Online shop 
1. Opis zadatka
Realizovati aplikaciju za online kupovinu.
Postoje 2 vrste korisnika ovog sistema:
1. Prodavac
2. Kupac
2. Funkcije sistema
2.1. Prikazinformacija neregistrovanim korisnicima
Prva stranica koju (neregistrovan) korisnik vidi je pocetna ̌ stranica aplikacije na kojoj je moguće ili
ulogovati se (već registrovani) na sistem ili preći na stranicu za registraciju.
2.2. Registracija korisnika i prijavljivanje na sistem
Na stranici za registraciju pomoću korisnikove email adrese i lozinke moze se ̌ izvrsiti ̌ prijava.
Ukoliko korisnik jošuvek nije registrovan na sistem, a zeli da koristi funkcije aplikacije, mora prvo da se ̌
registruje na odgovarajućoj stranici. Registracija je moguća na dva nacina. Prvi je takozvana klasi ̌ cnǎ
registracija - unosom licnih podataka koji obuhvataju: ̌ email adresu, lozinku, ime, prezime, datuma
rođenja i adresu. Lozinka se unosi u dva polja da bi se otezalo pravljenje gre ̌ saka prilikom odabira nove ̌
lozinke. Nakon registracije administrator treba da potvrdi registraciju. I drugi naciň – putem neke
drustvene ̌ mreze. ̌ Implementirati oba pristupa (Jedna drustvena ̌ mrezǎ je dovoljna).
Prilikom registracije potrebno je definisati:
• Korisnickǒ ime
• Email
• Lozinku
• Ime i prezime
• Datum rođenja
• Adresa
• Tip korisnika – Prodavac ili Kupac
• Sliku korisnika - Omogućiti upload slike;
Potrebno je obezbediti mehanizam za autentifikaciju i autorizaciju korisnika na serverskoj strani.
2.3. Profil korisnika
Registrovani korisnik je u mogućnosti da azurira ̌ svoje licně podatke na stranici za prikazsvog profila.
2.5. Dashboard
Nakon uspesnog ̌ logovanja korisnik je redirektovan na stranicu Dashboard-a . Na njoj se nalaze
sledeći elementi, koji će biti detaljno opisani u narednim poglavljima:
● Profil (svi)
● Dodavanje artikla (Prodavac)
● Nova porudzbina ̌ (Kupac)
● Prethodne porudzbine ̌ (Kupac)
● Nove Porudzbine ̌ (Prodavac)
● Sve porudzbine ̌ (Prodavac)
2.5.1. Profil
Prikazi izmena profila korisnika.
2.5.2. Dodavanje artikla
Prodavac mozě da dodaje nove artikle, menja ili brisě postojeće artikle. Artikal treba da ima:
 naziv,
 cenu,
 kolicinu, ̌
 opisi
 fotografiju.
2.5.3. Nova porudžbina
Kreiranje nove porudzbine se vr ̌ si izborom opcije ̌ „Porucǐ“ koja, pored informacija o artiklu omogućuje
unos kolicine, komentara i adrese dostave. Proizvode doda ̌ je prodavac. Korisnik moze poru ̌ citi jedan ili ̌
visě proizvoda u okviru porudzbine (ukoliko ima ̌ na stanju). Cena se racuna ̌ po tome stǎ porucuje ̌ i kolicini ̌
plus cena dostave koja je uvek ista. Kupac, nakon kreiranja porudzbine dobija informaciju o ̌ vremenu
dostave.
Napomena: Vreme dostave je nasumicaň izbor vremena (>1h). Nakon toga porudzbina ̌ prelazi u
prethodne porudzbine. ̌ Kupac mozě otkazati porudzbinu ̌ sat vremena nakon vremena porucivanja ̌ (u tom
slucaju ̌ vratiti kolicinu ̌ na prethodno stanje).
2.5.4. Prethodne porudžbine
Kupac mozě da vidi listu svojih prethodnih porudzbina. ̌ Ne prikazuju se otkazane porudzbine. ̌
2.5.5. Nove porudžbine
Prodavac vidi spisak novih porudzbina, ̌ prikazuje se i vreme dostave ISTO kao i kupcu koji ceka ̌ tu dostavu.
2.5.6. Sve porudžbine
Prodavac ima uvid u sve porudzbine kao i njihov status. Za porud ̌ zbine u toku nije potrebno ̌
odbrojavanje do dostave.
3. Tech stack
.NET CORE
Mongo db
C#-back
 Nue.js-front
3.2 Konkurentni pristup resursima
Vazno je da vi ̌ se ̌ istovremenih korisnika aplikacije, ne moze da radi nad istim elementom u istom ̌
vremenskom periodu. Pored navedenog ogranicenja, svaki student treba da pronađe jo ̌ špo jednu
konfliktnu situaciju za svoj deo zahteva i adekvatno je resi.̌
Napomena: Nije dovoljno zasititi ̌ klijent, potrebno je isto to uraditi sa serverom! Dakle probati
postmanom/swaggerom na primer da li je moguće obrisati/modifikovati entitet koji ne postoji.
Rukovati izuzecima na prednjoj i zadnjoj strani. Napraviti model na prednjoj strani, tako da ukoliko se
izmeni model na zadnjoj strani, je dovoljno da se izmena uradi samo na jednom mestu na prednjoj
strani.
Napomena: mora se koristiti Git za kontrolu verzija i repozitorijum mora biti na GitHubu dostupan
predavacima ̌ na uvid prilikom izrade i odbrane projekta.
3.3 Arhitektura resenja ̌ i kriterijumi ocenjivanja
U projektu se moraju ispostovati ̌ kriterijumi kvaliteta resenja ̌ i dobre prakse u izradi web aplikacija
pokazane na vezbama. ̌
1. Prednja strana aplikacije mora biti podeljena po komponentama
2. URL-ovi eksternih servisa koji se gađaju sa prednje strane moraju biti u .env fajlu i isčitavati ̌
se odatle, ovo ukljucuje i ̌ URL zadnje strane aplikacije.
3. HTTP pozivi sa prednje strane moraju biti u servisima koji se injektuju u komponente,
nikako direktno u komponentama.
4. Moraju postojati modeli na prednjoj strani
5. Na zadnjoj strani aplikacije baza podataka mora biti konfigurisana preko Fluent API,
ne anotacijama.
6. Zadnja strana mora biti troslojna web aplikacija, uz korisćenje ̌ injekcije zavisnosti.
7. Moraju postojati Dto i modeli baze podataka kao odvojeni modeli i mora postojati adekvatno
mapiranje između njih.
8. Mora biti ispostovana ̌ REST konvencija za nazivanje resursa.
https://restfulapi.net/resource- naming/
9. Lozinke u bazi podataka moraju biti hesirane ̌
10. Potpis i istek tokena moraju biti validirani
11. Konfigurabilne podatke (lozinke eksternih servisa, URL-ove) na zadnjoj strani
drzati ̌ u appsettings.json fajlu i ucitavati. ̌

