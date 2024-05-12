# Curso Git y GitHub [![Logo de la SCESI][logo-SCESI]][enlaceSCESI]
# Clase 1

## ¿Qué es un control de versiones?
Es un sistema para registrar cada cambio que se realiza en el código fuente de un proyecto. Basicamente permite un historial.

<p align="center">
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/VersionControl.jpeg" alt="Imagen Control de versiones" width="738">
</p>

## Importancia de un control de versiones
* **Seguimiento de cambios**, permitiendo un seguimiento y control, ademas que se podrian revertir errores.
* **Colaboracion eficiente**, facilita la colaboracion sobre todo en entornos de desarrollo intensos.
* **Seguridad**, siendo importante para garantizar la precisión e integridad de los archivos.
* **Flexibilidad** en el desarrollo.

## ¿Qué es Git?

<img src="https://cdn.iconscout.com/icon/free/png-256/free-social-285-116319.png" align="right"
     alt="Git Logo" width="110" height="110">

Es un sistema de control de versiones distribuido, aloja una copia completa del repositorio en nuestra maquina local para que posteriormente podamos subirlo a un repositorio remoto y podamos hacer trabajo colaborativo.

## ¿Qué es un repositorio?

<img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/estanteria-la-casa-el-salon-pintado-por-queyla-9921013.jpg" align="right"
     alt="Estanteria" width="150" height="150">

Es el pilar de los sistemas de control de versiones.

Es una especie de almacen para guardar los archivos con diferentes versiones, ademas de su historico, metaforicamente podriamos decir que es una estanteria de libros.

## Algunos otros sistemas de control de versiones
* **GitLab**
* **Bitbucket**
* **Mercurial**
* **Bazaar**

## Mas acerca de sistemas de control de versiones

**Abra las pestañas para ver mas información acerca del control de versiones.**

<details>
    <summary> Sistemas de control de versiones locales  :exclamation: :exclamation:  </summary>

  ### Sistemas de control de versiones locales
  Los sistemas de control de versiones locales son la forma más sencilla de tener un control de versiones y los utilizan principalmente los desarrolladores individuales en vez de los equipos. En un sistema de control de versiones local, todos los datos del proyecto se almacenan en una sola computadora y los cambios realizados en los archivos del proyecto se guardan localmente. 

<p align="center">
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/local.png" alt="Imagen control de versiones locales" width="538">
</p>

Una de las herramientas de control de versiones locales más populares fue un sistema llamado RCS, que todavía podemos encontrar en muchas de las computadoras actuales. Esta herramienta funciona guardando conjuntos de parches (es decir, las diferencias entre archivos) en un formato especial en disco, y es capaz de recrear cómo era un archivo en cualquier momento a partir de dichos parches.

Aunque los sistemas de control de versiones locales pueden ser útiles para los desarrolladores individuales, tienen limitaciones significativas cuando se trata de la colaboración en equipo. Por ejemplo, no permiten que varios desarrolladores trabajen en el mismo proyecto al mismo tiempo de manera eficiente. Además, dado que todos los datos se almacenan localmente, si la computadora del desarrollador falla, se puede perder todo el historial del proyecto
</details>    
<details>
    <summary> Sistemas de control de versiones centralizados  :exclamation: :exclamation:</summary>

### Sistemas de control de versiones centralizados
Los Sistemas de Control de Versiones Centralizados (CVCS) son un tipo de sistema de control de versiones donde hay un único “servidor” que contiene todas las versiones de los archivos. Este servidor centralizado almacena todos los archivos versionados, y varios “clientes” descargan los archivos desde ese lugar central.

En un CVCS, los clientes o desarrolladores se conectan al servidor principal para obtener el código fuente. Cualquier cambio o actualización del código fuente se almacena automáticamente en el repositorio central como una nueva versión. Los clientes pueden descargar la última versión del código desde el servidor central, realizar cambios en su copia local y luego subir (o “commit”) sus cambios al servidor central.

<p align="center">
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/centralized.png" alt="Imagen control de versiones centralizado" width="538">
</p>

Algunos ejemplos de CVCS son CVS, Subversion y Perforce.

Aunque los CVCS facilitan la colaboración y permiten un seguimiento fácil de quién hizo qué cambios, también tienen algunas desventajas. Por ejemplo, si el servidor central falla y no se han realizado copias de seguridad adecuadas, se podría perder todo el historial del proyecto. Además, los CVCS requieren conexión a la red para muchas operaciones, lo que puede ser una limitación en algunos casos.

</details>
<details>
    <summary> Sistemas de control de versiones distribuidos  :exclamation: :exclamation:  </summary>
  
### Sistemas de control de versiones distribuidos
Los Sistemas de Control de Versiones Distribuidos (DVCS) son un tipo de sistema de control de versiones donde cada desarrollador tiene su propio repositorio local con un historial completo de cambios. Esto significa que cada copia del código base es un repositorio completo.

En un DVCS, los desarrolladores pueden trabajar de forma aislada en su propia copia del código. Pueden hacer commits, crear ramas y cambiar entre ellas sin necesidad de una conexión a la red. Una vez que están listos para compartir sus cambios con otros, pueden “empujar” sus commits a un repositorio remoto.

Cuando varios desarrolladores han hecho cambios en diferentes copias del repositorio, estos cambios pueden ser fusionados. Los DVCS son muy buenos para manejar estas fusiones.

<p align="center">
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/distributed.png" alt="Imagen control de versiones distribuidos" width="538">
</p>

Un beneficio clave de los DVCS es que permiten la colaboración en línea y fuera de línea. También proporcionan una mayor seguridad, ya que cada desarrollador tiene una copia completa del historial del proyecto.
</details>

## Iniciando un proyecto en Git

Para crear un proyecto desde cero debemos seguir los siguientes pasos: 
* git init `<nombre de tu proyecto>`
* cd `<nombre de tu proyecto>`

En el caso que tu quisieras inicializar una carpeta ya existente entonces:
* cd `<directorio existente>`
* git init

## Los 3 estados de Git

<div align="center">

Estado       |Descripción|
|---------------|:--------------|
| Modified      |El archivo ha sido creado, eliminado o contiene cambios que no han sido marcados como confirmados.|
| Staged        |El archivo ha sido marcado como preparado para ser confirmado en el repositorio local.|
| Commited      |El archivo se encuentra grabado en el repositorio local. Esta acción recibe el nombre de commit|
</div>

## Cambiar el estado

Una vez que crees archivos o modifiques los que tengas te encontraras en el estado `Modified`, entonces deberas pasar al estado `Staged`, los pasos para hacerlo son:

* git status

Una vez que te ejecutes este comando deberia salirte algo como:

```yaml
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

```

Para este ejemplo llevaremos a `Staged` al archivo README.md

* git add `README.md`

Nuestro archivo esta listo para hacer el primer punto de guardado

* git commit

Se abrira una ventana en Visual Studio

```yaml
(en vez de este parentesis debes poner la descripcion de tu commit)
# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
#
# On branch main
#
# Your branch is up to date with 'origin/main'.
#
# Changes to be committed:
#       modified:   README.md
#
```
Guardas el archivo y lo cierras, despues de eso ya estaria hecho tu commit. Puedes revisar los commits con el comando:
* git log

## Pero... ¿Qué es un Commit?

Es una especie de punto de guardado, veamoslo como los puntos de guardados de los videojuegos. En este caso guardan el estado de todos los archivos de tu repositorio en el momento en el que se hizo, va firmada con el autor, fecha y demas información util para los demas desarrolladores.

Para hacer un commit los archivos deben haber estado previamente en la etapa de Staged.

<p align="center">
  <img src="https://media.licdn.com/dms/image/C4E22AQErd4dfzpgJQg/feedshare-shrink_800/0/1667848522109?e=2147483647&v=beta&t=wUNCJD38buj0A8_U-uc_9d0kjw7cIvbq9kMdTlRzcnU" alt="Imagen control de versiones distribuidos" width="350">
</p>

## ¿Qué es el HEAD?

Entiendelo como un marcador que te dice: "estás aquí"

Este marca el commit en el que te encuentras actualmente y puedes verlo con `git log` y yendo al commit mas actual.

Ejemplo:

```yaml
commit bd68fe7a12bedcff7f3330ec376ec1dfea2fad4b (HEAD -> main)
Author: SebastianBarreraVargas <sebastinbarreravargascat2014@gmail.com>
Date:   Sun May 5 18:20:18 2024 -0400
```

<details>
    <summary> Abreme para ver mas comandos!  :exclamation: :exclamation:</summary>
  
### Comandos variados que se llevaron durante la clase

<div align="center">

Comando       |Descripción|
|---------------|:--------------|
| Cambiar `<tu_archivo>` por .      |Esto aplica el comando a todos los archivos.|
| git rm `<tu_archivo>`        |Este comando remueve un archivo de la lista de add.|
| git commit -m "`<aqui va la info del commit>`"      |Es para hacer un commit sin abrir una ventana en VSC.|
| git commit --amend -m "`<nuevo mensaje para el commit>`"        |Este comando cambia el mensaje del ultimo commit realizado.|
| git commit -am "`<tu mensaje>`"      |Este comando hara stage y commit de todos los archivos rastreados.|
| git checkout `<id del commit al que quieres cambiar>`      |Puedes volver a un commit anterior copiando su id en ese comando, basicamente cambiar el HEAD alli.|

</div>

</details>

# Clase 2
## ¿Qué es una rama?
Es una versión separada del repositorio principal. Al ser una linea de desarrollo independiente cualquier cambio que hagas en la rama se mantendra separado de las demas, hace mas dificil que el codigo inestable se fusione con el principal. Ademas permiten un desarrollo no lineal y colaborativo.

<p align="center">
  <img src="https://www.espai.es/blog/wp-content/uploads/2021/05/desarrollo-con-ramas-git.jpg" alt="Imagen control de versiones distribuidos" width="450">
</p>

* Cuando quieras agregar una nueva caracteristica o corregir errores, sin importar lo pequeños que sean deberias crear una nueva rama para encapsular tus cambios.

* Cuando el trabajo este completo puede fusionarse con la rama principal.

## Creación de una rama

 :warning: Para crear una rama debes tener almenos un commit en el repositorio!! La rama se creara en base al ultimo commit de la rama en que creaste la nueva rama.

 <p align="center">
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/a5.gif" alt="Imagen Referencia" width="350">
</p>

Para crear una rama usaremos el comando:
* git branch `<nombre_rama>`

Cambiamos a nuestra nueva rama:
* git switch `<nombre_rama>`

#### Datasos curiosos
  Si creas una copia de una rama, los id's de los commits seran los mismos :nerd_face: :point_up:

  Esto pasa por que enrealidad al hacer una rama o merge estamos creando una copia de ese commit por lo que en esencia seria el mismo.

## Fusionar ramas

Las ramas que creamos tienden a tener el destino de ser fusionadas con otra rama (Cabe recalcar que no pasa siempre). 

La fusión es que los cambios que hemos realizado en nuestra rama se incorporaran a otra. 

<p align="center">
  <img src="https://static.javatpoint.com/tutorial/git/images/git-merge-and-merge-conflict.png" alt="Gif conflictos" width="450">
</p>

Usaremos el siguiente comando para incorporar los cambios a la rama en la que nos encontramos en ese momento:

* git merge `<nombre_rama>`

## Eliminar ramas
Despues de una fusión es probable que desees eliminar la rama que fusionaste para no dejarla suelta ya que ahora perdio su utilidad. Usaremos el comando:

*  git branch --delete `<nombre_rama>`

    o

* git branch -d `<nombre_rama>`

<p align="center">
  <img src="https://media.licdn.com/dms/image/D5612AQEgQz8BlpV2Ng/article-cover_image-shrink_600_2000/0/1687213388847?e=2147483647&v=beta&t=FRVXhh5Tqpel67GmW1r-7qpMIf4-ZiLDVpFRcl_gIZQ" alt="Eliminando ramas" width="250">
</p>

Cabe recalcar que si la rama que quieres eliminar no fue fusionada, te devolveran el siguiente error:

```yaml
error: The branch 'branch_name' is not fully merged.
If you are sure you want to delete it, run 'git branch -D branch_name'.
```

## Merge No Fast-Forward

<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTEX-2DuVzEOxibvIfoYAhLDMZTskvjcIUXe6nPskhFtw&s" align="right"
     alt="Fast Forward" width="100" height="100">

### ¿Qué es un fast-forward?
Cuando haces una fusión y los commits de esta rama estan directamente delante de la rama actual, Git hara por defecto un "fast-forward merge", lo que significa que simplemente movera el puntero de la rama actual hacia adelante ya que no hay divergencia de codigo entre las dos ramas.
### ¿Qué nos permite hacer?
Nos permite hacer merges creando un commit para indicar que se hizo una fusión.

Usamos el comando:

* git merge `<tu_rama>` --no-ff

## Conflictos en Git

Ocurren al querer fusionar a una rama que realizo cambios justo en las mismas lineas del fichero al que queremos fusionarnos.

<p align="center">
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/image.jpg" alt="Imagen tiburón" width="300">
</p>

### Resolviendo conflictos
Cuando nos ocurra esto debemos seleccionar con que cambio nos quedaremos, aunque tambien podriamos fusionar ambos a la rama con las opciones que nos ofrece Visual Studio.

<p align="center">
  <img src="https://www.jorgeacortes.com/blog/wp-content/uploads/2019/01/merge-conflict-solve-vs-code.gif" alt="Gif conflictos" width="650">
</p>

<details>
    <summary> Abreme para ver mas comandos!  :exclamation: :exclamation:</summary>
  
### Comandos variados que se llevaron durante la clase

<div align="center">

Comando       |Descripción|
|---------------|:--------------|
| git switch -c `<nombre_rama>`      |Crea la rama y automaticamente te lleva a ella.|
| git checkout -b `<nombre_rama>`      |Un comando mas que crea la rama y automaticamente te lleva a ella.|
| git checkout `<nombre_rama>`      |Un comando mas que te cambia a la rama `<nombre_rama>`.|
| git merge --edit      |Abre el editor antes de hacer el commit.|
| git merge --no-commit      |Evita que se haga commit automaticamente.|
| git branch -D `<nombre_rama>`      |Fuerza la eliminación de una rama.|
| git branch -a      |Nos permite visualizar todas las ramas incluso las que estan en el remoto.|
| git log --oneline      |Nos permite visualizar el historial de commits pero solo mostrandonos los nombres.|
| git log --graph      |Nos permite visualizar el historial de commits con una ayuda grafica.|
| git log --graph --oneline      |Nos permite visualizar el historial de commits con una combinacion de las dos anteriores opciones.|
</div>

</details>

# Clase 3

## Repositorios remotos
Estan hospedados en un servidor y serviran de punto de sincronización entre diferentes repositorios locales.

<p align="center">
  <img src="https://static.platzi.com/media/user_upload/Git%20push-88e4f9c0-01af-4253-b351-5e9a036e5a43.jpg" alt="Imagen Repos" width="300">
</p>

## Navegando por GitHub

### Buscar perfiles
Para buscar perfiles debemos seguir los siguientes pasos

<p float="center">
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/Captura%20de%20pantalla%202024-05-06%20102952.png" width="300" />
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/Captura%20de%20pantalla%202024-05-06%20103125.png" width="300" /> 
</p>
<p float="center">
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/Captura%20de%20pantalla%202024-05-06%20103201.png" width="350" />
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/Captura%20de%20pantalla%202024-05-06%20103247.png" width="350" /> 
</p>

La herramienta de busqueda en GitHub te puede servir para buscar contenido de otras personas y asi inspirarte en ellos y adaptar su codigo al tuyo.

<div align="center">

Area       |Descripción|
|---------------|:--------------|
|Code       |Sirve para ver las ramas e intercalar entre ellas, podras ver tus archivos, agregar archivos y añadir codigo.|
|Pull Requests       |Por asi decirlo es como un hilo de Twitter (X) en el cual se sigue una conversación sobre un topico en especifico.|
|Actions       |Es "una forma de automatización" cuando hagas ciertas acciones se ejecutaran otras acciones, se utiliza para el despliegue.|
|Projects       |Podemos crear un "Canvan" ver que tareas se haran respecto a una cierta historia de usuario.|
|Seguridad       |Sirve para administrar permisos, podremos por ejemplo modificar que cierta rama no la pueda modificar cualquier persona.|
|Wiki       |Documentacion mas extensa que un README.|
|Insights       |Nos permite ver estadisticas de nuestros repositorios.|
|Settings       |Podemos configurar diferentes cosas de nuestro repositorio, solamente esta disponible si somos el dueño del repositorio.|
</div>
Aqui se puede ver la estructura de la pagina code:

<p align="center">
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/ApartadoDeCode.jpg" alt="Imagen Code" width="700">
</p>

## Empezando un nuevo repositorio
Primero iremos a la pestaña `Create new` en Git Hub y elegiremos `New repository`

<p align="center">
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/Nuevo%20repositorio.png" alt="Imagen nuevo repo" width="150">
</p>

Llenaremos los datos con la informacion de nuestro repositorio, ademas podremos elegir un .gitignore y una licencia.

<p align="center">
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/Ejemplo%20nuevo%20repo.png" alt="Imagen ejemplo de nuevo repo" width="500">
</p>

## Sincronizando nuestro repositorio
Usaremos el siguiente comando en Git para poder sincronizarnos:

* git remote add `<nombre_repo_remoto>` `<url_repo>`

### ¿Como obtengo la `url_repo`?

Debemos ir al apartado de `Code` dentro de nuestro repositorio, ahora al icono verde que dice `<> Code` y podemos copiar el vinculo `HTTPS` para nuestro comando git remote. Luego de vincular tu codigo podras usar el siguiente comando para ver las conexiones remotas que tienes:

* git remote -v

<details>
    <summary> Abreme si quieres vincular tu repositorio con una clave SSH!  :exclamation: :exclamation:  :exclamation: :exclamation: </summary>

## Vincular un repositorio con clave SSH

### Crear la key
* ssh-keygen -t rsa -b 4096 `<tucorreo@gmail.com>`
* Al crearlo podras elegir una passphrase
### Pondremos a ejecutar la llave
* eval "$(ssh-agent -s)"
### Añadir la llave
* ssh-add~/.ssh/id_rsa
* Copias del portapapeles el id_rsa.pub
* Pegas en la seccion key de tu repositorio.

</details>

## Sincronizando repositorios

Usaremos un nuevo comando llamado git push, nos permite sincronizar nuestros cambios del repositorio local a nuestro repositorio remoto.

No necesariamente debe ser la rama main.

* git push `<nombre_repo_remoto>` `<rama_a_subirse>`

## Clonar repositorios
Para clonar con HTTPS:
* git clone `<url_repo_HTTPS>`

Para clonar con SSH:
* git clone `<url_repo_SSH>`

<details>
    <summary> Abreme para ver mas información!  :exclamation: :exclamation:  </summary>
  
### Datos o comandos variados llevados durante la clase

<div align="center">

Comando       |Descripción|
|---------------|:--------------|
| Forks      |Herramienta para aportar a un codigo que no te pertenece, puedes clonartelo y añadirlo a tus repositorios, puedes subir tus cambios para que el propietario pueda añadirlo si quiere.|
|Issues       |Es abrir un hilo, en el que comentas que errores puede tener el codigo y que se puedan realizar cambios en base a eso.|
|git push -f `<nombre_repo_remoto>` `<rama_a_subirse>`       |Forzara a sincronizar los cambios con el repositorio remoto (no recomendado).|
|git push -u `<nombre_repo_remoto>` `<rama_a_subirse>`       |Sube tus cambios a la rama “main” del repositorio “origin” y establece esa rama como la rama por defecto para futuros comandos git push.|
|git push -all `<nombre_repo_remoto>`  |Sincroniza todas las ramas con el repo remoto.|
|git remote prune `<nombre_repo_remoto>`|Borra las ramas del repositorio local que ya no existen en base al repositorio remoto.|
|git fetch|Se utiliza para descargar todos los datos de un repositorio remoto que no están presentes en tu repositorio local. Esto incluye nuevas ramas, actualizaciones a ramas existentes y otros cambios.|
|git branch -a|Lista todas las ramas, tanto las locales como las remotas.|
|git tag `<nombre-de-la-etiqueta>` `<identificador-del-commit>`|Agregas una etiqueta a un commit especifico|
|git remote remove `<nombre_repo_remoto>`|Elimina un alias de repositorio remoto|
</div>

</details>

# Clase 4
## Push, Pull & Pull request
### Experimentos con git push
 ## Experimento #1
 
**¿Que pasa si intento hacer git push desde una rama diferente con git push origin main?**

Bueno en el ejemplo estamos en la rama login e intentamos hacer el comando `git push origin main`
```bash
Sebas@DESKTOP-12UFO49 >MINGW64 ~/Remake/>CursoGit (login)
$ git push origin main
Everything up-to-date
```
Lo que sucede es que el comando intenta subir todos los cambios de la rama main
(local) pero este >ya esta con los cambios mas actuales en el remoto.

Para subir codigo a la rama main desde una rama diferente debo usar el siguiente codigo:
 * git push origin `<Rama_Remitente>`:`<Rama_Destinatario>`

 ## Experimento #2
 
 **La duda del push -u**

 Cuando tu quieres subir una rama nueva de tu repositorio local al repositorio remoto tal vez lo primero que pensarias es que debes usar `git push`, pero que ocurre si lo haces?

```bash
Sebas@DESKTOP-12UFO49 >MINGW64 ~/Remake/>CursoGit (login)
$ git push
fatal: The current branch login has no >upstream branch.
To push the current branch and set the >remote as upstream, use

    git push --set-upstream origin login

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.
```

Esto ocurre ya que tu rama no existe en el repositorio remoto, asi que deberas usar este comando:

* git push --set-upstream origin `<rama_nueva_a_subir>`

Pero la manera abreviada es:

>* git push -u origin `<rama_nueva_a_subir>`

## Experimento #3
**El peligro del `git push -f`**

Esta practica es muy peligrosa ya que podrias estar sobreescribiendo o perder algun archivo si fuerzas a sincronizarse a los repositorios.

<p align="center">
  <img src="https://preview.redd.it/git-push-force-v0-ky1rwu4yql5a1.jpg?auto=webp&s=319ce7412da353e8b69c261b1cf609dd46940f00" alt="Imagen Force" width="250">
</p>
>Es muy recomendable no realizarla. Aunque puede llegar a usarse para eliminar commits malos que quieren purgarse absolutamente.

## Experimento #4
### **Eliminar ramas remotas**

Con esto podras eliminar ramas de tu repositorio remoto. Si bien no es necesariamente una mala practica debes tener unas cuantas precauciones a la hora de usarlo:

* Verifica que la rama cumplio su vida util: Debes corroborar que tu rama hubiese cumplido con su proposito y su contenido ya este fusionado o ya no sea de importancia.
* Comunicate con los demas: Avisa que lo haras, ya que otros miembros podrian estarla usando o tener cambios que aun no subieron.

Aclarado esto, puedes usar el siguiente comando para eliminar ramas remotas:

* git push -d `<nombre_repo_remoto>` `<rama_a_eliminar>`

<details>
    <summary> Abreme para ver mas comandos push!  :exclamation: :exclamation:  </summary>
  
### Datos o comandos variados llevados durante la clase

<div align="center">

Comando       |Descripción|
|---------------|:--------------|
|git push -f `<nombre_repo_remoto>` `<rama_a_subirse>`       |Forzara a sincronizar los cambios con el repositorio remoto (no recomendado).|
|git push -u `<nombre_repo_remoto>` `<rama_a_subirse>`       |Sube tus cambios a la rama “main” del repositorio “origin” y establece esa rama como la rama por defecto para futuros comandos git push.  Al usar este parámetro, Git recordará las opciones que has utilizado, por lo que en el futuro puedes simplemente escribir git push y Git sabrá qué hacer|
|git push|Sincroniza la rama solo si hiciste el comando de arriba con anterioridad|
|git push -all `<nombre_repo_remoto>`  |Sincroniza todas las ramas con el repo remoto, especificando origin.|
|git remote prune `<nombre_repo_remoto>`|Borra las ramas del repositorio local que ya no existen en base al repositorio remoto.|
|git push --all|Este comando empuja todas las ramas al repositorio remoto por defecto. Si no se especifica un repositorio remoto, Git utilizará el que esté configurado como el remoto por defecto.|
|git push origin `<rama_a_subirse1>` `<rama_a_subirse2>` `<rama_a_subirseN>`|Sube las ramas especificadas al mismo tiempo.|
</div>

</details>

## Acerca de git pull
Git pull se utiliza para actualizar tu repositorio local con los ultimos cambios que tenga el repositorio remoto en ese momento.

<p align="center">
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/images.jpeg" alt="Imagen Pull" width="450">
</p>

### Adentremonos en comandos principales

El comando para hacer un git pull es simplemente:

* git pull

Este comando descarga los cambios del repositorio remoto y los combina con tu rama local. Si estás trabajando en una rama específica y quieres obtener los últimos cambios de esa rama en el repositorio remoto, puedes usar:

* git pull `<nombre_repo_remoto>` `<nombre_rama>`

Donde `<nombre_rama>` es el nombre de la rama de la que quieres obtener los cambios.

### ¿Se pueden producir conflictos con git pull?

Si se pueden producir ya que estas combinando cambios, pero la diferencia es que en este caso los cambios iran directamente a tu repositorio local

<details>
    <summary> Abreme para ver mas comandos push!  :exclamation: :exclamation:  </summary>
  
### Datos o comandos variados llevados durante la clase

<div align="center">

Comando       |Descripción|
|---------------|:--------------|
|git pull `<nombre_repo_remoto>` `<nombre_rama_a_traer>`|Puedes traerte cambios desde otra rama remota a tu rama actual con el siguiente comando. Se hara un commit indicando que se realizo esta acción.|
|git pull --all|Atrae cambios de todas las ramas del remoto a sus respectivas ramas en el local. Sin embargo, este comando no creará nuevas ramas locales para las ramas remotas que no existen en tu repositorio local. En la clase se tuvo que hacer un git pull --set-upstream origin `<rama>` para que funcione.|
|git pull origin `<rama_a_jalarse1>` `<rama_a_jalarse2>` `<rama_a_jalarseN>`|Jala las ramas especificadas al mismo tiempo.|

</div>

</details>

## Pull Request (PR)

Es una propuesta para incluir tus cambios en el código (commits) de una rama a otra, generalmente de una rama de trabajo a la rama principal del proyecto.

Los responsables del repositorio evaluaran los cambios que has hecho, discutir posibles modificaciones, y si están de acuerdo, pueden fusionar tus cambios en la rama objetivo.

<p align="center">
  <img src="https://media-assets-cdn.zenduty.com/blogscontent/2023/12/Pull_request.webp" alt="Imagen PullRequest" width="700">
</p>

### ¿Como se hace?
#### **Opcion 1**
1. Cuando hagas un git push en tu git hub te deberia aparecer una ventana en la que podrias hacerlo  (si es que no apareciera podrias ir al apartado de `Pull Request`).
2. Darle un titulo y una descripción.
3. Git Hub hara verificaciones y si no hay conflictos tu solicitud procedera.
#### **Opcion2**
1. Ir al apartado de `Pull Request`
2. Apretar en `New pull request`
3. Elegir una rama base a la que se llevaran los cambios (a la izquierda) y la rama que se va a combinar (derecha).
<p align="center">
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/Imagen%20alternativa%20pull%20request.png" alt="Imagen Referencia" width="450">
</p>

4. Darle un titulo y una descripción.

5. Git Hub hara verificaciones y si no hay conflictos tu solicitud procedera.

NOTA :exclamation: :exclamation: : No puedes revertir un pull request si ya lo añadiste!!! Asi que ten cuidado al revisarlos, no pongas que si a todo!!!(aunque podrias hacerle cambios)

<p align="center">
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/Captura%20de%20pantalla%202024-05-10%20192454.png" alt="Imagen Referencia" width="300">
</p>

### ¿Como hago un buen Pull Request?
<div align="center">

Comando       |Descripción|
|---------------|:--------------|
|Haz commits pequeños y significativos|Cada commit debe representar un cambio lógico y coherente. Esto facilita la revisión del código y la identificación de posibles errores.|
|Actualiza tu rama antes de hacer el Pull Request|Antes de crear un Pull Request, asegúrate de que tu rama esté actualizada con la última versión de la rama a la que quieres fusionar tus cambios. Esto puede evitar conflictos de fusión.|
|Describe claramente tu Pull Request|Al igual que con los mensajes de commit, la descripción de tu Pull Request debe explicar qué cambios hiciste, por qué son necesarios y cualquier detalle importante que los revisores deban saber.|
|Sigue las convenciones del proyecto|Cada proyecto puede tener sus propias convenciones y guías de estilo. Asegúrate de seguir estas convenciones para mantener la coherencia del código.|
|Prueba tus cambios|Antes de hacer un Pull Request, debes probar tus cambios para asegurarte de que funcionan como se espera y no introducen nuevos errores.|
|Solicita revisiones de código|Solicita la revisión de tu código a tus compañeros de equipo. Ellos pueden ofrecerte valiosos comentarios y sugerencias para mejorar tu código.|

</div>

### Revisar un pull request
Algunas recomendaciones para revisar una PR son:

* Comprender el contexto: Antes de comenzar la revisión, asegúrate de entender por qué se está haciendo la Pull Request y qué problema está tratando de resolver.
* Comprobar la coherencia del código: Asegúrate de que el código sigue las convenciones de codificación y estilo del proyecto.
* Buscar posibles errores: Revisa el código en busca de posibles errores, problemas de rendimiento, seguridad, etc.
* Dar feedback constructivo: Cuando encuentres problemas, proporciona comentarios claros y constructivos. Explica por qué algo es un problema y, si es posible, sugiere una solución.
* Aprender y compartir conocimientos: Las revisiones de código son una excelente oportunidad para aprender y compartir conocimientos. Si ves algo que no entiendes, pregunta. Si ves algo impresionante, dilo.

# Clase 5
## Flujos de trabajo
Los flujos de trabajo son maneras de organizar nuestras ramas y archivos durante el trabajo en equipo en un repositorio remoto.
Algunos ejemplos son:

* GitFlow
* GitHub Flow
* Trunk Based Development
* Forking Flow

Hablaremos un poco acerca de ellos:
## GitFlow
Siendo uno de los flujos mas antiguos, actualmente a perdido algo de popularidad viendose opacado por otros flujos de trabajo, aun asi es de los mas importantes, tiene la siguiente estructura:

<p align="center">
  <img src="https://miro.medium.com/v2/resize:fit:800/1*u4dlEq4sqIT6iHL_Usvwnw.png" alt="Imagen GitFlow" width="450">
</p>

1. Main: Contiene el codigo en produccion, almacena el historial de lanzamientos (no se toca directamente esta rama, solo para hotfix)
2. Develop: Esta rama nace directamente del main y contiene el codigo en pre-produccion,sirve como una rama de integracion para las caracteristicas.
3. Feature: Estas ramas nacen de los develop, aqui se integran funcionalidades.
4. Release: Se crean para preparar/mantener/registrar lanzamientos. Las correciones de errores deben ser aplicadas a esta rama antes de fusionarlas con el main.
5. Hotfix: Puede llegar a generar confusion con la rama Release pero la diferencia clave es que estas se crean directamente del main y corrigen errores puntuales en este, posteriormente se fusionan con el main y develop.

## GitHub Flow

Un flujo de trabajo con menos ramas que GitFlow, por esto es mucho mas ligero. Aqui se trabaja en un entorno de implementacion continua, no hay lanzamientos ya que ni bien se acaba una funcion esta esta disponible en ese preciso momento.

<p align="center">
  <img src="https://user-images.githubusercontent.com/6351798/48032310-63842400-e114-11e8-8db0-06dc0504dcb5.png" alt="Imagen GitHub Flow" width="450">
</p>

Deberemos seguir una serie de postulados para asi garantizar un codigo listo para la produccion. Tendremos dos ramas:

* **Main** : La rama en la que se integraran los cambios. Debe mantenerse protegido el `Main` asi que no se realizaran cambios directamente encima de este.
* **Feature** : Esta nace directo de la rama `main`, la vida de estas ramas debe ser lo mas corta posible. Cabe mencionar que con este tipo de flujo de trabajo tendremos que crear muchisimas ramas. Hablemos un poco del ciclo de vida de estas ramas:

  * Relizamos los commits.
  * Hacemos la Pull Request.
  * El grupo discute y/o da recomendaciones.
  * Se hacen pruebas de CI (Integracion Continua)/Entorno de produccion.

  ## Trunk Based Development

Nota: Segun lo dicho en clases esto es solo para tryhards :nerd_face: :point_up:

Tiene cierta similitud con GitHub Flow, tenemos estas ramas:

* `Main` 
* `Feature`

No necesariamente requiere de un Pull Request ya que en casos de arreglos ligeros para arreglar cosas no tan importantes haciendoles commit dentro del main. 

<p align="center">
  <img src="https://statusneo.com/wp-content/uploads/2022/08/tbd_workflow.drawio-1-1.png" alt="Imagen PullRequest" width="450">
</p>

Se pueden llegar a usar `actions` para automatizar ciertas areas para el despliegue.

## Ship / Show / Ask
Nota: Segun lo dicho en clases esto es solo para tryhards :nerd_face: :point_up:

Dicha y hecha la advertencia, exliquemos como funciona:

* `Ship`: Los cambios son directamente fusionados a la rama principal. Esto es si estas muy seguro de lo que estas haciendo.
* `Show`: Fusionara el codigo a la rama principal pero abrira una peticion de cambios para que lo revisen. Para personas que dudan un poco de lo que estan haciendo.
* `Ask`: Abre la PR para que sean revisados antes de fusionarse. Para personas inexpertas o que quieren que otros le aconsejen.

Es importante que para hacer este flujo exista un buen sistema CI/CD, un equipo confiable con buenas practicas que haya superado el ego individual.

# Clase6
## Buenas practicas en Git
Al igual que a la hora de programar, tambien tenemos buenas practicas a la hora de usar git, estos tienen propositos similares que las buenas practicas de programación, aun asi haremos un repaso de ellos:

* Mejor legibilidad para otros usuarios.
* Resolver conflictos sera mas facil.
* Te sera mas facil adaptarte a otros entornos de trabajo.

## Preguntas que podrias estarte haciendo

### ¿Cada cuanto hago un commit?
De preferencia amenudo, tipo es mejor que hagas cambios pequeños, no es bueno hacer un commit con 40 kilometros de recorrido ya que los errores que cometas seran mas dificiles de arreglas.

Esto no significa que hagas un commit de cosas sin sentido, hacelas con criterio.

### ¿Como escribo buenos commits?

Bueno hay ciertas reglas/consejos que deberias seguir para que tengas mejores commits, te dare algunos ejemplos de ellas:

* Hace tus commits en verbo imperativo.
* No uses punto final ni suspensivos en tus commits.
* Maximo 50 caracteres, tipo mantente en un margen cerca de 50 no pasa nada si te pasas por un poco.
* Añade el contexto necesario.
* Usa prefijos para especificar que tipo de commit es ejemplo:
  * `feat`: Una nueva característica para el usuario.
  * `fix`: Arregla un bug que afecta al usuario.
  * `perf`: Cambios que mejoran el rendimiento del sitio.
  * `build`: Cambios en el sistema de build, tareas de despliegue o instalación.
  * `ci`: Cambios en la integración continua.
  * `docs`: Cambios en la documentación.
  * `refactor`: Refactorización del código como cambios de nombre de variables o funciones.
  * `style`: Cambios de formato, tabulaciones, espacios o puntos y coma, etc; no afectan al usuario.
  * `test`: Añade tests o refactoriza uno existente.

### ¿Como hago buenos nombres de rama?
Se consistente al crear tus nombres de rama, ademas es recomendable describir el proposito de la rama en esta ejemplo: 

* feature/add_new_class

# Clase 7

## Deshacer cambios

Hay que deshacer cambios cuando por ejemplo tenemos un error grave que queremos corregir pero se complica, entonces es prudente volver a un punto anterior. Tambien puede usarse para recuperar archivos borrados.

<p align="center">
  <img src="https://asjordi.dev/_astro/cover.BWPm3lhd_CGrGv.webp" alt="Imagen PullRequest" width="450">
</p>

## Comandos destructivos

Estos pueden llegar a alterar el historial de commits. Lo opuesto serian los no destructivos, estos trabajan en base al historial sin afectarlo, se basan en este para crear nuevos commits.

<div align="center">

Comando       |Descripción|
|---------------|:--------------|
|git reset --soft `id_commit_que_quieres_ir` o  tambien git reset --soft HEAD~`tu_numero_de_commit`|Mantiene los cambios que ocurrieron antes de hacer commit de donde apunta. Quita la capacidad de volver a puntos futuros.|
|git reset --hard `id_commit_que_quieres_ir` o tambien git reset --hard HEAD~`tu_numero_de_commit`|Descarta todos los cambios. Quita la capacidad de volver a puntos futuros.|
| git commit --amend -m "`<nuevo mensaje para el commit>`"        |Este comando cambia el mensaje del ultimo commit realizado.|
|git push -f `<nombre_repo_remoto>` `<rama_a_subirse>`       |Forzara a sincronizar los cambios con el repositorio remoto (no recomendado).|

</div>

Es peligroso hacer comandos destructivos cuando trabajas con mas personas ya que el id cambia. Y si tu lo pusheas, habra problemas cuando ellos lo bajen.

## Comandos no destructivos

Estos comandos no alteran el historial de commits.

<div align="center">

Comando       |Descripción|
|---------------|:--------------|
|git revert HEAD~`<numero_de_commit>` o con git revert HEAD`<id_commit>`|Revierte los cambios que un commit introdujo y crea uno nuevo con los cambios revertidos.|
|git revert --abort|Aborta el revert.|
|git revert --continue|Continua con el revert luego de solucionar conflictos. (si es que hubiese)|
|git checkout `id_commit`|Con este comando podemos volver a una etapa anterior de nuestro codigo, ahi podras observar como se encontraba tu codigo en ese commit.|
|git checkout `<id_commit>` `<archivo_recuperar>`|Puede traer un archivo en especifico del pasado y agregarlo en el presente.|
</div>

# Clase 8

## Hooks

### ¿Qué es un hook?

Un hook es una especie de automatización que ocurrira cuando ocurran determinados eventos. Nos permiten personalizar el comportamiento de Git.

Por ejemplo, puedes usar un hook para ejecutar un proceso de comprobación de los nombres de los commits, evitando que se hagan a menos que tengan un prefijo.

<p align="center">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSgxA9FAxqJ9BK-d4O9wAx-pTFzMyqXXFp9rLuiwkH2sg&s" alt="Imagen Referencia" width="350">
</p>

 ### Hooks del lado del cliente:

Solo afectan al repositorio local en el que estan y su mayor desventaja es que sus acciones solo ocurriran para ti, siendo que tu equipo no tendra estos beneficios.

Tipos de hooks:

* pre-commit
* prepare-commit-msg
* commit-msg
* post-commit
* pre-push
* post-checkout y post-merge

## ¿Como añado un hook a mi repositorio local?

* Primero: Deberemos ir a la carpeta de nuestro proyecto y habilitar la visualización de archivos ocultos.

<p align="center">
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/PrimeraImagenHooks.png" alt="Imagen Referencia" width="500">
</p>

* Segundo: Entraremos en la carpeta .git, esta carpeta es crucial para la integridad de tu proyecto asi que te ruego no tocar cosas que no sabes. (Lo comprobe toqueteando en otro proyecto de prueba).

<p align="center">
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/SegundaImagenHooks%2B%7D.png" alt="Imagen Referencia" width="500">
</p>

* Tercero: Abre la carpeta hooks aqui encontraras varios hooks de muestra.

<p align="center">
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/terceraImagenHooks.png" alt="Imagen Referencia" width="500">
</p>

* Cuarto: Crea una copia del .sample y cambia el nombre de tu copia a un tipo de hook que tu desees. Abre el hook con un edito de codigo y posteriormente crea el codigo necesario para tu hook.

<p align="center">
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/cuartaImagenHooks.png" alt="Imagen Referencia" width="500">
</p>

* Quinto: Quitale el .sample a tu archivo. (En esta imagen usamos git para quitarlo pero podrias usar el edito de windows no hay problema)

<p align="center">
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/quintaImagenHooks.png" alt="Imagen Referencia" width="500">
</p>

Nota: Si quieres que otra persona tenga tus hooks debes pasarle tu archivo y el debe añadirlo a su carpeta hooks.

## GitHub Actions

Esta es una forma de introducir hooks para tu servidor, es una heramienta increible ya que no solamente te permite crear pasos para correr cosas en tu CI/CD, incluso te permite añadir "hooks" que otras personas ya hicieron lo cual es muy comodo y practico.

* Para añadir `Github Actions` que otras personas ya hicieron debes seguir los siguientes pasos:

1. Ir a la pestaña actions de tu repo remoto:

<p align="center">
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/GithubActionsParte1.png" alt="Imagen Referencia" width="350">
</p>

2. Buscar alguno que te interese y agregarlo.

<p align="center">
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/GithubActionsParte1-1.png" alt="Imagen Referencia" width="350">
</p>

<p align="center">
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/GithubActionsParte1-1.2.png" alt="Imagen Referencia" width="350">
</p>

**Nota:** No profundizaremos en tema de crear nuestras propias github actions ya que por lo menos en mi caso no lo llegare a implementar, pero en resumen para crear una github actions debes crear las mismas carpetas que se ven en la imagen 3 e introducir tu codigo personalizado enun archivo .yml posteriormente deberashacer commit y pushearlo a tu repo remoto, de esta forma estarias creando tus propios `Hooks` en github.

## ¿Qué son los alias?

Son formas de resumir comandos en Git. Un ejemplo de `alias` es el origin que usas para hacer push o pull, ya que estos resumen la parte de tu url.

<p align="center">
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/GitAlias1.png" alt="Imagen Referencia" width="350">
</p>

### ¿Como creo un alias?

Para crear un alias debes hacer el siguiente comando:

* git config --global alias.`<nombre_alias>` `<comando_a_ejecutar>`

Si haces esto podras ejecutar tu comando con:

* git `<nombre_alias>`

## Algunos trucos de Git

#### Guardar cambios temporalmente

* git stash

Cuando tienes archivos que no estan terminados en una rama y quieres cambiarte de rama pero no quieres hacer `git commit` podrias usar este comando, lo que hara es guardarlos en una lista. Para verla:

* git stash show

Para retomar tu trabajo y sacar los cambios de esa lista puedes usar:

* git stash pop

#### Detectar que commit introdujo un bug

* git bisect

Nota: Muchas gracias por leer, este es el fin de este documento que recopilo comandos de las clases de Winsor (el vicepresidente de la SCESI) y ademas muestra algunos comandos/información extra, el objetivo de este README fue que las personas que vayan a leer esto en un futuro puedan entender la función de diversos comandos y funcionalidades de Git, espero tengan un buen dia/tarde/noche.

**11 de mayo de 2024.**

[logo-SCESI]: https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/scesi-para-fondo-claro-1.png
[enlaceSCESI]: https://www.scesi.org