# Practica
# git


- ¿Qué comando utilizaste en el paso 11?
$ git reset --hard HEAD~1
¿Por qué?
con --hard borras el working copy y asi lo pide la practica

***************************************************************

- ¿Qué comando o comandos utilizaste en el paso 12?
$ git reflog
Para ver el ID del commit anterior donde aun no lo borraba

$ git checkout ed2119f
lo use para mover el HEAD a un viaje al pasado donde tenia el archivo modificado, me dice que detached HEAD y no me asusto :)

$ cat git-nuestro.md
compruebo que es el archivo del commit atras

$ git branch "temporal"
para crear una rama y hacer un commit 

$ git checkout temporal
me voy a esa rama (el apuntador head se va a esa rama)

$ git checkout styled
luego, me cambio a la rama styled

$ git merge temporal
entonces, celula absorbe a temporal y le quita sus poderes y ya tengo el archivo modificado como antes

$ git branch -d temporal
y borro la rama temporal porque ya no sirve para nada
Estoy en la rama styled y veo que el archivo es el modificado , todo bien.

***************************************************************

- El merge del paso 13, ¿Causó algún conflicto?
estoy en styled
$ git merge master
dice que todo esta bien
$ cat git-nuestro.md
hago un cat para ver el archivo despues del merge y veo que el archivo es el modificado, no hay conflictos

 ¿Por qué?
La verdad los archivos eran diferentes en ambas ramas y sin embargo no causo conflictos, es la primera vez que uso git , quiza con mas experiencia podria decir porque, o si me puedes dar feedback para entender. dice Already up to date al hacer el merge...

***************************************************************

- El merge del paso 19, ¿Causó algún conflicto? 
$ git merge htmlify
estoy en styled y mergeo a htmlify me marca conflicto
¿Por qué? dice que hay conflicto en el archivo git-nuestro.md que repare los conflictos y luego haga un commit

***************************************************************

- El merge del paso 21, ¿Causó algún conflicto?
$ git merge styled
estoy en master y absorbo styled, no causa conflicto
 ¿Por qué?  fue un fast forward , veo que el archivo es el de la 1a modificacion osea el que tenia styled, el puntero HEAD se mueve a donde estae el puntero de la rama styled y ahi tmbien esta ahora el puntero de la rama master, y tomó el archivo que tenia styled, la verdad no se porque, quiza con mas uso de git 
entienda que cuando se hace un merge los archivos se actualizan por asi decirlo a donde apunte HEAD.

***************************************************************

- ¿Qué comando o comandos utilizaste en el paso 25?
$ git log --graph --decorate --pretty=oneline

***************************************************************

- El merge del paso 26, ¿Podría ser fast forward? 
No, porque la rama title ya tenia un commit que es donde edite el archivo git-nuestro.md a mi gusto lo del titulo y cuando tienen ya un commit se tiene que hacer un nuevo commit para que una rama absorba a la otra.

***************************************************************
 
- ¿Qué comando o comandos utilizaste en el paso 27?
$ git reset HEAD~1
SIN LO DE --hard deshace el commit pero deja el working copy sin borrarlo

***************************************************************

- ¿Qué comando o comandos utilizaste en el paso 28?
$ git checkout -- git-nuestro.md

***************************************************************

- ¿Qué comando o comandos utilizaste en el paso 29?
$ git branch -D title
ya que primero utilice -d pero me dijo que title isn't fully merged y me dio la opcion de utilizar -D

***************************************************************

- ¿Qué comando o comandos utilizaste en el paso 30?
$ git reset --hard head~1
lo hice porque hice un reflog yme dijo que el commit anterior era:
6fbbb51 HEAD@{1}: merge title: Merge made by the 'recursive' strategy.

entonces veo que me equivoque porque en realidad me mando a donde hice la moficacion a mi gusto, y de nuevo veo el reflog y ahora si me voy al ID del commit donde se creo el merge:
$ git reflog
$ git checkout 6fbbb51
Visualizo el archivo y en efecto, es donde yo lo edite a mi gusto, procedo a crear una rama temporal2  
$ git branch temporal2
$ git checkout temporal2
$ git checkout master
$ git merge temporal2
$ git branch -d temporal2
hago el mismo procedimiento de un ejercicio anterior por eso ya no lo explico pero al ultimo borro la rama temporal, yluego checo el archivo y esta con la edicion a mi gusto , esta todo bien.

***************************************************************

- ¿Qué comando o comandos usaste en el paso 32?
$ git reflog
copié el ID del commit (initial)
$ git checkout c5fd280

***************************************************************

- ¿Qué comando o comandos usaste en el punto 33?
$ git checkout 89ebce2
copié el ID del commit donde puse el titulo al poema y lo comprobe con cat y en efecto, el archivo git-nuestro.md esta actualizado a cuando le puse el titulo a mi gusto.

