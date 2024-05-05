# Curso Git y GitHub [![Logo de la SCESI][logo-SCESI]][enlaceSCESI]

## ¿Qué es un control de versiones?
Es un sistema para registrar cada cambio que se realiza en el código fuente de un proyecto. Basicamente permite un historial.

<p align="center">
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/VersionControl.jpeg" alt="Imagen Control de versiones" width="738">
</p>

## Importancia de un control de versiones
* **Seguimiento de cambios**, permitiendo un seguimiento y control, ademas que se podrian revertir errores.
* **Colaboracion eficiente**, facilita la colaboracion sobre todo en entornos de desarrollo intensos.
* **Seguridad**, siendo importante para garantizar la <span style="color:red">precisión</span> e <span style="color:red">integridad </span> de los archivos.
* **Flexibilidad** en el desarrollo.

## ¿Qué es Git?

<img src="https://www.google.com/url?sa=i&url=https%3A%2F%2Ficonscout.com%2Ficons%2Fgit&psig=AOvVaw1cVYHsovxbsYRFp8y_rzut&ust=1715010922191000&source=images&cd=vfe&opi=89978449&ved=0CBIQjRxqFwoTCND3sdjv9oUDFQAAAAAdAAAAABAd" align="right"
     alt="Git Logo" width="120" height="178">

Es un sistema de control de versiones distribuido, aloja una copia completa del repositorio en nuestra maquina local para que posteriormente podamos subirlo a un repositorio remoto y podamos hacer trabajo colaborativo.

## ¿Qué es un repositorio?

<img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/estanteria-la-casa-el-salon-pintado-por-queyla-9921013.jpg" align="right"
     alt="Estanteria" width="120" height="178">

Es el pilar de los sistemas de control de versiones.

Es una especie de almacen para guardar los archivos con diferentes versiones, ademas de su historico, metaforicamente podriamos decir que es una estanteria de libros.

## Algunos otros sistemas de control de versiones
* **GitLab**
* **Bitbucket**
* **Mercurial**
* **Bazaar**

## Mas acerca de sistemas de control de versiones
<details>
    <summary> Sistemas de control de versiones locales </summary>

  ### Sistemas de control de versiones locales
  Los sistemas de control de versiones locales son la forma más sencilla de tener un control de versiones y los utilizan principalmente los desarrolladores individuales en vez de los equipos. En un sistema de control de versiones local, todos los datos del proyecto se almacenan en una sola computadora y los cambios realizados en los archivos del proyecto se guardan localmente. 

<p align="center">
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/local.png" alt="Imagen control de versiones locales" width="738">
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
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/centralized.png" alt="Imagen control de versiones centralizado" width="738">
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
  <img src="https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/distributed.png" alt="Imagen control de versiones distribuidos" width="738">
</p>

Un beneficio clave de los DVCS es que permiten la colaboración en línea y fuera de línea. También proporcionan una mayor seguridad, ya que cada desarrollador tiene una copia completa del historial del proyecto.
</details>

[logo-SCESI]: https://github.com/SebastianBarreraVargas/Git/blob/main/Imagenes/scesi-para-fondo-claro-1.png
[enlaceSCESI]: https://www.scesi.org