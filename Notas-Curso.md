# Notas de Curso Git
 
[Link de curso](https://www.youtube.com/watch?v=VdGzPZ31ts8&t=14s&ab_channel=HolaMundo)

## ¿Qué es Git?

Nos permite tener un historial de todo el codigo que escribimos

Cuando el codigo crece hay mas probabilidad de errores.

### Rollback 
Volver a un version anterior

### Desentralizado
Cada Dev tiene una copia del codigo, los cambios pueden ser sincronizados

### Usos de Git
* Historial 
* Almacenar código
* Trabajar en equipo 
* Cuando se indrodujo un error

## Se usa la TERMINAL

## USA GIT BASH


### Como tratar los saltos de linea

Desarrollando en windows, el salto de linea agrega 2 caracteres:
* CR
* LF

Para subir codigo hay que eliminar CR

Core.autocrfl en TRUE

### Comandos

**git config -h** para ver todos las opciones que tengo en git

**ls dir cd**

**git init** 
para iniciar git en el directorio

Dentro de **.git** en el directorio correspondiente se van a estar ordenando los archivos y demas cosas

* HEAD
* config
* description
* hooks/
* info/
* objects/
* refs/

La carpeta .git siempre es ignorada

## git add 

Pasa a una esta de **STAGE**, no va a estar en el repositorio, aca **indicamos los cambios que se hicieron**. Se pueden agregar y sacar archivos.

## git commit

Pasamos los archivos **de STAGE a COMMIT** 

## git push

Almacenamos los archivos en un **SERVER**, en general GITHUB

Si eliminamos un archivo tenemos que agregar el archivo eliminado a STAGE para luego ser eliminado del SERVER 



## Probando
### git status

Veo si hubo cambios, archivos nuevos, etc.

### git add  
* puedo poner el **nombre+extensión** del archivo
* puedo poner una **comilla** "'" para agregar todos los archivos con X extensión          
* Si pongo un **punto** agrego TODO. Considerado **MALA PRACTICA**

### git commit -m "comentario"
El comentario tiene que hacer alución a lo que se esta commiteando


### git rm ARCHIVO

cuando eliminemos archivos


### Renombrar archivo
mv archivo.txt archivo1.txt

### Archivos para ingnorar siempre
* Variables de entorno .env
* contraseñas 
* Cosas de bases de datos

crear un .gitignore

git add .gitignore

git commit del archivo

### git diff

podemos ver 

 


# RAMAS 
Se pueden bifurcar y volver a unir 

**git branch**
 para ver la rama en la que estoy

**git checkout -b NombreDeLaRama** para crear una nueva rama


---
En git: 
**cat archivo**

Me muestra el contenido

---

**git checkout Rama** para cambiar de rama

**git merge nombre de la rama** para unir el contenido de los archivos. Para efectuar los cambios tenemos que estar en la rama master, sino no funciona
