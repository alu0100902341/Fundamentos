# Fundamentos del Desarrollo de Videojuegos

![N|Solid](http://derechoconstitucionalull.org/wp-content/uploads/2017/02/ULL-1.png)
[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Repositorio de la asignatura Fundamentos del Desarrollo de Videojuegos del Máster de Desarrollo de Videojuegos de la ULL

## Miembros del grupo
  - Eleazar Díaz Delgado
  - J. David Padilla Pérez
  - Ángel Luis Morales Hernández
  - Sergio Ravelo Vegino

### Resumen

> Este repositorio se utilizará como repositorio principal
> del grupo para esta asignatura.
> Aquí se subirán todas las prácticas y relacionados con la asignatura.
> Debe estar sincronizado entre todos los integrantes del grupo.

### Entregables
#### 1.- Reposito Git LFS
Git es un software de control de versiones diseñado por Linus Torvalds, pensando en la eficiencia y la confiabilidad del mantenimiento de versiones de aplicaciones cuando éstas tienen un gran número de archivos de código fuente. Su propósito es llevar registro de los cambios en archivos de computadora y coordinar el trabajo que varias personas realizan sobre archivos compartidos.

Git Large File Storage (LFS) es una aplicación que nos permite guardar ficheros binarios de gran tamaño junto un repositorio git.

##### Procedimiento
##
Lo primero que hemos hecho ha sido crear una jerarquía de carpetas con diferentes tipos de archivos sobre los cuáles queremos tener seguimiento en git. A continuación hemos inicializado el repositorio Git.

```
$ git init
```

Para poder ignorar ciertos archivos hemos generado un archivo .gitignore y le hemos añadido patrones a añadir.

```sh
$ touch .gitignore
$ vi .gitignore
> # Don't track these files
> /local
> /Big_images/*.bmp
```
Con esto estamos ignorando todo lo que esté en la carpeta /local y cualquier imagen dentro de la carpeta /Big_images cuyo formato sea BMP.
Luego hemos añadido todo los archivos al seguimiento (teniendo en cuenta que al tener .gitignore configurado no se añadirán ciertos archivos)

```sh
$ git add .
```
A continuación hemos instalado LFS y le hemos dicho que haga tracking sobre todos los archivos dentro de la carpeta /Big_images.

```sh
$ git lfs install
$ git lfs track "/Big_images"
```

Por último hemos añadido el repositorio remoto mediante el comando "git remote", hemos confirmado los cambios con "git commit" y hemos subido la jerarquía a git mediante "git push".

```sh
$ git remote fundamentos https://github.com/alu0100902341/Fundamentos.git
$ git commit -m "Primer commit"
$ git push fundamentos master
```

License
----

Universidad de La Laguna
