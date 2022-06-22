# Oma- ja laensõnade kasutuse võrdlemine
Siin repositooriumis on digihumanitaaria projekti raames koostatud kood oma- ja laensõnade kasutuse võrdlemiseks. Uurimise all on sõnad, millel on eesti omasõna ja vastav samatähenduslik vene, saksa ja/või inglise laen. Kood otsib Digari ajakirjandustekstidest tekste, kus otsitavaid sõnu on mainitud, salvestab nee failidena ja koostab nende failide tulemusel oma- ja laensõnade kasutussageduse võrdlemiseks graafikud ja tabelid<br>

Failis laensonad_kood.ipnyb on kood Jupyter Notebooki kujul, mida saab kasutada Jupyteri keskkonnas.<br>

# Juhised koodi kasutamiseks:
Laadige alla laensonad_kood.ipynb ja avage see Jupyteri keskkonnas.
## Failide tegemise blokis:
Searchterm on see sõna, mida tahad otsida.
<br>
Searchfile all saad panna sellele failile nime, kuhu tulemus salvestatakse
<br>
subset_ek on korpuse kõik eestikeelsed tekstid, kust sõna hakatakse otsima
<br>
Lemmatiseeritud tekstide jaoks on see 'searchtype="lemmas"
<br>
Lisage failinimesse, mis keelest ta on (eesti, vene, saksa või inglise), nt kampsun_eesti.txt, pullover_inglise.txt, sviiter_vene.txt
<br>
### NB! Kõigile otsingusõnadele lisada ette ja taha \\\b nagu allpool kujutatud. 
Nii välistatakse juhud, et otsides sõna 'kamp' leitakse ka 'kampsun'

## Failide lisamine kaustadesse:
Et kood töötaks, on vaja teha kõigepealt üks suur kaust, nt 'koik_keeled'. Seejärel saab lisada sinna alamkaustu. Ühes alamkaustas on ühe mõiste kohta käivad sõnad, mille failinimes peab avalduma, mis tüüpi sõnaga on tegu (kas eesti omasõna, saksa, vene või inglise laen, nt 'jumestus_eesti.txt', 'grimm_vene.txt', 'meik_inglise.txt', 'mink_saksa.txt'). Alamkausta nimi, kus need failid on, võiks kajastada kõiki neid sõnu (nt 'jumestus_meik_grimm_mink'), sest kausta nimi muudetakse hiljem graafiku pealkirjaks.
<br>
### NB! Mõelge täpselt, kuhu tahate tulemusi salvestada. Minul näeb failipuu välja selline:
-kodu <br>
---- koik_keeled (siin on kood) <br>
-------- graafikud <br>
-------- tabelid <br>
------------ normitud <br>
------------ tavalised <br>
-------- tekstid <br>
------------ jumestus_meik_grimm_mink <br>
------------------ jumestus_eesti.txt <br>
------------------ grimm_vene.txt <br>
------------------ meik_inglise.txt <br>
------------------ mink_saksa.txt <br>
<br>
Kui teil on samasugune failipuu, siis pole vaja koodis midagi muuta. Kui te aga tahaks midagi teisiti teha, otsi koodist sõna 'path' ja leiate kõik kohad, kus seda muuta saad. See keskkond arvestab koduks selle koha, kus kood on, nii et kui tahta nt, et fail salvestatakse kohta "kodu/koik_keeled/graafikud", peab kirjutama pathiks ainult "graafikud". 
