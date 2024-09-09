#Minishell 🐚

Este es un proyecto desarrollado en el marco del programa de 42 Barcelona. La meta fue crear una pequeña réplica de la shell de Linux, utilizando el lenguaje de programación C, y manejando procesos para la ejecución de los comandos. El proyecto simula muchas de las funcionalidades básicas de la terminal, incluyendo pipes, redirecciones y comandos built-in.

#Características del proyecto 🚀

Nuestra implementación de Minishell incluye las siguientes funcionalidades clave:

- Tokenización, Expansión y Parseo de comandos para su correcta ejecución.
- Historial funcional de comandos.
- Ejecución de comandos mediante la búsqueda del ejecutable en `$PATH`, o usando rutas relativas/absolutas.
- Redirecciones de entrada y salida:
  - `<` redirige el input.
  - `>` redirige el output.
  - `<<` recibe un delimitador para input hasta que aparezca el delimitador.
  - `>>` redirige el output en modo append.
- Pipes (`|`) para conectar el output de un comando al input de otro.
- Gestión de variables de entorno y el estado de salida (`$?`).
- Manejo de combinaciones de teclas ctrl-C, ctrl-D y *ctrl-* como en bash.
- Comandos built-in implementados:
  - `echo` (con opción `-n`)
  - `cd`
  - `pwd`
  - `export`
  - `unset`
  - `env`
  - `exit`

#Requisitos 📋

Para ejecutar este proyecto necesitas tener instalado:

  - GCC o cualquier compilador de C compatible.
  - GNU Make para compilar con el Makefile.
  - Sistema operativo basado en Unix.

#Instalación y Uso 💻

Clona este repositorio:
~~~
git clone https://github.com/tuusuario/minishell.git
cd minishell
~~~
Compila el proyecto usando el Makefile:

`make`

Ejecuta la shell:

`./minishell`

Para limpiar los archivos compilados:

`make fclean`

#Uso de comandos 📝

Puedes utilizar comandos comunes como ls, pwd, cd, así como los built-ins implementados.
Soporte para variables de entorno como `$USER` y `$?`.
Soporte para redirecciones (`>`, `<`, `>>`, `<<`) y pipes (`|`).

Ejemplo de uso:

`ls -l | grep minishell > output.txt`

#Créditos 👥

Este proyecto fue desarrollado en conjunto por:

  Camilo Andres Garatejo Moreno
  Xavier Roca Pérez

#Recursos adicionales 📚

Si te interesa saber más sobre cómo funciona una shell o cómo fue implementada, te dejo algunos recursos útiles:

    Documentación sobre shells en Linux
    Referencia en C
