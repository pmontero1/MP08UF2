# Instal·lació Owncloud



1. Hem de instalar apache:


![alt text](1ouncloud.png)


2. Desactivem el llistat de directoris del servidor:

![alt text](2ouncloud.png)


3. Hem de instalar MariaDB


![alt text](3ouncloud.png)


I configurem la instal·lació:
   
Aquí és interessant:

* Deshabilitar usuaris anònims.
* Desactivar accés remot com a root.
* Eliminar les bases de dades de testeig i accedir-hi.
* Actualitzar les taules de privilegis.


![alt text](4ouncloud.png)



![alt text](5ouncloud.png)



![alt text](6ouncloud.png)


![alt text](7ouncloud.png)



Finalment reiniciem el servidor MariaDB.

![alt text](8ouncloud.png)




Crear la base de dades d'owncloud:

Entrem a MariaDB:


![alt text](9ouncloud.png)



Creem un usuari anomenat ownclouduser amb una contrasenya que podria ser Admin1234.

![alt text](10ouncloud.png)



li donem accés a l'usuari a la base de dades creada:

![alt text](11ouncloud.png)


Apliquem els canvis i sortim:


![alt text](12ouncloud.png)

Instal·lar PHP i els seus mòduls necessaris:

![alt text](13ouncloud.png)





![alt text](14ouncloud.png)


Hem de tenir en compte els requisits d'Owncloud abans d'instal·lar els mòduls.





![alt text](15ouncloud.png)

Després de la instal·lació editem el fitxer php.ini i canviarem alguns valors:

![alt text](116ouncloud.png)

![alt text](12.2ouncloud.png)




Instal·lem Owncloud:



![alt text](17ouncloud.png)



Canviem propietari i permisos dels directoris d'owncloud. www-data perquè els pugui fer servir Apache, 755 perquè els pugui executar i llegir qualsevol usuari de Linux:


![alt text](18ouncloud.png)


Configurar Apache:


![alt text](19ouncloud.png)



Hem de deixar un fitxer com el següent, però canviant el ServerName i el ServerAlias ​​pels noms i àlies del nostre propi domini.



![alt text](19.2ouncloud.png)



Habilitem owncloud i el mòdul rewrite:



![alt text](20ouncloud.png)


Reiniciem Apache:



![alt text](21ouncloud.png)







** Explicació de les linies del fitxer Owmcloud.conf:


![alt text](owncloudLinies.jpg)



1r adresa web del admin 2 on volem que aparegui la gent que entra al servei 3 Nom del servidor
