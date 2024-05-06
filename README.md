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
    <summary> Sistemas de control de versiones locales </summary>

  ### Sistemas de control de versiones locales
  Los sistemas de control de versiones locales son la forma más sencilla de tener un control de versiones y los utilizan principalmente los desarrolladores individuales en vez de los equipos. En un sistema de control de versiones local, todos los datos del proyecto se almacenan en una sola computadora y los cambios realizados en los archivos del proyecto se guardan localmente. 

<p align="center">
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/local.png" alt="Imagen control de versiones locales" width="538">
</p>

Una de las herramientas de control de versiones locales más populares fue un sistema llamado RCS, que todavía podemos encontrar en muchas de las computadoras actuales. Esta herramienta funciona guardando conjuntos de parches (es decir, las diferencias entre archivos) en un formato especial en disco, y es capaz de recrear cómo era un archivo en cualquier momento a partir de dichos parches.

Aunque los sistemas de control de versiones locales pueden ser útiles para los desarrolladores individuales, tienen limitaciones significativas cuando se trata de la colaboración en equipo. Por ejemplo, no permiten que varios desarrolladores trabajen en el mismo proyecto al mismo tiempo de manera eficiente. Además, dado que todos los datos se almacenan localmente, si la computadora del desarrollador falla, se puede perder todo el historial del proyecto
</details>    
<details>
    <summary> Sistemas de control de versiones centralizados </summary>

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
    <summary> Sistemas de control de versiones distribuidos </summary>
  
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

</details>
<details>
    <summary> Abreme para ver mas comandos! </summary>
  
### Comandos variados que se llevaron durante la clase

<div align="center">

Comando       |Descripción|
|---------------|:--------------|
| Cambiar `tu_archivo` por .      |Esto aplica el comando a todos los archivos.|
| git rm `tu_archivo`        |Este comando remueve un archivo de la lista de add.|
| git commit -m "`(aqui va la info del commit)`"      |Es para hacer un commit sin abrir una ventana en VSC.|
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

Para crear una rama usaremos el comando:
* git branch `nombre_rama`

Cambiamos a nuestra nueva rama:
* git switch `nombre_rama`

#### Datasos curiosos
  Si creas una copia de una rama, los id's de los commits seran los mismos :nerd_face: :point_up:

  Esto pasa por que enrealidad al hacer una rama o merge estamos creando una copia de ese commit por lo que en esencia seria el mismo.

## Fusionar ramas

Las ramas que creamos tienden a tener el destino de ser fusionadas con otra rama (Cabe recalcar que no pasa siempre). 

La fusión es que los cambios que hemos realizado en nuestra rama se incorporaran a otra. 

Usaremos el siguiente comando para incorporar los cambios a la rama en la que nos encontramos en ese momento:

* git merge `nombre_rama`

## Eliminar ramas
Despues de una fusión es probable que desees eliminar la rama que fusionaste para no dejarla suelta ya que ahora perdio su utilidad. Usaremos el comando:

*  git branch --delete `nombre_rama`

    o

* git branch -d `nombre_rama`

Cabe recalcar que si la rama que quieres eliminar no fue fusionada, te devolveran el siguiente error:

```yaml
error: The branch 'branch_name' is not fully merged.
If you are sure you want to delete it, run 'git branch -D branch_name'.
```

## Merge No Fast-Forward

### ¿Qué es un fast-forward?
Cuando haces una fusión y los commits de esta rama estan directamente delante de la rama actual, Git hara por defecto un "fast-forward merge", lo que significa que simplemente movera el puntero de la rama actual hacia adelante ya que no hay divergencia de codigo entre las dos ramas.
### ¿Qué nos permite hacer?
Nos permite hacer merges creando un commit para indicar que se hizo una fusión.

Usamos el comando:

* git merge `tu_rama` --no-ff

<details>
    <summary> Abreme para ver mas comandos! </summary>
  
### Comandos variados que se llevaron durante la clase

<div align="center">

Comando       |Descripción|
|---------------|:--------------|
| git switch -c `nombre_rama`      |Crea la rama y automaticamente te lleva a ella.|
| git checkout -b `nombre_rama`      |Un comando mas que crea la rama y automaticamente te lleva a ella.|
| git checkout `nombre_rama`      |Un comando mas que te cambia a la rama `nombre_rama`.|
| git merge --edit      |Abre el editor antes de hacer el commit.|
| git merge --no-commit      |Evita que se haga commit automaticamente.|
| git branch -D `nombre_rama`      |Fuerza la eliminación de una rama.|
| git branch -a      |Nos permite visualizar todas las ramas incluso las que estan en el remoto.|
| git log --oneline      |Nos permite visualizar el historial de commits pero solo mostrandonos los nombres.|
| git log --graph      |Nos permite visualizar el historial de commits con una ayuda grafica.|
| git log --graph --oneline      |Nos permite visualizar el historial de commits con una combinacion de las dos anteriores opciones.|
</div>

</details>


[logo-SCESI]: https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/scesi-para-fondo-claro-1.png
[enlaceSCESI]: https://www.scesi.org