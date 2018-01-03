## Desarrollando con Symfony
### Desarrollo de Software usando el framwwork PHP: Symfony

#### 0. Preparación para trabajar con Symfony:



<table>
	<tr>
		<td>
			<div
				<a href="https://www.apachefriends.org/es/index.html" target="_blank">
					<img src="https://d16zszyyqlzz6z.cloudfront.net/images/xampp-logo-ac950edf.svg" width="150">
					<br><p>Xamp</p>
				</a>
			</div>
		</td>
		<td>
			<div>
				1. Instalar <b>Xamp</b> (Entorno de Desarrollo: Apache + MariaDB + PHP + Perl)<br>
				Windows - IOS - Linux: https://www.apachefriends.org/es/download.html
    	</div>
    </td>
	</tr>
	<tr>
		<td>
			<div
				<a href="https://getcomposer.org/" target="_blank">
					<img src="https://getcomposer.org/img/logo-composer-transparent2.png" width="150">
					<br><p>Composer</p>
				</a>
			</div>
		</td>
		<td>
			<div>
				2. Instalar <b>Composer</b>: https://getcomposer.org/<br>
				<i>"Librería que gestiona las dependencias de los proyectos PHP"</i><br>
				Linux / Unix / OSX: Comandos en: https://getcomposer.org/download/<br>
					<ul>Windows:
					    <li>1 - Descargar instalador y ejecutar.</li>
					    <li>2 - Buscar carpeta de xamp donde está php y seleccionar: php.exe</li>
					    <li>3 - Comprobar instalación: Abrir Consola y ejecutar: "composer".</li>
					</ul>
    	</div>
    </td>
	</tr>
</table>

3. Instalar Symfony por consola (by Composer): https://symfony.com/download  

    1 - Ir a la ruta en la consola (Path): "C:\xampp\htdocs\"

    2 - Escribir comando:_(La versión usada es la 2.8)_  

	~~~
	composer create-project symfony/framework-standard-edition my_project_name "2.8.*
	~~~
  
~~~
Database?: "press enter" (por defecto)
Database Port?: "press enter" (por defecto)
Database Name?: "Puesto por el usuario" ("nombre_del_proyecto")
Root?: "press enter" (por defecto)
Password?: "press enter" (por defecto)
smtp?: "press enter" (por defecto)
mailer host?: "press enter" (por defecto)
mailer usar?: "press enter" (por defecto)
mailer password?: "press enter" (por defecto)
Token? "press enter": (por defecto)
~~~

#### 1. Empezando con Symfony: Crear un Bundle ("paquete" o plugin)
1. Crear un bundle por consola:  
~~~
php app/console generate:bundle
~~~

~~~
Varias aplicaciones? "press enter" (por defecto no)
Nombre: version\nombreBundle (indicaremos la versión de nuestra App)
Nombre corto: nombrecortoBundle (indicaremos un nombre corto para llamar a la App)
Estructuras de Directorio: "press enter" (por defecto)
Formato de Configuración Rutas: YML
~~~

Recomendación: Vaciar la cache después de la instalación
~~~
php app/console cache:clear --env=prod --no-debug
~~~

#### 2. Estructura de Directorios (taxonomía de un Bundle)

+ **app/**: contiene la configuración de la aplicación.
    + app/config: Está toda la configuración básica de la App (se cambiará si se hace migración).
    + app/Resources/views: Guardaremos las plantillas twig de las diferentes vistas.
+ **bin/**: ayuda con el Debugging.
+ **src/**: aquí se encuentra todo el código PHP de la aplicación (aquí es donde más trabajaremos).
    + src\versionX.X\nombreBundle\/**Controller**: Aquí estará todo la acción de nuestro software, los controladores.
    + src\versionX.X\nombreBundle\/**Entity**: Aquí estarán nuestras entidades (tablas de la BD).
    + src\versionX.X\nombreBundle\/**Form**: Aquí estarán la base de nuestros formularios relacionados con las entidades.
    + src\versionX.X\nombreBundle\/**Repository**: Aquí estaran los repositorios relacionados con las entidades.
    + src\versionX.X\nombreBundle\Resources\/**config**: Aquí estará la configuración de las rutas de las vistas y los controladores, al igual que la configuración de las entidades.
    + src\versionX.X\nombreBundle\Resources\/**views**: Aquí estarán las diferentes vistas (páginas web).
+ **test/**: contiene una muestra.
+ **vendor/**: por convención aquí se guardan todas las librerías creadas por terceros.
+ **web/**: este es el directorio web raíz y contiene todos los archivos que se pueden acceder públicamente.
    + web\public: aquí alojaremos los diferentes elementos CSS y Javascript


Help:  

https://symfony.com/doc/current/index.html


Spanish:  

http://librosweb.es/libro/composer/
https://librosweb.es/libro/symfony_2_x/

GtiHub Symfony:  

https://github.com/symfony  

Gestionar Proyecto con GitHub:  

http://symfony.com/doc/2.3/cookbook/workflow/new_project_git.html
