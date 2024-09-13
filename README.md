# PracticaGitHubKC-Jaime
Este Repositorio contiene la práctica de GitHub de Jaime González, que está cursando el Bootcamp de IA II en KeepCoding:

- ¿Qué comando utilizaste en el paso 11? ¿Por qué?

En el paso 11, he utilizado el comando `git reset --hard HEAD~1` ya que con git reset muevo el puntero head más el puntero de la rama en la que me encuentro, al commit que le especifique. En este caso, le he especificado que mueva el puntero head un commit hacia abajo con ~1. Se ha utilizado la rama --hard para que los cambios del staging area se vean reflejados también en el working copy, por lo que los cambios se han eliminado también de la copia local del fichero.

- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

En el paso 12 he utilizado el comando `git reset --hard 6f0978a` ya que, de nuevo, con git reset muevo el puntero head y el de rama al commit que se le especifique, en este caso le he especificado directamente el hash del commit que me interesa, que contiene los cambios que habíamos descartado en el último git reset. Al usar el fla --hard, he recuperado los cambios del commit a2aa6e5 en mi working copy.

- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?

Haciendo el merge de la rama main desde styled con `git merge main` no causa ningún conflicto porque la rama styled incluye todos los commit que tiene la rama main y por ello el merge no surge efecto, devolviendo el mensaje "Already up to date." 

- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?

Sí, causo conflicto ya que tenemos una ramificación y ambas ramas han modificado las mismas líneas del mismo fichero. Por ello, se genera un conflicto entre la rama styled y la rama htmlify. Se resuelve el conflicto mergeando ambas ramas y manteniendo el contenido de la rama styled.

- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?

Este merge no causa ningún conflicto, ya que realizamos un merge FastForward porque todos los commits de main, se encontraban en la rama styled. Por lo que el efecto de este merge es mover el puntero main al último commit de la rama styled, es decir, al commit en el que se encuentra el puntero styled en el momento del merge.

- ¿Qué comando o comandos utilizaste en el paso 25?

Para dibujar el diagrama del grafo del repo he usado el comando `git log --oneline --graph --decorate --all` 

- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?

Para el merge he realizado el siguiente comando `git merge --no-ff title -m "Merge no FastForward con title"`. Esto crea necesariamente un nuevo commit para mergear ambas ramas. Este merge podría ser FastForward perfectamente y no requerir de un nuevo commit, ya que la rama title contiene todos los commits de main.

- ¿Qué comando o comandos utilizaste en el paso 27?

Para deshacer el merge he realizado `git reset HEAD~1` sin --hard para mantener los cambios en el working copy.

- ¿Qué comando o comandos utilizaste en el paso 28?

Con el comando restore puedo descartar los cambios que tengo en el staging area de un fichero concreto. Por ello he usado `git restore git-nuestro.md`

- ¿Qué comando o comandos utilizaste en el paso 29?

Para eliminar la rama he ejecutado `git branch -d title`. Pero da un error ya que el merge se ha quedado a medias.

- ¿Qué comando o comandos utilizaste en el paso 30?

He realizado un `git reset --hard 3401d49` para recuperar los cambios del merge.

- ¿Qué comando o comandos usaste en el paso 32?

He usado `git reset 56d8093` para ir al primer commit

- ¿Qué comando o comandos usaste en el punto 33?

He usado `git reset 3401d49` para ir al commit de mergeo entre title y main
