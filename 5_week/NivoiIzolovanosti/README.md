### Nivoi izolovanosti:

* make all da se svi fajlovi kompajliraju.
* unesemo rokove iz 2016. godine iz unos.sql fajla
* posle svakog primera pokrenuti i brisanje martovskog roka iz istog fajla

1. RR - za vreme koriscenja tog kursora ne moze ni insert ni update nad istom tabelom 

  u jednom terminalu pokrenemo ./repetableRead i tu se 2 puta ispisu svi rokovi 2016 <br/>
  u drugom ./testInsert i vidimo da se tek kad repetableRead zavrsi tj isklikcemo dovoljno puta izvrsi insert naredba
  
2. RS - za vreme koriscenja tog kursora moze insert al ne update nad istom tabelom 

  u jednom terminalu pokrenemo ./readStability i tu se 2 puta ispisu svi rokovi 2016 <br/>
  u drugom ./testInsert i vidimo da sad u sred izvrsavanja repRead mozemo izvrsiti insert i on ce procitati taj red <br/>
  u drugom ./testUpdate i vidimo da update nece moci da se izvrsi dok se ./readStability ne izvrsi

3. CS - za vreme koriscenja tog kursora mozemo i insert i update odraditi. 

  u jednom terminalu pokrenemo ./cursorStability i tu se 2 puta ispisu svi rokovi 2016 <br/>
  u drugom ./testInsert i vidimo da sad u sred izvrsavanja repRead mozemo izvrsiti insert i on ce procitati taj red <br/>
  u drugom ./testUpdatei i vidimo da sad u sred izvrsavanja repRead mozemo izvrsiti update