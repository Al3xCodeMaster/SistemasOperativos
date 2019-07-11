# Lenguaje C - SHELL

Se realizo una shell con la cual se buscaba poner en contexto los conocimientos adquiridos en clase sobre las llamadas al sistema (API CALLS).


## Desarrollo del programa:

Se desarrollaron tres archivos:

* [shell.c](shell.c)
* [shell_utils.c](shell_utils.c)
* [shell_utils.h](shell_utils.h)

Para compilar el programa se llevan a cabo los siguientes pasos:

* Generar la librería
```
gcc -c shell_utils.c -o shell_utils.o
ar rcs shell_utils.a shell_utils.o
```

* En el paso anterior se generó el archivo `libfun.a`. Ahora enlazaremos el programa `basico.c` con la librería `libfun.a`.

``
# Lenguaje C - 101

En esta clase se hizo una revisión muy rápida de un programa sencillo en C que imprime el mensaje `hola mundo`. 
Después se mostró la forma como se genera una librería de enlace estático y como la funcionalidad implementada


## Desarrollo del programa:

Se desarrollaron tres archivos:

* [basico.c](basico.c)
* [libfun.c](libfun.c)
* [libfun.h](libfun.h)

Para compilar el programa se llevan a cabo los siguientes pasos:

* Generar la librería

```
gcc -c shell_utils.c -o shell_utils.o
ar rcs shell_utils.a shell_utils.o
```

* En el paso anterior se generó el archivo `shell_utils.a`. Ahora enlazaremos el programa `shell.c` con la librería `shell_utils.a`.

```
gcc shell.c -L. -l:shell_utils.a -o shell
```

* Finalmente, el programa se ejecuta:

```
./shell
```
