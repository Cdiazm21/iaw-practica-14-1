# iaw-practica-14-1
Practica 14-1

Voy a hacer una especie de introduccion de que va la practica. Estamos creandonos una instancia en la que en esa misma instancia vamos a usar docker para poder usar los contenedores y poder tener en una misma maquina instalado mysql, wordpress, phpmyadmin y el certificado.
Esto se dividira en redes y volumenes.

Para explicar practica vamos a dividirla en varios pasos:

**Paso 1:**
Vamos a crearnos una instancia con terraform, a esta maquina le vamos a añadir el grupo de seguridad y una ip elastica(esto esta explicado en las anteriores practicas). 

Muestro el grupo de seguridad:

![](Fotos/4.PNG)

Muestro la creacion de la instancia y de la ip elastica:

![](Fotos/5.PNG)

**Paso 2**
Hay que instalarnos docker y docker compose, para esto vamos a utilizar ansible:

![](Fotos/6.PNG)

Ahora vamos a añadir los paquetes de python para docker y movemos el directorio a la instancia:

![](Fotos/7.PNG)

**Paso 3**

Ahora tenemos que crearnos los contenedores, los volumenes y las redes en nuestra instancia.
Para esto vamos a usar la pagina docker hub para usar las imagines oficiales de las que vamos a usar.
En nuestro caso nos pide la practica usar las imagenes de phpmyadmin, wordpress, mysql y https-service.

Para wordpress:

![](Fotos/8.PNG)

Para mysql:

![](Fotos/9.PNG)

Para phpmyadmin:

![](Fotos/10.PNG)

Para https-portal(este seria el certificado como certbot):

![](Fotos/11.PNG)

Ahora muestro los volumenes y las redes:

![](Fotos/12.PNG)

Recordatorio= Para poder ejecutar docker compose hay que instalarse en nuestra maquina:

![](Fotos/1.PNG)

Las variables usadas son:

![](Fotos/13.PNG)

**Paso 4** 

Hay que asignar a nuestra ip un dominio, en mi caso he usado la pagina de noip.com:

![](Fotos/15.PNG)

Esto hay que añadirlo en nuestro https-portal.

**Paso 5**

Comprobamos que funciona, para esto vamos a poner nuestro dominio en nuestro navegador:

![](Fotos/2.PNG)

Y seguimos los pasos hasta llegar a nuestro wordpress:

![](Fotos/3.PNG)