# El directorio raíz "/" (root directory):

En sistemas operativos basados en Linux, como Ubuntu, Debian, CentOS y otros, el "directorio raíz" (root directory) es el punto de partida fundamental de la jerarquía del sistema de archivos. Es el nivel más alto en la estructura de directorios y contiene todos los demás directorios y archivos del sistema. Se identifica por el símbolo "/", y se referencia como "/".

# Abrir Terminal:

`Ctrl + Alt + T`: Este atajo suele funcionar en la mayoría de los entornos de escritorio de Ubuntu y abre una nueva ventana de terminal.

# Comandos:
 
 1. ### Comando "mkdir" en Linux: Crear Directorios. 

 El comando "mkdir" (abreviatura de "make directory") en sistemas Linux es utilizado para crear uno o varios directorios nuevos en una ubicación específica del sistema de archivos. Este comando es útil para organizar archivos y facilitar la estructura de carpetas.

 Su sintaxis básica es la siguiente:

```bash
mkdir  nombre_del_directorio
```

2. ### Comando "cd" en Linux: Cambio de Directorio.

El comando "cd" (Change Directory) en sistemas Linux permite a los usuarios cambiar de ubicación en la jerarquía de directorios. Es una herramienta fundamental para navegar entre carpetas y acceder a ubicaciones específicas en la línea de comandos.

 Su sintaxis es simple:
 ```bash
cd [ruta]
```
* Cambiar a un directorio específico: **cd Documentos**
* Regresar al directorio anterior: **cd ..**
* Ir al directorio personal del usuario: **cd ~**

3. ### Comando "touch" en Linux: Creación de Archivos.

El comando "touch" en sistemas Linux se utiliza para crear archivos vacíos o actualizar las marcas de tiempo de archivos existentes. Aunque su nombre implica "tocar" archivos, su funcionalidad principal es la creación y gestión de archivos.

Su sintaxis es simple:
```bash
touch nombre_del_archivo
```
Crear un archivo vacío: `touch archivo.txt`

4. ### Comando "ls" en Linux: Listar Contenido de Directorios.

El comando "ls" en sistemas Linux es utilizado para listar y mostrar el contenido de un directorio específico en la terminal. Proporciona información sobre archivos y subdirectorios, incluyendo nombres, permisos, tamaños y marcas de tiempo.

 Su sintaxis básica es:

 ```bash
 ls
 ```
 Opciones:
 * Listar archivos con detalles (formato largo): 
 ```bash
 ls -l
 ```

 5. ### Comando "cp" en Linux: Copiar Archivos y Directorios.

El comando "cp" es esencial para duplicar archivos y directorios en Linux. Puede usarse con diferentes opciones para personalizar el proceso de copia y asegurarse de que los archivos se mantengan organizados y respaldados en el sistema.

Su sintaxis básica es:

```bash
cp  origen destino
```
* Copiar  archivos a un mismo directorio: 
```bash
`cp archivo1.txt archivo2.txt`
```
*en este ejemplo archivo origen esta en el mismo directorio que el destiono.*

* Copiar un archivo a otro lugar: `cp archivo.txt /ruta/destino`

```bash
cp archivo2.txt carpeta2
```
* Copiar un archivo a otro lugar con otro nombre:

```bash
cp archivo2.txt carpeta2/archivoDos.txt
```
*  Copiar el archivo desde el directorio actual al directorio padre (nivel superior) utilizando ../ para indicar el directorio padre.
```bash
cp miDocu.txt ..
```


6. ### Comando "cat" en Linux: Visualización de Contenido de Archivos.

El comando "cat" en sistemas Linux se utiliza para mostrar el contenido de uno o varios archivos en la terminal. Es una herramienta simple pero útil para examinar y visualizar el texto y contenido de los archivos.

Su sintaxis básica es:

```bash
cat archivo(s)
```

* Mostrar el contenido de un archivo: `cat archivo.txt` 
* Mostrar el contenido de varios archivos: `cat archivo1.txt archivo2.txt` 

7. ### Comando "mv" en Linux: Mover y Renombrar Archivos y Directorios.

El comando "mv" en sistemas Linux se utiliza para mover o renombrar archivos y directorios de una ubicación a otra. Además de cambiar la ubicación, es útil para cambiar el nombre de archivos y directorios.

 Su sintaxis básica es:
 ```bash
 mv  origen destino
 ```
 * Cambiar el nombre de un directorio: `mv antiguo_nombre nuevo_nombre`

 * Mover el archivo  desde el directorio actual al directorio padre (nivel superior) sin cambiar su nombre. 

 ```bash
  mv archivo.txt ..
```

 7. ### Comando "rm" en Linux: Eliminación de Archivos y Directorios.

 El comando "rm" en sistemas Linux se utiliza para eliminar archivos y directorios. Es una herramienta poderosa para eliminar contenido del sistema de archivos, pero debe usarse con precaución ya que los archivos eliminados no se envían a la Papelera y se borran de manera permanente.

  Su sintaxis básica es:

  ```bash
  rm archivo(s) o directorio(s)
  ```

  * Eliminar un archivo: `rm archivo.txt`.
  * Eliminar todos  archivos cuyos nombres comiencen con "archivo" : `rm archivo*`
  * Eliminar un directorio y su contenido:`rm -r carpeta` 

  8. ### Comando "pwd" en Linux: Mostrar Directorio Actual.

  El comando "pwd" en sistemas Linux se utiliza para mostrar el directorio de trabajo actual en la terminal. Proporciona la ruta completa del directorio en el que te encuentras ubicado en ese momento.

  Su sintaxis es simple:

 ```bash
  pwd
  ```
  Si el directorio actual es "/home/usuario/documentos", el comando pwd mostrará: `/home/usuario/documentos`



