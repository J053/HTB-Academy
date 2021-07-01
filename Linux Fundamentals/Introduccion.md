# Estructura de Linux

### Historia

Muchos eventos condujeron a la creacion del primer nucleo de Linux y, en ultima instancia, del sistema operativo (SO) Linux, comenzando con el lanzamiento del sistema operativo Unix por Ken Thompson y Dennis Ritchie (quienes trabajaban para AT&T en ese momento) en 1970. La Berkeley Software Distribution (BSD) fue lanzada en 1977, pero como contenia el codigo de Unix propiedad de AT&T, un pleito resultante limito el desarrollo de BSD. Richard Stallman inicio el proyecto GNU en 1983. Su objetivo era crear un sistema operativo libre similiar a Unix, y parte de su trabajo dio lugar a la creacion de la Licencia Publica General de GNU (GPL). Los proyectos realizados por otros a lo largo del tiempo no lograron dar como resultado un nucleo libre que funcionara y fuera ampliamente adoptado hasta la creacion del nucleo Linux.

Al principio, Linux era un proyecto personal iniciado en 1991 por un estudiante finlandes llamado Linus Torvalds. Su objetivo era crear un nuevo nucleo del sistema operativo libre. A lo largo del tiempo, el nucleo de Linux ha pasado de ser un corto numero de archivos escritos en C bajo una licencia que prohibia su distribucion comercial a la ultima version con mas de 23 millones de lineas de codigo fuente (sin incluir los comentarios), con licencia de la Licencia Publica General GNU v2.

Linux esta disponible en mas de 600 distribuciones (o un sistema operativo basado en el nucleo de Linux y el software y las bibliotecas de apoyo). Algunas de las mas populares y conocidas son Ubuntu, Debian, Fedora, OpenSUSE, elemental, Manjaro, Gentoo Linux, RedHat y Linux Mint.

En general, Linux se considera mas seguro que otros sistemas operativos y, aunque en el pasado ha tenido muchas vulnerabilidades en el nucleo, cada vez son menos frecuentes. En menos susceptible al malware que los sistemas operativos Windows y se actualiza con mucha frecuencia. Linux tambien es muy estable y, por lo general, ofrece un rendimiento muy alto al usuario final. Sin embargo, puede ser mas dificil para los participantes y no tiene tantos controladores de hardware como Windows.

Como Linux es gratuito y de codigo abierto, el codigo fuente puede ser modificado y distribuido comercialmente o no por cualquiera. Los sistemas operativos basados en Linux se ejecutan en servidores, ordenadores centrales, ordenadores de sobremesa, sistemas integrados como routers, televisores, consolas de videojuegos, etc. El sistema operativo general de Android que se ejecuta en los telefonos inteligentes y las tabletas se basa en el nucleo de Linux y, por ello, Linux es el sistema operativo mas ampliamente instalado.

Linux es un sistema operativo como Windows, iOS, Android o macOS. Un SO es un software que gestiona todos los recursos de hardware asociados a nuestro ordenador. Eso significa que un SO gestiona toda la comunicacion entre el software y el hardware. Ademas, existen muchas distribuciones diferentes (distro). Es como una version de los sistemas operativos Windows.

Con las instancias interactivas, tenemos acceso a la Pwnbox, una version personalizada de Parrot OS. Este sera el sistema operativo principal con el que trabajaremos a travez de los modulos. Parrot OS es una distribucion de Linux basada en Debian que se centra en la seguridad, la privacidad y el desarrollo. 

### Filosofia

Linux sigue cinco principios basicos:


| Principio  | Descripcion |
| ----------- | ----------- |
| Todo es un archivo | Todos los archivos de configuracion de los distintos servicios que se ejecutan en el sistema operativo Linux se almacenan en uno o varios archivos de texto.
| Programas cortos de un solo proposito | Linux ofrece muchas herramientas con las que trabajaremos, que pueden combinarse para trabajar juntas |
| Capacidad de encadenar programas para realizar tareas complejas | La integracion y combinacion de diferentes herramientas nos permite realizar muchas tareas de gran envergadura y complejidad, como el procesamiento o filtrado de resultados de datos especificos. |
| Evitar las interfaces de usuario cautivas | Linux esta elaborado parar trabajar principalmente con el interprete de comandos (o terminal), que ofrece al usuario un mayor control sobre el sistema operativo. |
| Datos de configuracion almacenados en un archivo de texto | Un ejemplo de este tipo de archivos es el archivo **/etc/passwd** que almacena todos los usuarios registrados en el sistema. |

### Componentes

| Componente | Descripcion |
| ---------- | ----------- |
| Bootloader | Una pieza de codigo que se ejecuta para guiar el proceso de arranque para iniciar el sistema operativo. Parrot Linux utiliza el gestor de arranque GRUB. |
| OS Kernel  | El nucleo es el componente principal de un sistema operativo. Gestiona los recursos de los dispositivos de E/S del sistema a nivel de hardware. |
| Daemons    | Los servicios en segundo plano se llaman "demonios" en Linux. Su proposito es asegurar que las funciones clave como la programacion, la impresion y el multimedia funcionen correctamente. Estos cortos programas se cargan despues de arrancar o iniciar sesion en el ordenador. |
| OS Shell   | El shell del sistema operativo o el interprete del lenguaje de comandos (tambien conocido como linea de comandos) es la interfaz entre el SO y el usuario. Esta interfaz permite al usuario decirle al SO lo que debe hacer. Los shells mas utilizados son Bash, Tcsh/Csh, Ksh, Zsh y Fish. |
| Graphics server | Esto proporciona un subsistema grafico (servidor) llamado "X" o "servidor X" que permite que los programas graficos se ejecuten local o remotamente en el sistema X-windowing. |
| Window Manager  | Tambien se conoce como interfaz grafica de usuario (GUI). Hay muchas opciones, como GNOME, KDE, MATE, Unity y Cinnamon. Un entorno de escritorio suele tener varias aplicaciones, entre ellas los navegadores de archivos y de Internet. Estas permiten al usuario acceder y gestionar las caracteristicas y servicios esenciales y de acceso frecuente de un sistema operativo. |
| Utilities  | Las aplicaciones o utilidades son programas que realizan funciones particulares para el usuario o para otro programa. |

### Arquitectura  de Linux

El sistema operativo Linux puede dividirse en capas:

| Capa | Descripcion |
|------|-------------|
| Hardware | Dispositivos perifericos como la memoria RAM del sistema, el disco duro, la CPU y otros. |
| Kernel | El nucleo del sistema opeartivo Linux cuya funcion es virtualizar y controlar los recursos comunes del hardware del ordenador como la CPU, la memoria asignada, los datos a los que accede y otros. El kernel otorga a cada proceso sus propios recursos virtuales y previene/mitiga los conflictos entre diferentes procesos. |
| Shell | Una interfaz de linea de comandos (CLI), tambien conocida como shell en la que un usuario puede introducir comandos para ejecutar las funciones del kernel. |
| System Utility | Pone a disposicion del usuario toda la funcionalidad del sistema operativo. |

### Jerarquia del sistema de archivos

El sistema operativo Linux esta estructurado en una jerarquia en forma de arbol y esta documentado en el estandar de [**jerarquia del sistema de archivos (FHS).**](https://www.pathname.com/fhs/) Linux esta estructurado con los siguientes directorios estandar de nivel superior:

![Filesystem Hierarchy Standard](https://academy.hackthebox.eu/storage/modules/18/NEW_filesystem.png)

| Ruta | Descripcion |
|------|-------------|
| / | El directorio de nivel superior es el sistema de archivos raiz y contiene todos los archivos necesarios para arrancar el sistema operativo antes de montar otros sistemas de archivos, asi como los archivos necesarios para arrancar los otros sistemas de archivos. Tras el arranque, todos los demas sistemas de archivos se montan en puntos de montaje estandar como subdirectorios de la raiz. |


















































