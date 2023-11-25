# Cursos Git Desarrollo Colaborativo

## Configurando GIT

> Agrego el usuario

```sh
git config --global user.name "Maximiliano Principe" # Global para todos los repos creados con mi usuario de windows.

git config --local user.name "Maxi Principe" # Local para este único repo. (Este comando se tiene que ejecutar cuando ya tengo un repositorio de git) 
```

> Agrego el mail

```sh
git config --global user.email "mlapeducacionit@gmail.com" # Global para todos los repos creados con mi usuario de windows.

git config --local user.email "mlapeducacionit@gmail.com" # Local para este único repo. (Este comando se tiene que ejecutar cuando ya tengo un repositorio de git) 
```

> Para verificar las configuraciones hechas

```sh
git config --global --get-regexp user
```

## Incializo un repositorio de GIT

```sh
git init # Va crear en la carpeta del proyecto una carpeta '.git' en el directorio (carpeta)
```

**IMPORTANTE**: No hay que borrar ni alterar manualmente los archivos dentro de la carpeta '.git. Solo trabajar git sobre esa carpeta, no nosotros.

```sh
clear # cls (ctrl + l -> Limpia la consola)
```

## Estados de los archivos
Los archivos en git pueden tener diferentes estados.

![Estados de los archivos](_ref/git-status.png)

* UNTRACKED: Significa que el archivo no está siendo seguido por GIT, sabe que existe pero no tiene idea de lo que pasa dentro del archivo. No lo controla git. No lo revisa.

* STAGED o Index: (Pre foto) Archivos que están preparandos para crear un commit (sacar la foto) el snapshot y preservar los cambios hechos de mi código fuente.

* UNMODIFIED: Los archivos respecto al LR no fueron modificados

* MODIFIED: Los archivos que con respecto al LR fueron modificados

## Zona/Area virtual de git

* Working Directory (WD): Área de trabajo donde se van agregando o quitando los archivos de mi proyecto)

* Staging Area (SA): (Pre foto): Área de control de cambios, se agregan los archivos para darle seguiendo)

* Local Repo (LR): (foto) Área de validación de cambios, donde se registran las modificaciones realizadas dentro del proyecto. 


## GIT STATUS
¿Qué hace? Controla en que estado están los archivos y en que zona o area de la estructura virtual están los archivos.

```sh
git status
```

## GIT ADD
Me permite marcar los archivos (pre foto) que considero listos para crear (foto) el commit (snapshot)

```sh
git add <nombre-archivo1> <nombre-archivo2> <nombre-archivo3>
git add README.md

## Agrega todo a la zona/area de (SA)
git add .
git add *.*
```

## GIT LOG
Me muestra la lista de commit (La timeline de fotos que tengo.) Cada commit tien un hash (el dni del commit (foto))

> Versión larga

```sh
git log 
```

> Versión corta

```sh
git log --version 
```

## .gitkeep
Git no versiona carpetas vacías por lo cual si yo necesito que una carpeta esté dentro del repositorio de git voy a tener que crear el archivo **.gitkeep**