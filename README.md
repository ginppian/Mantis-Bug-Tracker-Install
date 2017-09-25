Mantis Bug Tracker
=======

<p align="center">
	<img src="https://github.com/ginppian/Mantis-Bug-Tracker-Install/blob/master/imgs/img1.png" width="682" height="350">
</p>

## Descripción

<p align="justify">
	<a href="https://www.mantisbt.org/">Mantis Bug Tracker</a> es un sistema de gestión de incidencias gratuito y libre. Nos sirve para llevar un control completo de cada proyecto y mantener el historial de cada incidencia en el tiempo; es además, la mejor manera de verificar en cualquier momento el estado de nuestras solicitudes.
</p>

## Requisitos para este Tutorial

* <a href="https://www.apachefriends.org/es/index.html">XAMPP</a>

## Instalación

<p align="justify">
	1. Descargamos <i>Mantis</i> desde <a href="https://www.mantisbt.org/download.php">aquí</a>.
</p>

<p align="justify">
	2. Una vez descargado lo descomprimimos y arrastramos la carpeta a <i>C:\xampp\htdocs</i>.
</p>

 
<p align="justify">
	Nota: Si estamos en nuestro servidor Apache (<a href="https://github.com/ginppian/Traccar4">tuto</a>) lo descargamos así:
</p>

```
cd ~
wget https://sourceforge.net/projects/mantisbt/files/latest/download.php
unzip download
mv mantisbt-2.6.0 mantisbt
sudo mv mantisbt /var/www/html
```

<p align="justify">
	3. Configuramos la instalación:
</p>

<p align="center">
	<img src="https://github.com/ginppian/Mantis-Bug-Tracker-Install/blob/master/imgs/img3.png" width="682" height="350">
</p>

<p align="justify">, 
	Es muy simple, seleccionamos el tipo de BD que usamos, el hostname que por defecto es <i>localhost</i>. En mi experiencia:
</p>

```
Username (for Database)
Admin Username (to create Database if required)
```

<p align="justify">
	Usan el mismo usuario y contraseña, que en mi caso es, user: <i>root</i> y pass: (sin contraseña). Ahora precionamos el boton *Install/Upgrade Database*.
</p>

<p align="center">
	<img src="https://github.com/ginppian/Mantis-Bug-Tracker-Install/blob/master/imgs/img2.png" width="682" height="350">
</p>

<p align="justify">
	Veremos varios mensajes de <i>GOOD</i>, hasta abajo precionamos *continue* para ir a la página de login.
</p>

<p align="center">
	<img src="https://github.com/ginppian/Mantis-Bug-Tracker-Install/blob/master/imgs/img4.png" width="682" height="350">
</p>

<p align="justify">
	El usuaro es: <b>administrator</b> y la clave es <b>root</b>
</p>

<p align="justify">
	Lo siguiente es configurar el idioma, desabilitar que nos notifique por correo para pedirnos una nueva confirmación cuando creamos un nuevo usuario, configurar el idioma, y la zona horaria. Todo eso lo editamos en el archivo: <b>mantisbt/config/config_inc.php</b>. Se vería algo así:
</p>

```
<?php
$g_hostname               = 'localhost';
$g_db_type                = 'mysqli';
$g_database_name          = 'bugtracker';
$g_db_username            = 'root';
$g_db_password            = 'mypass';

$g_crypto_master_salt     = 'PCKCJ5SIEU5pcUAZWlV79aYY1FOGkVulem/btIjI1AQ=';

$g_default_timezone       = 'America/Mexico_City';
$g_default_language = 'spanish';
$g_enable_email_notification = OFF;

```

<p align="justify">
	4. Ahora tenemos que borrar la carpeta <b>Admin</b> para que nadie más vuelva a hacer la configuración que acabamos de hacer.
</p>

<p align="justify">
	5. Entramos a <i>Mantis</i> con el usuario administrator, en la parte superior derecha nos vamos a mi cuenta, en el panel ponemos nuestra contraseña actual *root* y ponemos nuestra nueva contraseña.
</p>

<p align="justify">
	Nota: Si en nuestro servidor no se crea el archivo <i>config_inc.php</i> por que necesitamos permisos podemos crearlo nos otros y copiar el código de arriba y funcionará perfectamente.
</p>


<p align="justify">
	Ahora sólo queda *Invitar usuarios*, <i>Crear un proyecto</i> y llevar nuestros bugs. 
</p>

## Fuentes

* <a href="http://www.programandoconcafe.com/2012/06/mantis-instalacion-del-mantis.html">MANTIS - INSTALACIÓN DEL MANTIS</a>





