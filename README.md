# ProyectoMillonario

Repositorio Creado para dejar de estudiar y trbajar.
## Indice 
 
- [Commit inicial](#commitInicial)
- [Push inicial](#pushInicial)
- [Ignorar archivos](#ignorarArchivos)
- [Añadir fichero](#añadirfichero)
- [Crear un tag](#crearTag)
- [Subir el tag](#subirTag)
- [Crear una rama](#crearRama)
- [Añadir Fichero2](#añadirFichero2)
- [Crear rama remota](#crearRama2)
- [Merde directo](#mergeDirecto)
- [Merge con conflicto](#mergeConflicto)
- [Listado de ramas](#listadoRamas)
- [Arreglar conflicto](#arreglarConflicto)
- [Borrrar rama](#borrarRama)
- [listado de cambios](#listadoCambios)

## Clonando el repositorio

<details>
<summary>Comandos</summary>

- git clone

</details>

__Salida__:

```code
git clone git@github.com:adogonz23/ProyectoMillonario.git
Clonando en 'ProyectoMillonario'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Recibiendo objetos: 100% (3/3), listo.
```

<a name="CommitInicial"></a>

## Commit inical

<details>

<summary>Comandos</summary>

- git add .
- git commit -m"aguacate inicial"

</details>

__Salida__:
```code
dam@a108pc01:~/Documentos/ProyectoMillonario$ git commit -m "aguacate inicial"
[main 7181d38] aguacate inicial
 1 file changed, 84 insertions(+), 2 deletions(-)
 rewrite README.md (63%)

```
<a name="pushInicial"></a>

## Push Inicial

Subir los cambios al repositorio remoto.

<details>

<summary>Comandos</summary>

- git push oring master(main)
</details>

__Salida__:
```code
git push origin master
error: src refspec master no concuerda con ninguno
error: falló el empuje de algunas referencias a 'github.com:adogonz23/ProyectoMillonario.git'
dam@a108pc01:~/Documentos/ProyectoMillonario$ git push origin main
Enumerando objetos: 5, listo.
Contando objetos: 100% (5/5), listo.
Compresión delta usando hasta 12 hilos
Comprimiendo objetos: 100% (2/2), listo.
Escribiendo objetos: 100% (3/3), 812 bytes | 812.00 KiB/s, listo.
Total 3 (delta 0), reusados 0 (delta 0), pack-reusados 0
To github.com:adogonz23/ProyectoMillonario.git
   54bc61e..7181d38  main -> main

```
Como he clonado el repositorio y con la creacion de este mismo creee el archivo readme, el paso que me he saltado es el de creear el readme (**touch README.md**)

<a name="ignorarArchivos"></a>

## Ignorar archivos

Crear en el repositorio local un fichero llamado **privado.txt** <br>
Crear en el repositorio local una carpeta llamda **privada**.

<details>

<summary>Comandos</summary>

- touch privado.txt
- mkdir privada
</details>

**Salida:**

```code
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ touch privado.txt
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ mkdir privada
```
Realizar los cambios oportunos para que tanto el archivo como la carpeta sean ignorados por git
<details>

<summary>Comandos</summary>

- echo "privado.txt" >> .gitignore 
- echo "/privada" >> .gitignore
- git add .
- git commit -m "añadiendo el fichero .gitignore"

</details>

**Salida:**

```code
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ echo "privado.txt" >> .gitignore
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ echo "/privada" >> .gitignore
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ git add .
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ git commit -m "añadiendo aguacates ignorados"
[main a55b85c] añadiendo aguacates ignorados
 2 files changed, 5 insertions(+)
 create mode 100644 .gitignore

```

A la pregunta de si el fichero debe subir al repositorio al ejecutar los comando no consigo una respuesta concreta ya que ha hecho 5 nuevas inserciones y a creado el modo gitignore pero no se si al hacer un push los archivos apareceran en el repositorio, mi idea es que no.
<a name="añadirFichero"></a>

## Añadir fichero.txt

Añadir fichero **1.txt** al repositorio local

<details>

<summary>Comandos</summary>

- touch 1.txt
- git add .
- git commit -m"añadiendo 1.txt"

</details>

**Salida**:

```code
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ touch 1.txt
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ git add .
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ git commit -m "añadiendo 1.txt"
[main 0ef0118] añadiendo 1.txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 1.txt

```
los cambias realizados en entorno local los puedo ver el archivo esta creado ahora faltaria ver si se sube al hacer el push.

<a name="crearTag"></a>

## Crear un tag

crer un tag **v01**.

<details>

<summary>Comandos</summary>

- git tag v.01
</details>

**Salida**:


```code
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ git tag v0.1

```
<a name="subirTag"></a>

## Subir el tag 

Subir los cambios al repositorio remoto

<details>

<summary>Comandos</summary>

- git push --tag origin main
</details>

**Salida**:
```code
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ git push --tag origin main
Enumerando objetos: 9, listo.
Contando objetos: 100% (9/9), listo.
Compresión delta usando hasta 4 hilos
Comprimiendo objetos: 100% (5/5), listo.
Escribiendo objetos: 100% (7/7), 798 bytes | 798.00 KiB/s, listo.
Total 7 (delta 1), reusados 0 (delta 0), pack-reusados 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To github.com:adogonz23/ProyectoMillonario.git
   04d8a9b..0ef0118  main -> main
 * [new tag]         v0.1 -> v0.1

```

Los *tag* son como marcas que podremos dejar en nuestro proyecto, las cuales prodemos consultar y nos permiten ver el estado de nuestro proyecto , rama  o donde la hayamos colocado en el repositorio.

<a name="crearRama"></a>

## Crear una rama

Crea un rama **v0.2** <br>
Posiciona tu carpeta de  trabajo en esta rama

<details>

<summary>Comandos</summary>

- git branch v0.2
- gitcheckout v0.2
</details>

**salida**: como no soy muy completo escribi mal el nombre de la rama, pero seguimos trabajando.
```code
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ git branch v.02
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ git checkout v.02
M	README.md
Cambiado a rama 'v.02'

```
<a name="añadirFichero2"></a>

## Añadir fichero  2.txt

Añadir un fichero **2.txt** en la rama v.02
<details>

<summary>Comandos</summary>

- touch *2.txt*
- git add .
- git commit -m "fichero 2" 
</details>

**Salida**:

```code
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ git add .
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ git commit -m"añadiendo archivo 2"
[v.02 8a00f73] añadiendo archivo 2
 2 files changed, 146 insertions(+)
 create mode 100644 2.txt

```
Las ramas sirven principalmente para no trabajar sobre laa rama principal y por algun error carganros el proyecto aunque se pueda restaurar, tambien facilita mucho el trabajo en equipo, se pueden crear diferentes ramas para dividir el trabajo y unificarlo una vez este comprobado y funcinal.

<a name="crearRama2"></a>

## Crear rama remota
 
Subir los cambios al repositorio

<details>

<summary>Comandos</summary>

- git push origin v.02
</details>
 
**Salida**:
```code
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ git push origin v.02
Enumerando objetos: 5, listo.
Contando objetos: 100% (5/5), listo.
Compresión delta usando hasta 4 hilos
Comprimiendo objetos: 100% (3/3), listo.
Escribiendo objetos: 100% (3/3), 2.17 KiB | 2.17 MiB/s, listo.
Total 3 (delta 1), reusados 0 (delta 0), pack-reusados 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'v.02' on GitHub by visiting:
remote:      https://github.com/adogonz23/ProyectoMillonario/pull/new/v.02
remote: 
To github.com:adogonz23/ProyectoMillonario.git
 * [new branch]      v.02 -> v.02

```
<a name="mergeDirecto"></a>

## Merge directo

Posicionarse en la rama main <br>
Hacer un merge de la rama v.02 en la rama main

<details>

<summary>Comandos</summary>

- git checkout main
- git merge v.02 -m "merge v.02 sin conflictos"
</details>

**Salida**:

```code
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ git checkout main
Cambiado a rama 'main'
Tu rama está actualizada con 'origin/main'.
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ git merge v.02 -m"merge sin conflictos"
Actualizando 0ef0118..8a00f73
Fast-forward (no commit created; -m option ignored)
 2.txt     |   0
 README.md | 146 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
 2 files changed, 146 insertions(+)
 create mode 100644 2.txt

```
por lo que yo puedo entender fusiona la rama v.2 con la actual pero al no haber creado un commit la opcion de *-m* la ignora.

<a name="mergeConflicto"></a>

## Merge con conflicto

En la rama main porner *hola* en el fichero **1.txt** y hacer commit
<details>

<summary>Comandos</summary>

- git checkout main
- echo "Hola" >> 1.txt
-  git add .
- git commit -m "hola en 1.txt"
</details>

**Salida**:
```code
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ git checkout main
Ya en 'main'
Tu rama está adelantada a 'origin/main' por 1 commit.
  (usa "git push" para publicar tus commits locales)
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ echo "Hola" >> 1.txt
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ git add .
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ git commit -m "hola en 1.txt"
[main 9ee21af] hola en 1.txt
 1 file changed, 1 insertion(+)
```
Posicionarse en la rama v.02 y poner *adios* en el fichero **1.txt** y hacer el commit

<details>

<summary>Comandos</summary>

- git checkout v.2
- echo "Adios" >> 1.txt
- git add .
- git commit -m "adios en 1.txt"
</details>

**Salida**:
```code
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ git checkout v.02
Cambiado a rama 'v.02'
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ echo "Adios" >> 1.txt
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$  git add .
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ git commit -m "añadiendo adios a 1.txt"
[v.02 62086c5] añadiendo adios a 1.txt
 1 file changed, 1 insertion(+)
```
Posicionarse en la rama main y hacer un merge con la rama v.02
<details>

<summary>Comandos</summary>

- git checkout main
- git merge v.02
- vim 1.txt
- git add .
-  git commit -m "arreglado merge en 1.txt" 
</details>

**Salida**:
```code
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ git checkout main
1.txt: needs merge
error: necesitas resolver tu índice actual primero
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ git merge v.02
error: No es posible hacer merge porque tienes archivos sin fusionar.
ayuda: Corrígelos en el árbol de trabajo y entonces usa 'git add/rm <archivo>',
ayuda: como sea apropiado, para marcar la resolución y realizar un commit.
fatal: Saliendo porque existe un conflicto sin resolver.
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ git add .
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ git commit -m"arreglando el merge"
[main 790f85a] arreglando el merge

```
Al hacer el **vim 1.txt** ese comando me pedia una instalacion, luego de instalarlo volvi probarlo y me salia el contenido del fichero en la rama principal y en el v.2 pero no sabia que hacer dentro de el asi que cerre el terminal y ejecute los comandos de nuevo sin el **vim**

<a name="listadoRamas"></a>

## Listado de ramas

listar ramas con merge y las ramas sin merge ( **listado de ramas fusionadas y sin fusionar**)

<details>

<summary>Comandos</summary>

- git branch --merged
- git branch --no-merged
</details>

**Salida**:
```code
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ git branch --merged
* main
  v.02
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ git branch --no-merged

```
Como podemos observar no tengo nada listado en *no-mergerd* eso quiere decir que por ahora esta todo bien hecho.
<a name="arreglarConflicto"></a>

## Areglar conflicto

Es un paso que ya hicimos anteriormente, asi que solo pondremos los comados utilizados.

<details>

<summary>Comandos</summary>

- vim 1.txt
- git add .
- git comit -m"mensaje"
</details> 

**Salida**: No queria cargarme la tarea asi que no toque nada 

```code
E325: ATENCIÓN
Se ha encontrado un archivo de intercambio con el nombre ".1.txt.swp"
          propiedad de: adonay   de fecha: mié oct 11 14:23:18 2023
         nombre del archivo: ~adonay/Documentos/ProyectoMillonario/1.txt
         modificado: SI
 nombre del usuario: adonay  nombre del servidor: adonay-VirtualBox
      ID del proceso: 4590
al abrir el archivo "1.txt"
             de fecha: mié oct 11 14:20:15 2023

(1) Puede que otro programa esté editando el mismo archivo. De ser así,
    tenga cuidado de no acabar con dos ejemplares diferentes del mismo
    archivo al hacer cambios. Salga del programa o continúe con precaución.
(2) Falló una sesión de edición de este archivo.
    Si es así, use ":recover" o "vim -r 1.txt"
    para recuperar los cambios (véa ":help recovery").
    Si Ud. ya ha hecho esto, borre el archivo de intercambio ".1.txt.swp"
    para evitar este mensaje.

¡El archivo de intercambio ".1.txt.swp" ya existe!
[A]brir para lectura únicamente, (E)ditar de todas formas, (R)ecuperar, (B)orrar
, (S)alir, (A)bortar: 
```
Opcion mas segura "Salir"

<a name=""></a>

## borrar rama

crear un  tag **v.02** <br>
borrar la raa **v.02**
<details>

<summary>Comandos</summary>

- git tag v.02
- git branch -d v.2
</details>

**Salida**
```code
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ git tag v.02
adonay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ git branch -d v.02
Eliminada la rama v.02 (era 62086c5).
```
<a name="listadoCabios"></a>

## Listado de cambios

Lista los distintos cambios con sus ras y tags

<details>

<summary>Comandos</summary>

- git config --global alis.list 'log --oneline --decorate --graph --al'
- git list (git list no me fubncionaba) use *git log*

</details>

**Salida**:
```code
donay@adonay-VirtualBox:~/Documentos/ProyectoMillonario$ git log
commit 790f85ab1c492f5a1bbde7328d88bb3aabbe816e (HEAD -> main, tag: v.02)
Merge: 9ee21af 62086c5
Author: adogonz23 <adogonzalez75@gmail.com>
Date:   Wed Oct 11 14:24:32 2023 +0100

    arreglando el merge

commit 62086c500cbde324515b3362d51f2e968f592148
Author: adogonz23 <adogonzalez75@gmail.com>
Date:   Wed Oct 11 14:17:06 2023 +0100

    añadiendo adios a 1.txt

commit 9ee21af1950dff0fff0475aa38f7449f750ebda9
Author: adogonz23 <adogonzalez75@gmail.com>
Date:   Wed Oct 11 14:12:49 2023 +0100

    hola en 1.txt

commit 8a00f7325affe24cd7b97ce87936d2c5ce510c46 (origin/v.02)
Author: adogonz23 <adogonzalez75@gmail.com>
Date:   Wed Oct 11 13:48:49 2023 +0100

:Wed Oct 11 13:48:49 2023 +0100

    añadiendo archivo 2

commit 0ef0118c4a108c7fa6af0215bef0a1d205bea211 (tag: v0.1, origin/main, origin/HEAD)
Author: adogonz23 <adogonzalez75@gmail.com>
Date:   Wed Oct 11 13:24:13 2023 +0100

    añadiendo 1.txt

commit a55b85c153c9a9dfc0ff3d7ba221407028328c83
Author: adogonz23 <adogonzalez75@gmail.com>
Date:   Wed Oct 11 13:15:17 2023 +0100

    añadiendo aguacates ignorados

commit 04d8a9b8b7ef564525e58a53bacc28f278486f17
Author: adogonz23 <adogonzalez75@gmail.com>
Date:   Tue Oct 10 15:28:42 2023 +0100

    a

commit 7181d3850eb24df4e8dcba32423dfa2985437422
Author: adogonz23 <adogonzalez75@gmail.com>
Date:   Tue Oct 10 15:19:39 2023 +0100

    aguacate inicial

commit 54bc61e64ec2f691d07365c9135e374b2e3b7132
Author: adogonz23 <145137932+adogonz23@users.noreply.github.com>
Date:   Tue Oct 10 14:57:26 2023 +0100

    Initial commit
(END)


```
Con cada enter pulsado me iba mostrando cambios mas  antiguos

Fin de tarea