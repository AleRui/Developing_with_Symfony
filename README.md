## Desarrollando con Symfony
### Desarrollo de Software usando el framwwork PHP: Symfony

#### 0. Preparación para trabajar con Symfony:

1. Instalar **Xamp** (Entorno de Desarrollo: Apache + MariaDB + PHP + Perl)
	Windows - IOS - Linux: https://www.apachefriends.org/es/download.html

2. Instalar **Composer**: https://getcomposer.org/
"Librería que gestiona las dependencias de los proyectos PHP"
Linux / Unix / OSX: Comandos en: https://getcomposer.org/download/
Windows:
    1 - Descargar instalador y ejecutar.
    2 - Buscar carpeta de xamp donde está php y seleccionar: php.exe
    3 - Comprobar instalación: Abrir Consola y ejecutar: "composer".

3. Instalar Symfony por consola (by Composer): https://symfony.com/download
    1 - Ir a la rut (Path): "C:\xampp\htdocs\Symfony"
    2 - Escribir comando: _(La versión usada es la 2.8)_
	~~~
	composer create-project symfony/framework-standard-edition my_project_name "2.8.*
	~~~
    - Database? "press enter" (por defecto)
	- Database Port? "press enter" (por defecto)
	- Database Name? "Puesto por el usuario" ("nombre_del_proyecto")
	- Root? "press enter" (por defecto)
	- Password? "press enter" (por defecto)
	- smtp? "press enter" (por defecto)
	- mailer host? "press enter" (por defecto)
	- mailer usar? "press enter" (por defecto)
	- mailer password? "press enter" (por defecto)
	- Token? "press enter" (por defecto)

#### 1. Empezando con Symfony: Crear un Bundle ("paquete" o plugin)
1. Crear un bundle por consola:
	~~~
	php app/console generate:bundle
	~~~
	- Varias aplicaciones? "press enter" (por defecto no)
	- Nombre: version\nombreBundle
	- Nombre corto: nombrecortoBundle
	- Estructuras de Directorio: "press enter" (por defecto)
	- Formato de Configuración Rutas: YML

Recomendación: Vaciar la cache: php app/console cache:clear --env=prod --no-debug


Help:
http://symfony.com/doc/2.4/book/index.html

Spanish
http://librosweb.es/libro/composer/
https://librosweb.es/libro/symfony_2_x/

GtiHub Symfony:
https://github.com/symfony
Gestionar Proyecto con GitHub: http://symfony.com/doc/2.3/cookbook/workflow/new_project_git.html
