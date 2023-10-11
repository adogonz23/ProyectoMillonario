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













<a name=""></a>


<details>

<summary>Comandos</summary>

</details>