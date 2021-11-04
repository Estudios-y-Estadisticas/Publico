# Instrucciones de Uso

Bienvenido al sistema de documentación del departamento de Estudios y Estadísticas. Aquí se detallan los diversos procesos que se ejecutan en el departamento.

## Funcionamiento

El sistema funciona de la siguiente forma:

### Github

Se usa github como plataforma informática para el almacenamiento de la documentación, esto tiene diversas ventajas respecto de un sistema basado en carpetas compartidas y archivos de Word u otros formatos.

- La visualización en Github es mediante un navegador Web
- Cada persona debe tener un usuario para conectarse y ver el contenido (seguridad)
- Cada persona al editar documentos registra su usuario y hora con los cambios
- Se puede volver a versiones antiguas de un documento en cualquier momento y ver las modificaciones que cada usuario haga

También tiene algunas desventajas

- Es un sistema que requiere de varios pasos estrictos para que funcione
- Requiere de aprender una nueva tecnología y el uso de 2 programas.



## Instrucciones de uso

Para poder utilizar el sistema se deben seguir los siguientes pasos.

### Paso 1: Crear una cuenta en GitHub

Ir a [github.com/](https://github.com/) y hacer clic en **Sign Up**, seguir los pasos. Una vez completado enviar el nombre de usuario a [estadisticas@fonasa.cl](#)

Por ejemplo la cuenta en dónde se aloja la documentación es [https://github.com/Estudios-y-Estadisticas](https://github.com/Estudios-y-Estadisticas) en dónde el nombre de usuario es:

```
Estudios-y-Estadísticas
```

### Paso 2: Instalar Github Desktop

Es necesario instalar este programa en el computador del usuario para que descargue una copia completa del repositorio que contiene la documentación. Se puede encontrar en:

[https://desktop.github.com/](https://desktop.github.com/)

Una vez instalado hay que registrar nuestra cuenta en el programa, se puede hacer en `Archivo > Opciones`

![image-20211103161851945](img/image-20211103161851945.png)

Con el botón **Sign In**

![image-20211103162005123](img/image-20211103162005123.png)

Esto nos devuelve al navegador web para introducir las credenciales de la cuenta.

### Paso 3: Clonar el repositorio

Luego que ya estamos aceptados como colaboradores en el repositorio de la documentación podemos clonarlo en nuestro computador. Esto lo hacemos en github desktop

![image-20211103162653982](img/image-20211103162653982.png)



Tenemos que clonar desde la URL https://github.com/Estudios-y-Estadisticas/Documentacion

![image-20211103163027959](img/image-20211103163027959.png)

Si vamos a la carpeta `"C:\Users\orojas\Documents\Documentacion"` (en mi caso) veremos que github desktop clonó todo el contenido.

### Paso 4: Editar o crear documentación

> Antes de crear o editar un archivo del repositorio tenemos que abrir el programa **github desktop** que es el encargado de llevar los controles de versión o cambios realizados a los documentos.

Si bien un repositorio puede almacenar cualquier tipo de archivo, los cambios sólo se registran en archivos de tipo texto, no es necesario que tengan la extensión `.txt` sino que puede ser un script de R, Python, SQL, etc. todos los cuales se almacenan como texto, pero con una extensión diferente a `.txt`.

#### Markdown

La documentación en este sistema será Markdown, que corresponde a archivos de texto plano que tienen un formato interno que permite visualizar como si fuera un archivo de Word.

> **Markdown** es un [lenguaje de marcado ligero](https://es.wikipedia.org/wiki/Lenguajes_de_marcas_ligeros) creado por [John Gruber](https://es.wikipedia.org/w/index.php?title=John_Gruber&action=edit&redlink=1) que trata de conseguir la máxima legibilidad y facilidad de publicación tanto en su forma de entrada como de salida, inspirándose en muchas  convenciones existentes para marcar mensajes de correo electrónico  usando texto plano [Wikipedia

Por ejemplo en Markdown para hacer las negritas se debe escribir doble asterisco alrededor de la palabra: `**negrita**` que se verá asói: **Negrita**

No es necesario escribir todas las veces los asteriscos porque el programa que usaremos permite muchos atajos del teclado o con su interfaz.

#### Typora

Para editar documentos usaremos Typora, que se puede encontrar en [https://typora.io](https://typora.io#download) hay que descargar e instalar.

Antes de comenzar a editar documentos vamos a configurar algo muy importante relativo a las imágenes. Cuando peguemos una imagen en markdown no se guarda junto al archivo como un Word, sino que se almacena en un archivo y se accede a la imagen. Typora lo hace automático y hay que configurar algo para que así sea.

![image-20211103164314792](img/image-20211103164314792.png)

Vamos a `Archivo > Preferencias...` tendremos que dejar la configuración tal cual se ve:

![image-20211103164422203](img/image-20211103164422203.png)

Esto permite que al existir un documento de markdown en un el disco, Typora automáticamente creará la carpeta `./img` y guardará en ese lugar las imágenes que se peguen al documento y las dejará enlazadas.

### Paso 5: Commit y Push

Ahora que ya creamos o editamos un documento en Markdown hay que subirlo a github. Cuando editemos veremos que esos cambios se registran en **github desktop** con color rojo y con verde las adiciones.

También indica si se agregaron archivos se modificaron en la barra latera.

![image-20211103165229624](img/image-20211103165229624.png)

Si ya estamos listos es hora de ejecutar los procedimientos de control de cambios.

#### Commit

Este paso se realiza abajo a la izquierda y consiste en crear un **Título** y un **Comentario** sobre las modificaciones realizadas. Si la edición es pequeña basta con escribir `actualización` o algo así. Pero si son cambios grandes conviene dejar algún detalle.

![image-20211103165520914](img/image-20211103165520914.png)

Al hacer el commit, github desktop archivará la existencia de las modificaciones realizadas

#### Push

Lo siguiente es enviar nuestro Commit a la linea de edición que existe en el tiempo, basta con apretar el siguiente botón en Github desktop

![image-20211103165915161](img/image-20211103165915161.png)

Finalmente si ya no quedan cambios a registrar tendremos que hacer el push a la linea de edició que está en GitHub, en la nube

![image-20211103170041121](img/image-20211103170041121.png)

Basta con hacer clic en **Push origin**. Ya en la página de Github podremos acceder a las versiones antiguas seleccionando por **Commit**

![image-20211103170344664](img/image-20211103170344664.png)

