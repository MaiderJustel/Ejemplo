A important Gen 
-----------


-----------

INTRODUCCION

La anhidrasa carbónica es una enzima muy importante para el proceso de calcificación en organismos marinos. Todos los corales al realizar la calcificación requieren de esta proteina. Por ello se ha tomado la base de datos de Pocillopora Base y se ha realizado BLAST con la anhidrasa carbónica 1 y 2 de Acropora millepora.
![Foto](http://www.melevsreef.com/pics/06/03/baby_blue_morphed.jpg)


Para hacerlo seguimos estos pasos.

**1. Primero vamos a descargar la base de datos de Pocillopora Base. La guardamos en Desktop/Bigdata/Blast/db/FASTA**

**db = base de datos**

El link de Pocillopora es :

< http://cnidarians.bu.edu/PocilloporaBase/cgi-bin/index.cgi>

#..........JUPYTER..............

!makeblastdb \

-dbtype nucl \

-in Desktop/Bigdata/Blast/db/FASTA de Pocillopora Base

-out Desktop/Bigdata/Blast/db/coral.db                  
#...................................



**2. Ahora vamos a descargar un gen de interese del Gen Bank. La guardamos en DesDesktop/Bigdata/Blast/query
3 Ahora vamos a hacer BLAST en la base de datos creada y el gen que hemos descargado para ello:**



#..............JUPYTER..............

!blastn \

-query Desktop/Bigdata/Blast/query/FASTA del gen

-db Desktop/Bigdata/Blast/db/FASTA de Pocillopora Base

-task blastn \

-outfmt 6 \

-out Desktop/Bigdata/Blast/coral.fastanew
#.....................................


**3. Ahora vamos a llamar a al nuevo archivo que hemos creado**



..............JUPYTER................

!head  Desktop/Bigdata/Blast/coral.fastanew

me va a salir una tabla

gi 333333313      f7yieuendnd

......................................



**5. Ahora vamos a ver la secuencia de un conting. Como por ejemplo de f7yieuendnd.**



#................JUPYTER...............

!grep -w -A 100 "f7yieuendnd" \

Desktop/Bigdata/Blast/db/FASTA de Pocillopora Base (la base de datos que nos descargamos de la web)

#.......................................


**6. Ahora nos saldra una secuencia del contig. la copiamos y la llevamos a la pagina de NCBI en BLAST y vemos con que nos coincide.**

Este es el link de la pagina


