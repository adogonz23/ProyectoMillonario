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
- [Crear rama remota](#crearRama)
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












<a name=""></a>


<details>

<summary>Comandos</summary>

</details>