Tartu Ülikooli bakalaureusetöö näidis
===

## Mis see on?

Tegemist on 2013. aastal Keemia Instituudis kaitstud bakalaureusetöö vormistusnäidisega.
Kui ma hakkasin tööd kirjutama, ei leidnud ma ühtegi terviklikku LaTeXis vormistatud lõputöö näidist ja pidin seetõttu otsast peale alustama.
Loodetavasti on tulevastel LaTeXi-huvilistel töökirjutamine/vormistamine veidi lihtsam.

## Kasutamine
Tööga on kaasas `Rakefile`, mis lihtsustab mõnevõrra kompileerimist.
Selle kasutamiseks peab olema paigaldatud Ruby ja `rake`.

    gem install rake

LaTeXi failide kompileerimiseks saad kasutada käsku `rake compile` ja 
töökataloogi puhastamiseks ajutistest failidest `rake clean`.
Tulemus on failis `thesis.pdf`.

## Struktuur

Põhifail on `thesis.tex`.
Tiitelleht ja kõik peatükid on eraldi failides.
Failid on võimaluste piires kommenteeritud.

## Litsents

Töö on avaldatud MITi litsentsi all.
Täpsemalt saab lugeda failist `LICENSE`.