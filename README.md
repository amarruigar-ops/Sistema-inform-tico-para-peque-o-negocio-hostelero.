# Anteproyecto

**Proyecto intermodular de Administración de Sistemas informáticos en Red**

Ciclo Formativo de Grado Superior

**Técnico Superior en Administración de Sistemas Informáticos en Red**

Curso 26/27

**Autor:** Marcos Ruiz García

---

## Índice

- [Introducción](#introducción)
- [1. Título](#título)
- [2. Descripción](#descripción)
- [3. Justificación](#justificación)
- [4. Objetivos](#objetivos)
- [5. Lenguajes de programación y tecnologías](#lenguajes-de-programación-y-tecnologías)
- [6. Prototipo de interfaz de usuario](#prototipo-de-interfaz-de-usuario)
- [7. Gestor de base de datos](#gestor-de-base-de-datos)
- [8. Entornos de aplicación del proyecto](#entornos-de-aplicación-del-proyecto)
- [9. Fases de desarrollo](#fases-de-desarrollo)
- [10. Módulos del ciclo formativo relacionados](#módulos-del-ciclo-formativo-relacionados)
- [11. Anexos y bibliografías](#anexos-y-bibliografía)

---

## Introducción

En este proyecto voy a diseñar un sistema informático(base de datos,aplicación y página web,red,servidor)para el pequeño bar en el que trabajo.Así puedo conseguir optimizar el trabajo.

## Título

Sistema de gestión para pequeños negocios hosteleros

## Descripción

Mi proyecto va a consistir en realizar una aplicación web para el bar en el que trabajo,pudiendo servir esta también para diversos comercios de hostelería.Está enfocada para pequeños comercios/negocios.Los clientes, a través del navegador acceden a ella y puedan hacer consultas, hacer reservas,pedidos(ya sea a domicilio,recoger o en el propio bar).Los trabajadores ,dueño podrán gestionar el stock a través de esta.

Si un producto se ha acabado, un trabajador accede a la aplicación ,lo indica y esta no deja pedir más de ese producto.Los clientes podrán iniciar sesión si lo desean y sus datos quedarán guardados en una base de datos.Estos podrán ver también la carta, las redes sociales, el número de teléfono…Este no engloba pagos reales,solo simulados ni pedidos a proveedores.

## Justificación

El bar en el cual trabajo es un negocio humilde sin muchos recursos económicos.Muchas veces, por no tener un buen sistema, los clientes piden productos agotados, ya que los trabajadores no tenemos conocimientos muchas veces de qué productos se encuentran agotados.

Las reservas, al cogerlas en papel, se sobreponen unas con otras o no está claro de qué mesa es cada cliente.Quitan tiempo de trabajo a quien tiene que atenderlas.Con este software las reservas las hará el propio el cliente, el propio programa dirá qué mesas están disponibles y cuales no.

Los pedidos , al tener que atender al cliente , quitan tiempo de estar haciendo otras tareas, haciendo que los clientes que se encuentran en el establecimiento lleguen a quejarse por la tardanza. Los pedidos también quitan tiempo de trabajo, por lo que el programa permite que estos los hagan los clientes, optimizando así el trabajo de los empleados.

El stock está acostumbrado a hacerse manualmente,desordenado, haciendo que muchas veces falten o sobren cosas.El sistema permite llevar un control actualizado de que hay, que hace falta y qué hacer el inventario sea más simple.

Existen soluciones similares, como lo son Glovo, theFork o Covermanager.

Glovo se enfoca en pedidos, ya sea para domicilio o para ir a recoger al local. Glovo trabaja con comisión por pedido, entre un 30/35% + IVA.Además, los datos pertenecen a la empresa, no al negocio, por lo que este no tendría control de clientes.También, controla notablemente el negocio, los precios, radios de reparto y tarifas.

TheFork se enfoca en que los usuarios puedan descubrir restaurantes, pero solo hacen reservas y es algo parecido a un portal con multitud de restaurantes para elegir. Su precio oscila, dependiendo del plan contratado, de los 75 euros a los 200, teniendo comisiones de 2 a 2'5 euros por comensal(precio orientativo).Los datos también pertenecen a la empresa, no al negocio.La marca impone un modelo económico y operativo basado en comisiones por comensal, cuotas de software y la asunción de los costes de sus promociones.

CoverManager es similar a TheFork, con la diferencia de que este si es un software personalizado de cada restaurante, pero se centra también en sistema de reservas.Tiene una cuota mensual fija que oscila de los 89 euros hasta 189 al mes.Los datos pertenecen totalmente al bar, algo que se asemeja a mi proyecto, al igual que el negocio es poco dependiente a la marca.

Mi sistema combinará las funciones de los vistos anteriormente, será un software personalizado para cada negocio hostelero ,accesible y orientado para pequeños negocios, abarcando las funcionalidades necesarias, como consultas, gestión de reservas y pedidos,gestión de stock…

## OBJETIVOS

El objetivo principal que me he propuesto es configurar un servicio informático para optimizar el trabajo de pequeños negocios hosteleros.

Crear una base de datos en la que se alojarán los datos de todos los clientes, el stock de los productos, entre otras cosas.

Diseñar una estructura de red simple para que el servidor, que se encuentra dentro del negocio, de salida a internet y se pueda acceder a la página web y a sus servicios.

Crear una página web fácilmente accesible por el navegador, accesible tanto desde móvil como ordenador y personalizada del negocio deseado .

Gestionar el DNS,configurando un dominio público para que en el buscador al poner el nombre del establecimiento te dirija a la página directamente, a sociando un nombre de dominio a la IP del servidor

Gestionar el servicio para simular pagos a través de tarjeta por la página.

Crear y gestionar el servicio de pedidos para permitir encargar pedidos y que de el precio exacto de los productos.

Hacer copias de seguridad de los datos para garantizar la seguridad de estos. Configurar las copias de seguridad de manera que estas se guarden en la nube, de modo que el servidor se pueda restaurar desde aquí.

Crear un balanceador de cargas y cluster web para garantizar la alta disponibilidad de mi servidor, y que si este falla, aun así siga estando activo.Estas estarán en máquinas físicas, para aislarlas y facilitar la recuperación.

Proteger el servidor expuesto en internet mediante protocolos de seguridad , ya que al publicar la web en internet y alojar datos de usuarios, trabajadores,etc, estos tienen el riesgo de ser fácilmente accesible por usuarios no deseados.

Configurar los roles y permisos que tendrán los diferentes usuarios de la plataforma: los clientes,trabajadores, dueños o administradores…

Configurar el sistema de monitorización en una máquina virtual independiente de las del clúster para que supervise el servidor, copias de seguridad…

Configurar la replicación de la base de datos entre los nodos para que ambos servidores utilicen la misma base de datos.

## Lenguajes de programación y tecnologías

Para la realización de este proyecto , primero usaré Virtualbox para crear máquinas virtuales , que serán linux, más concretamente ubuntu desktop ya que al ser gráfico es más sencillo gestionarlas, y es más sencillo para instalar los servicios deseados.

Usaré html para el diseño de la página y php para el funcionamiento de ésta, siendo los dos lenguajes que más conozco.

El servidor web que voy a utilizar será apache, ya que es el que mejor manejo

Para la base de datos usaré MySQL como gestor de base de datos, con SQL como lenguaje de consulta.

Utilizaré la nube,concretamente google drive, y la herramienta rclone para alojar las copias de seguridad del servidor, y garantizar la seguridad de estos.

Bash y cron para automatizar las copias, y mysqldump para volcar la base de datos.

Para el balanceador de carga usaré HAproxy.

Para la monitorización del servidor utilizaré Grafana, siendo la más gráfica, junto con Prometheus para almacenar los datos

Para garantizar la seguridad, utilizaré firewall y https.

Utilizaré keepalived para la ip virtual compartida entre los balanceadores

Usaré DNS para el nombre de dominio público.

## Prototipo de interfaz de usuario

Pantalla para iniciar sesión en la página:

![Pantalla de inicio de sesión](img/login.png)

La pantalla de inicio:

![Pantalla de inicio](img/inicio.png)

Interfaz para hacer pedidos:

![Interfaz para hacer pedidos](img/pedidos.png)

Para hacer reservas, tanto en terraza:

![Reservas en terraza](img/reservas-terraza.png)

Como en salón:

![Reservas en salón](img/reservas-salon.png)

Y para hacer consultas:

![Interfaz de consultas](img/consultas.png)

## Gestor de base de datos

Voy a usar el gestor de base de datos MySQL, ya que creo que es el lenguaje que más manejo, el que más he utilizado y el más óptimo para almacenar datos de clientes,pedidos…

La infraestructura de la base de datos de mi proyecto se verá de la siguiente manera representado en un diagrama entidad relación:

![Diagrama entidad-relación](img/er.png)

## Entornos de aplicación del proyecto

Para el hardware de mi proyecto,usaré 4 máquinas físicas, 2 para los servidores web activos en clúster y las otras 2 para los balanceadores de carga.

En las máquinas de los servidores web usaré 2 CPU, 6 GB de RAM y 40 GB disco.Al ser el más cargado, el que más servicios lleva, es necesario más CPU y más ram.

Para configurar los balanceadores de carga, voy a usar HAproxy.

En los balanceadores de carga, se usan los requisitos mínimos de Ubuntu Desktop, que son superiores a los de HAProxy, 1 CPU, 4 GB de RAM y 25 GB de disco.

Los equipos usarán Ubuntu, ya que es el sistema operativo que más manejo y en el que es más fácil instalar los servicios deseados.

Para diseñar el código de la página web, utilizaré Visual Studio Code.

Para el prototipo de la web usaré figma.

Los equipos estarán conectados a la red del negocio con cable, para asegurar una conexión menos expuesta que el wifi y estable.Además, se contará con un router para proporcionar el internet y un switch para prolongar la conexión a todos los equipos.

La máquina virtual en la cual se alojará la monitorización del sistema,se encontrará en adaptador puente, para que se encuentre en la misma red que las máquinas físicas.Esta máquina virtual se encontrará en el equipo físico de uno de los servidores web.

Las ip de estas máquinas serán fijas, estáticas en cada equipo, para evitar una desconfiguración de la red.Con keepalived usare una ip virtual compartida para los balanceadores, que estará fuera del rango del router.

Usaré un SAI que es el dispositivo que mantendrá encendidas las máquinas y las protegerá contra fallos eléctricos cuando se corta la luz.Aguanta fallos cortos, y también alimentará al router, para evitar que el servicio se quede sin salida a internet.

Para la simulación de este proyecto usaré máquinas virtuales para simular que son equipos físicos.

Para hacer el prototipo de red, he utilizado CiscoPacketracer.

## FASES DE DESARROLLO

**Planificación inicial:**Definir cómo voy a desarrollar el proyecto y qué elementos voy a necesitar para llevarlo a cabo. Organizar las tareas que tengo que realizar, establecer los objetivos que quiero conseguir y determinar qué máquinas, programas y servicios voy a utilizar. También estudiaré cómo distribuir el trabajo para poder completar todas las partes del proyecto.

**Análisis y diseño:**Estudiar cómo va a funcionar el sistema y cómo se van a relacionar sus diferentes componentes. Diseñar la estructura de la base de datos, la interfaz de la página web y la infraestructura de red que utilizarán los servidores. También definir los distintos tipos de usuarios y sus permisos, así como los servicios que necesitaré configurar para garantizar el funcionamiento y la seguridad del sistema.

**Desarrollo e implementación:**Comenzar a desarrollar la aplicación web utilizando HTML y PHP. Crear las diferentes páginas y funcionalidades, como el inicio de sesión, la consulta de la carta, la realización de pedidos y la gestión de reservas.

También voy a configurar la base de datos MySQL, creando las tablas necesarias para almacenar la información de los clientes, productos, pedidos, reservas y stock.

Posteriormente, voy a instalar y configurar los servidores Apache en las máquinas correspondientes, prepararé la infraestructura de red y voy a configurar los servicios necesarios para que la aplicación pueda funcionar correctamente.

Por último, voy a implementar el sistema de balanceo de carga mediante HAProxy y Keepalived, además de configurar las copias de seguridad automatizadas y el sistema de monitorización.

**Pruebas y validación:**Una vez desarrollado el sistema, tendrá que realizar diferentes pruebas para comprobar que todas las funcionalidades funcionan correctamente.

Voy a comprobar que los clientes pueden registrarse, iniciar sesión, consultar los productos, realizar pedidos y reservar mesas. También tengo que verificar que los trabajadores puedan gestionar el stock y consultar los pedidos y reservas.

Además, tendré que realizar pruebas de conectividad entre las máquinas, voy a comprobar que el balanceador distribuye correctamente las peticiones entre los servidores y simular la caída de uno de ellos para verificar que el servicio continúa funcionando.

También habrá que comprobar que las copias de seguridad se realizan correctamente y que los datos pueden recuperarse en caso de fallo. Por último, voy a revisar el sistema de monitorización para asegurarme de que recoge correctamente la información de los servidores.

**Despliegue :**Cuando haya comprobado que todo funciona correctamente, proceder a poner en funcionamiento el sistema en el entorno preparado para el proyecto.

Configurar el dominio y el acceso a la página web, verificar que los servicios estén activos y que los clientes puedan acceder desde diferentes dispositivos, tanto móviles como ordenadores.

También comprobar que los trabajadores y administradores pueden acceder a sus respectivos apartados con los permisos correspondientes. Dejar configurados los servicios para que se inicien automáticamente y el sistema pueda funcionar de forma continua.

**Mantenimiento y soporte:** Una vez puesto en marcha el sistema, será necesario realizar un mantenimiento periódico para garantizar su correcto funcionamiento.

Actualizar los sistemas operativos y los servicios instalados para corregir posibles errores y mejorar la seguridad. También revisar los registros de actividad y las alertas generadas por el sistema de monitorización para detectar posibles problemas.

Comprobar periódicamente que las copias de seguridad se realizan correctamente y que se pueden restaurar los datos cuando sea necesario. Además, revisar el estado de los servidores, la base de datos, el balanceador de carga y la infraestructura de red.

Por último, solucionar los posibles problemas que puedan surgir y realizar mejoras en la aplicación según las necesidades del negocio.

## Módulos del ciclo formativo relacionados

**Implantación de sistemas operativos:**Instalación y configuración de Ubuntu en los servidores y máquinas virtuales.

**Planificación y administración de redes:**Configuración de la red, direcciones IP, router, switch y conexión entre servidores.

**Fundamentos de hardware:**Selección y configuración de los componentes físicos de los equipos.

**Gestión de bases de datos:**Creación y diseño de la base de datos MySQL para almacenar clientes, pedidos, reservas y productos.

**Lenguajes de marcas y sistemas de gestión de información:**Utilización de HTML para diseñar y estructurar la página web.

**Administración de sistemas operativos:**Administración de los servidores, usuarios, permisos y automatización de tareas.

**Servicios de red e Internet:**Configuración de Apache, DNS y otros servicios necesarios para publicar la web.

**Implantación de aplicaciones web:**Desarrollo e instalación de la aplicación web utilizando HTML y PHP.

**Administración de sistemas gestores de bases de datos:**Administración de MySQL, copias de seguridad y replicación de bases de datos.

**Seguridad y alta disponibilidad:**Protección de los servidores, configuración de HAProxy, Keepalived y monitorización.

## ANEXOS Y BIBLIOGRAFÍA

**Anexos:**Prototipo interfaz de la página web:

<https://www.figma.com/make/vnpZdQyytBaSRNhA8QoAVP/Web-de-Reservas-y-Pedidos?t=xP7PN0TLsF0jrzzw-20&fullscreen=1>

Prototipo de la red:

![Prototipo de la red](img/red.png)

**Bibliografías:**

Búsqueda de Estado del arte:

<https://www.thefork.es/contact>

<https://www.theforkmanager.com/es/landing-page/sistema-de-software-para-restaurante?ps=SEA&sfcid=701Jv00001EDAygIAH&utm_source=google&utm_medium=cpc&utm_campaign=ES_GOOGLE_B2B_AI-Max&utm_term=gestor%20de%20reservas%20restaurante&gad_source=1&gad_campaignid=24380685743&gbraid=0AAAAADlbOxV7jI25ALMRlYL068UU-Dz1T&gclid=Cj0KCQiAtvXXBhC2ARIsAJc8SURYWE6Q7GWtaz386IO7EZlk4qlKx4zEzErOrEmqUDOG-bKpZWvrULcaAh5pEALw_wcB>

<https://glovoapp.com/docs/es/faq/>

Datos MySQL:

Información HAproxy

Ubuntu:
