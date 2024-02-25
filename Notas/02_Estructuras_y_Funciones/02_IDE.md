[Contenidos](../Contenidos.md) \| [Anterior (1 Introducción y repaso)](01_Introduccion_y_repaso.md) \| [Próximo (3 Manejo de archivos)](03_Archivos.md)

# 2.2 Entorno de desarrollo integrado

A partir de aquí te vamos a proponer trabajar principalmente dentro de un entorno de desarrollo integrado (IDE, por sus siglas en inglés). 

En este curso vamos a trabajar usando [VS Code](https://code.visualstudio.com/) (Visual Studio Code), aunque podés usar el que más te guste. Otro IDE muy utilizado es [Spyder](https://www.spyder-ide.org/), pero en todos los ejemplos que veamos vamos a usar VS Code.

Te dejamos un [video](https://www.youtube.com/watch?v=nllg_MCZm6I) para que sepas cómo utilizar el VS Code.

## Extensiones de VS Code

Vamos a listar algunas de las extensiones que vas a precisar y otras que son opcionales pero que ayudan muchísimo:

1. **Python Extension Pack - (Author: Don jayamanne):** esta extensión agrega muchos plugins útiles para Python.
2. **Code Runner - (Author: Jun Han):** esta extensión agrega un icono arriba a la derecha para poder correr python fácilmente.
3. **Error Lens - (Author: Alexander):** esta extensión te permite ver errores en tiempo real. Puede ser un poco molesta, si no te gusta la podes deshabilitar/desinstalar.
4. **autopep8 - (Author: Microsoft):** esta extensión te permite formatear tu script según la convención PEP 8 que es una guía de estilo.
5. **indent-rainbow - (Author: oderwat):** esta extensión agrega colores a las indentaciones, así se identifican más fácilmente.
6. **Indent one space - (Author: Alexander):** Visual Studio no permite por defecto indentar a un espacio hacia atras. Para poder hacerlo existe esta extensión. Seleccionamos código y tocamos Shift + Barra espaciadora para usarlo.
7. **Jupyter - (Author: Microsoft):** Si queremos usar bloques de código como en las Jupyer Notebooks o Google Colab, podemos descargar esta extensión.

## Configuraciones muy útiles:

1. **Formatear tu código al guardar:** esta configuración te permite que cuando guardes tu código se formatee según la convención PEP 8. Para activar esta opción primero tenes que bajarte un formateador como "autopep8" (hay muchos), luego ir a configuración y en la barra de búsqueda de configuraciones escribí: Format On Save, y tickeá la opción que aparece.  
![format on save](/Notas/02_Estructuras_y_Funciones/img/format_on_save.png)

2. **Guardar al ejecutar el código:** esta configuración permite guardar el script automáticamente al ejecutarlo. **Solo está disponible si tenés la extensión de Code Runner**. Para activarla tenés que ir a configuración y en la barra de búsqueda de configuraciones escribí: Code-runner: Save File Before Run.  
![save file before run](/Notas/02_Estructuras_y_Funciones/img/save_file_before_run.png)

3. **Abrir código en terminal:** esta configuración es propia de la extensión Code Runner. A veces cuando clickeamos en el icono para correr el código nos aparece solo el output del código y no la terminal, lo cual puede ser molesto para hacer algunas operaciones como input() o interrumpir la ejecución de código con Ctrl + C (haciendo un KeyboardInterrumpt). Para solucionar esto buscamos la opción "Code-runner: Run In Terminal" y la tickeamos.  
![run in terminal](/Notas/02_Estructuras_y_Funciones/img/run_in_terminal.png)

## Atajos de teclado

Estos son algunos atajos de teclado útiles que les pueden servir para agilizar la programación. Si alguna de estas funciones no hace lo que corresponde, tienen que modificar dicha función en File > Preferences > Keyboard Shortcuts. Ahí pueden buscar por descripción del comando o por teclas asociadas.

- **Alt + Z:** esto nos permite ajustar el código a la ventana. A veces sucede que tenemos un choclo de código y no queremos usar la barra lateral para andar moviéndonos de izquierda a derecha y viceversa. Entonces podemos usar este atajo para poder ajustar el código a la ventana.

- **Ctrl + K + C:** este atajo nos permite comentar varias líneas de código al mismo tiempo. Y si las queremos descomentar tocamos **Ctrl + K + U**

- Para indentar código hacia la derecha con tabulaciones podemos seleccionar todo el código que queramos y tocar **tabulación**. Y si quisieramos indentar hacia la izquierda tocamos **Shift + Tabulación**.

- Si quisieramos indentar de a 1 espacio a la vez tenemos que tener instalada la extensión de indent one space que mencionamos antes. Y es lo mismo que con la tabulación solo que con la barra espaciadora: seleccionamos el código y tocamos **espacio** para indentar hacia la derecha y **shift + espacio** para indentar hacia la izquierda.

- Si mantenemos **Alt** podemos correr lineas de codigo hacia arriba o abajo con las flechas.

- Si mantenemos **Alt + Shift** y tocamos la flecha hacia abajo podemos duplicar las lineas.

- Otro atajo para seleccionar líneas de código con cierto patrón de caracteres es **Ctrl + D**. Lo que va a hacer esto es colocar **cursores**. Por ejemplo, imaginemos que tenemos varios print() en nuestro código que queremos seleccionar para comentarlos. En vez de hacerlo manualmente, podemos pintar la palabra print() tocar **Ctrl + D** varias veces hasta que se posicionen cursores y luego podemos comentar esas líneas con **Ctrl + K + C**.


[Contenidos](../Contenidos.md) \| [Anterior (1 Introducción y repaso)](01_Introduccion_y_repaso.md) \| [Próximo (3 Manejo de archivos)](03_Archivos.md)

