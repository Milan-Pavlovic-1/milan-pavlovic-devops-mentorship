# DevOps Mentorship Program - Milan Pavlovic



## Week 2
Koraci i komande koristene prilikom izrada taska:


```bash
$ ssh user@host -p 2200 # komanda za spajanje na server koristenjem porta 2200, ime usera i host kome pristupamo
# moze se navesti i ip adresa hosta umjesto dns hosta
$ ls # komanda za ispis sazdrzaja odnosno fajlova i foldera unutar foldera
$ ls -la # komanda slicna prethodnoj, ali koja mimo vidljivih fajlova i foldera ispisuje i one sakrivene sa predznakom .
$ cd # promjena direktorijuma
$ cat # ispis sadrzaja fajla
$ cat ./-name_of_the_file # morali smo dati punu putanju zbog - ispred imena fajla
$ exit ili logout # komanda da se izadje sa servera ili u slucaju da smo root user da odemo na "normal" usera
$ file ./file* # file je komanda koja nam omogucava da vidimo tip fajla
# fajl moze biti human-readable (eg. "ASCII text") or MIME type (e.g "text/plain; charset=us-ascii")
# mi trazimo human readably fajl te stoga trazimo fajl ispred kojeg pise "ASCII TEXT"
# drugi dio komande znaci samo da unutar trenutnog direktorijuma trazimo sve fajlove koji pocinju sa "file" i posle toga imaju random karaktere
# svrha wildcarda odnosno "*" jeste da zameni bilo koji karater
$ cat "spaces in this filename" ili cd "spaces in this folder"$ 
# unutar navodnika kada stavimo ime je nacin da ciljamo imena folera ili fajlova koji imaju space(razmak) u imenu
$ cat spaces\ in\ this\ filename/ ili cd spaces\ in\ this\ folder/  # isto postizemo kao sa prethodnom komandom
$ | # ova komanda se naziva "pipe", a zadatak joj je da rezultat lijeve komande prepuštamo dalje u komandu desno 
$ sort data.txt | uniq -u # prva komanda nam sortira fajl, sve linije koje se ponavljaju ce biti jedna ispod druge
# koristimo pipe da taj output gurnemo u komandu uniq
# komanda uniq -u otklanja sve linije koje su se ponovile vise od 1
$ grep # pretrazujemo fajl ili fajlove koji sadrzavaju zeljeni string
# postoji vise opcija filtriranja, kao sto je -F trazimo pojam u fajlu, -v trazimo suprotno od tog pojma
$ 2>dev/null # skrivanje svih mogucih errora, (e.g access denied)
$ strings # pretrazujemo human-readable string unutar binarnog fajla
$ find # komanda koja sluzi za pronalazenje fajlova i direktorijuma rekruzivno odnosno kroz folder te njegove subfoldere
# postoji vise opcija kako se ova komanda koristi
# mozemo filtrirati pretragu po human-readable fajlovima, executable, velicini fajla, imenu fajla itd.
# e.g find . type -f -readable -size 1033c ! -executable
$ base64 # komanda za sifrovanje i desifrovanje fajlova. Za dekodiranje koristimo parametar -d.
```