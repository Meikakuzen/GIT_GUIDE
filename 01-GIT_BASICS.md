# GIT 1                                                    

## GIT BASICS 1

- La versión de git

> git --version

- La ayuda de git

> git help 

- La ayuda de un comando concreto. Salgo con Q

> git help commit

- Configurar git

> git config --global user.name "mi_nombre"
> git config --global user.email "mi_email"

- Listar la configuración

> git config --global -e

- Presionar la tecla A para modificar. Para salir Esc :wq! (w de write y q para salir, signo de admiración para que lo haga inmediatamente)

----

## GIT BASICS 2

- Iniciar git

> git init

- Esto crea el directorio .git en el repositorio. Si lo borras borras el repo. No se toca!

- Renombrar master a main

> git branch -M main

- **status** da la info sobre los commits, en que rama estoy

> git status

- Para añadir todos los archivos

> git add .

- Para añadir un archivo

> git add index.html

- commit es como hacer una foto. Con -m añado el nombre del commit en un solo paso

> git commit -m "first commit"

- **log** sirve para ver la info del commit, el autor, la fecha..

> git log
----

## GIT BASICS 3

- Si quiero revertir/reconstruir todo el proyecto a su última versión guardada en git

> git checkout -- .

- **branch** dice en qué rama estoy trabajando

> git branch

- Se pueden tener varias ramas de un repo. La rama puede regresar a la rama principal
- Se recomienda hacer el mínimo de modificaciones en el master. Suele ser la versión final para producción
- Mejor trabajar en ramas
- Para bajar un archivo del stage

> git rm --cached nombre_del_archivo

- Tambien puedo usar el **reset** para bajarlos del stage. Solo sirve si al archivo se le está dando seguimiento

> git reset nombre_del_archivo

- Si quiero tomar todos los archivos html sería

> git add *.html

### Diferentes formas de añadir al stage

- Para añadir un archivo en una carpeta

> git add uploads/*.js

- Por supuesto luego hay que hacer el **commit**
- Si quiero agregar todo un directorio con sus subcarpetas

> git add css/

### Creando Alias

- A veces hay comandos que se escriben muy a menudo, git status por ejemplo. Puedo crear un alias para este comando
- Me interesa solo saber la info del index. Puedo resumirlo con **--short**

> git status --short

- Puedo crear un alias para este comando. Por ejemplo s

> git config --global alias.s "status --short"

- Puedo editarlo usando este comando y tecleando A para editar. Esc :wq! para salir

> git config --global -e

- Puedo usar el comando **--online** para acortar la info

> git log --online

- Los alias son útiles para configurar outputs muy largos. Por ejemplo, de esta manera

> git config --global alias.lg "log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"





