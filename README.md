# Oma- ja laensõnade kasutuse võrdlemine
Siin repositooriumis on digihumanitaaria projekti raames koostatud kood oma- ja laensõnade kasutuse võrdlemiseks. 
Failis laensonad.ipnyb on kood Jupyter Notebooki kujul, mida saab kasutada Jupyteri keskkonnas
Failis laensonad.Rmd on kood R markdowni kujul, mida saab kasutada RStudios.
Faili laensonad.html abil on kood ja selle väljundid vaadeldavad veebibrauseris.

# Juhised koodi kasutamiseks:
Laadige alla laensonad.ipynb ja avage see Jupyteri keskkonnas.
## Failide tegemise blokis:
Searchterm on see sõna, mida tahad otsida.
<br>
Searchfile all saad panna sellele failile nime, kuhu tulemus salvestatakse
<br>
subset_ek on korpuse kõik eestikeelsed tekstid, kust sõna hakatakse otsima
<br>
Lemmatiseeritud tekstide jaoks on see 'searchtype="lemmas"
<br>
### NB! Kõigile otsingusõnadele lisada ette ja taha \\\b.
Nii välistatakse juhud, et otsides sõna 'kamp' leitakse ka 'kampsun'

## Failide lisamine kaustadesse:
Et kood töötaks, oleks vaja failid kaustadesse lisada. Kõigepealt oleks vaja teha üks suur kaust, nt 'laensonad'. Seejärel saab lisada sinna alamkaustu. Ühes alamkaustas on ühe mõiste kohta käivad sõnad, mille failinimes peab avalduma, mis tüüpi sõnaga on tegu (kas omasona, eestindatud või voorsona, nt 'pagasnik_voorsona.txt', 'pagasiruum_eestindatud.txt', 'pakiruum_omasona.txt'). Alamkausta nimi, kus need failid on, võiks kajastada kõiki neid sõnu (nt 'pakiruum_pagasiruum_pagasnik), sest kausta nimi muudetakse hiljem graafiku pealkirjaks. 
<br>
### NB! Mõelge täpselt, kuhu tahate tulemusi salvestada. Minul näeb failipuu välja selline:
-kodu <br>
---- laensonad (siin on kood) <br>
-------- graafikud <br>
-------- tabelid <br>
------------ normitud <br>
------------ tavalised <br>
-------- tekstid <br>
------------ pakiruum_pagasiruum_pagasnik (siin on tekstifailid, mis nende otsingusõnade kohta said) <br><br>
Kui teil on samasugune failipuu, siis pole vaja koodis midagi muuta. Kui te aga tahaks midagi teisiti teha, otsige koodist sõna 'path' ja leiate kõik kohad, kus seda muuta saad. See keskkond arvestab koduks selle koha, kus kood on, nii et kui tahta nt, et fail salvestatakse kohta "kodu/laensonad/graafikud", peab kirjutama pathiks ainult "graafikud". 

