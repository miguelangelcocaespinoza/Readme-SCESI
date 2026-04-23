# Trabajo Individual

Miguel Angel Coca Espinoza


## Clase 1


### Que es GIT?

![imagen de git](image/git.png)

Es un sistema de control de versiones
Basicamente para guardar cambios a lo largo de un proyecto de forma local

### Como nacio GIT?

![imagen de linus-linux](images/linuslinux.png)
![imagen de padre e hijo](images/padre e hijo.png)

Git nacio porque Linus Torvalds al estar usando BitKeeper se canso de las limitaciones que le imponian,
asi que del coraje el lo que hizo fue crear su propio sistema de control de versiones
lo cual le tomo unas 2 a 3 semanas y ya lo tenia listo.

### Como instalar GIT?

![imagen de linux](images/linux.png)

Para instalarlo lo unicio que se debe hacer es ingresar a la pagina de GIT https://git-scm.com/ 
en el cual debes seleccionar si lo descagaras para Windows, Linux, Mac OS en le caso de Windows solo es cuestion de descargar el instalador
pero en el caso de linux te da una serie de comandos que varian segun a la DISTRO que tengas
para ya luego tener GIT listo para su uso.

### Configuraciones Basicas

-git config --global user.name "Tu Nombre"
-git config --global user.email "tu@correo.com"
-git config --global core.autocrlf true

### Archivos que todo repositorio de GIT deberia tener

README.md 

![imagen de readme](images/readme.png)

.gitignore
 
![imagen de .gitignore](images/ignore.png)



## Clase 2 


### Los estados de GIT

![imagen de esquema](images/esquemagit.png) 

#### Directorio de trabajo (Modificado)

La carpeta local, pero no esta asegurado

#### Stage Area (Preparado)

El punto intermedio de el directorio y el repositorio
en el cual va lo que si quiero guardar

#### Repositorio Local (Confirmado)

Todos los cambio con ID (hash) uqe ya esta asegurado

### Directorio de trabajo (Modificado)  

Es la carpeta comun pero bajo la observacion de GIT y cataloga en:

#### Untracked

Significa sin seguimiento pero no hay una version anterior esto suele pasar cuando recien son creadas.

#### Modified 

Significa que en este caso GIT ya tiene una version previa de tu archivo pero lo modificaste, cambiaste nombre o eliminaste.

Archivo que no este en el .gitignore se procedera a su catalogacion ya sea Untracked o Modified 


Cuando quiero que un archivo modificado anteriormente vuelva a su estado original se usa:
git restore <archivo>
Nota: Borra todo fisicamente por lo que no se podra recuperar 

![imagen de .gitignore](images/capgitignore.png)

En el caso en el que un archivo que cree no quiero que GIT lo vea:
Lo que debo hacer es agregar el nombre completo del archivo al .gitignore 



### Stage Area (Preparado)

Este nos permite seleccionar que archivos tendran seguimiento del commit 

git add <archivo>: Esto nos permite agregar uno por uno
git add .: Este agrega todos los archivos observados por GIT

Para sacar archivo del stage a un estado anterior

git restore --staged <archivo>

### Repositorio Local (confirmado)

Para crear un commit o punto de guardado se debe poner lo siguiente:

git commit -m "mensaje"

y para deshacer el ultimo commit es:

git reset --soft HEAD~1



![imagen de esquema 2](images/esquema.png)



### Buenas Practicas

####Cuando debo hacer un commit?
Se usara lo que es los commits atomicos, las confirmaciones seran de cada cambio o acciones importantes pero pequeñas y que tengan un significado.

### Escribir Buenos commits

Se deben usar pocas palabras pero efectiva:
#### Usar verbos imperativos (Add, Change, Fix, Remove)
-Add: Añadir un nuevo archivo 
-Change: indica una modificacion de un archivo
-Fix: Es para un arreglo de un Bug
-Remove: Cuando se elimina un archivo ya existente

#### No usar punto final ni puntos suspensivos en un mensaje de commit

(Mal) git commit -m "Add new search feature."
(Mal) git commit -m "Fix a problem with topbar..."
(Bien) git commit -m "Change the default system color"

### Escribe buenos commits'

-Usa como maximo 50 caracteres: El mensaje debe ser corto, objetivo y claro y solo debe tener un cambio y si se puede separar hazlo.
-Usa un prefijo para tus commits para hacerlos mas semanticos: Para que sea mas entendible de que se tratara el commit y de que trata

git commit -m "<tipo de commit>: <descripcion>"
ejm
git commit -m "feat:Add mew search feature"

### Prefijos
- feat: para una nueva caracteristica agregada.
- fix: para un bug que afecta a nuestro usuario.
- perf: para cambios que mejoran el rendimiento.
- build: para cambios del sistema.
- ci: para cambios en la integracion.
- docs: para cmabios en la documentacion.
- refactor: para cambios de nombre en variables o funciones.
- style: para cambios de formato, tabulaciones o cosas que no afectan a usuario.
- test: para test o refactorizacion de uno ya existente.

### Añade todo el contexto que sea necesario en el cuerpo del commit 
-En el caso en el que necesites agregar un mensaje mas largo se debe hacer lo siguiente:

git commit

prefijo: Titulo de tu commit

Cuerpo que describe tu commit











