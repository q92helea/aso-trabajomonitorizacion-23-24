# ASO_TrabajoMonitorizacion

# 1  Las herramientas de monitorización de servidores.
       
## 1.1  Introducción general.
## 1.2  Las herramientas  a estudiar: ICINGA
Icinga es una plataforma de monitoreo de código abierto que se utiliza para supervisar la disponibilidad y el rendimiento de los recursos informáticos, como servidores, redes, servicios y aplicaciones. Su nombre, Icinga, es una palabra zulú que significa "busca", "navega" o "examina" y se pronuncia con un chasquido consonántico.

Esta plataforma ofrece una flexibilidad, escalabilidad y capacidades avanzadas, que la ha convertido en una herramienta madura y ampliamente utilizada por administradores de sistemas y profesionales de TI. Sus características incluyen la generación de informes detallados, un sistema de alertas altamente personalizable y la capacidad de adaptarse a entornos diversos. Icinga es conocida por su capacidad para escalar desde implementaciones simples hasta despliegues complejos con miles de dispositivos monitoreados, lo que la hace atractiva para una amplia gama de usuarios en diversos sectores.

 # 2  La herramienta ICINGA
 
 ## 2.1  Historia
 
 Ichinga nacio el 6 de Mayo 2009, cuando un grupo de  miembros del anterior consejo asesor de la comunidad de Nagios, desarrolladores de numerosas extensiones de Nagios y personas de NETWAYS, el organizador de la Conferencia de Monitoreo de Nagios y proveedor de la plataforma MonitoringExchange (anteriormente NagiosExchange), anunciaron Icinga, como una nueva bifurcación del código, como respuesta a su descontento por el cuello de botella existente, en ese momento, en el desarrollo del software de Nagios, y su deseo de abrir su desarrollo a una base más amplia. 
 
En su primer año, los desarrolladores de Icinga lanzaron versiones separadas del núcleo, API e interfaz web, y celebraron su descarga número 10,000. En 2010, el proyecto Icinga lanzó un núcleo e interfaz web unificados y estables; añadió soporte para la transición de IPv4 a IPv6, optimizó la conectividad de la base de datos y renovó la interfaz de usuario con su "Icinga Web", e integró varios complementos de la comunidad (PNP4Nagios, LConf, Heatmap y Business Process Addon) logrando más de 100,000 descargas y aumentado a 23 la cantidad de miembros del equipo. 

Esta buena trayectoria como su potencial fueron respaldados con su inclusión, por parte Jeffrey Hammond, de la empresa Forrester Research, en la lista de proyectos de código abierto "creciente" (en contraposición a "menguante").Esta distinción resaltaba el crecimiento y la evolución positiva del proyecto, por el aumento en su demanda y relevancia en el ámbito de la monitorización de sistemas y redes. 

En octubre de 2012, el proyecto Icinga presentó un avance tecnológico significativo: Icinga 2. Este fue un desarrollo paralelo y un reemplazo del marco de trabajo del núcleo original. Los desarrolladores de Icinga expresaron su intención de reescribir el núcleo para abordar problemas como la configuración complicada y las limitaciones de escalabilidad en implementaciones de gran tamaño. El proyecto también anunció planes para desarrollar el núcleo de Icinga 2 principalmente en lenguaje C++, diseñar una nueva arquitectura de cargador de componentes y remodelar el proceso de ejecución de las verificaciones de monitorización, pero esto no ocurrió hasta el 2014, cuando se lanzó la primera versión estable de Icinga 2, que incluía características como un agente y una API, que estaban programadas para ser lanzadas en el futuro y desarrolladas principalmente en lenguaje C++. Además, presentó una nueva arquitectura de cargador de componentes, así como una remodelación del proceso de ejecución de las verificaciones de monitorización.

Icinga ha experimentado un desarrollo constante, con lanzamientos frecuentes y un crecimiento significativo en su base de usuarios. Su arquitectura modular, capacidad para recopilar datos de manera eficiente, generación de informes detallados, sistema de alertas altamente personalizable y capacidad para escalar desde implementaciones simples hasta despliegues complejos con miles de dispositivos monitoreados la convierten en una herramienta atractiva para una amplia gama de usuarios. La Última versión estable, la 2.14.2 se lanzó el 18 de enero de 2024.

 ## 2.2  Funciones/utilidades y características. Ventajas y desventajas
	Nota: hablar de versiones gratuitas y pago (funcionalidades de pago)
 ## 2.3  Plataformas posibles donde instalar  requisitos (agentes y máquinas desde las que se monitoriza).
	Sistemas y distros con versiones necesarias.  
 ## 2.4  Requisitos tanto de agentes como de máquinas de monitoreo.
 ## 2.5  Esquema de Red (entorno). Máquinas, dirección de la red, IP’s, S.O. de las máquinas, servicios instalados. 
![esquema](diagrama.png)
## 2.6  Instalación y configuración en máquinas a monitorizar.
### Instalación y Configuración de Icinga en un Servidor Windows

**Preparación del servidor:**

* **Actualice el sistema operativo:** Asegúrese de tener la última versión de Windows Server instalada.
* **Instale el paquete de .NET Framework 4.8:** Icinga requiere .NET Framework para funcionar.
* **Instale el módulo de Windows PowerShell ISE:** Se utiliza para ejecutar scripts de PowerShell para la configuración.
* **Descargue los archivos de instalación:** Obtenga la última versión de Icinga desde el sitio web oficial: https://icinga.com/get-started/download/

**Instalación de Icinga:**

1. **Ejecute el instalador:** Inicie el archivo `icinga-windows-x64.msi` y siga las instrucciones en pantalla.
2. **Elija el tipo de instalación:** Seleccione "Servidor Icinga" para una instalación completa con la interfaz web y la base de datos.
3. **Configure los componentes:** Elija los módulos de Icinga que desea instalar. Se recomienda instalar los módulos básicos como `icinga2`, `icingaweb2` e `ido-mysql`.
4. **Configure la base de datos:** Seleccione "Usar una base de datos existente" e ingrese la información de su servidor MySQL.
5. **Complete la instalación:** Siga las instrucciones en pantalla para finalizar la instalación.

**Configuración de Icinga:**

1. **Configure el archivo de configuración principal:** Abra el archivo `icinga2.conf` en un editor de texto como Notepad++.
2. **Ajuste la configuración general:** Modifique la configuración según sus necesidades, como la zona horaria, el nombre del servidor y la configuración de notificaciones.
3. **Defina los hosts y servicios a monitorizar:** Cree archivos de configuración para cada host y servicio que desea monitorizar. Utilice la sintaxis de Icinga para definir las comprobaciones y notificaciones.
4. **Importe la configuración:** Importe los archivos de configuración a Icinga usando el comando `icinga2 feature enable configimport`.
5. **Inicie el servicio Icinga:** Inicie el servicio `Icinga 2` para que la configuración surta efecto.

**Acceso a la interfaz web:**

1. Abra un navegador web e ingrese la dirección URL `https://localhost:5665/icingaweb2/`.
2. Inicie sesión con el usuario `icingaadmin` y la contraseña que estableció durante la instalación.
3. La interfaz web le permite ver el estado de sus hosts y servicios, administrar la configuración y crear nuevos monitores.

**Recursos adicionales:**

* Documentación oficial de Icinga: https://icinga.com/docs/icinga-2/latest/doc/04-configuration/
* Tutoriales de Icinga: https://www.youtube.com/watch?v=gmv66GIA0l8
* Foro de la comunidad de Icinga: https://community.icinga.com

# 3. Instalación y configuración en máquinas a monitorizar (agentes) y remotas.
 ## 3.1  Instalación y configuración en agentes 
 ## 3.2  Diseño de pruebas.  Decisión de servicios a monitorizar
 ## 3.3  Puesta en marcha (pruebas) y ejemplo de uso.

 # 4  [Otros puntos a investigar según la herramienta]

    • Instalación mediante script en las máquinas de la red a monitorizar.
    • Monitorización remota por SSH  o en consola. 
    • Monitorización usando el navegador web.Alerta a usuario 
    • Tarea programada (si procede) en cron.
    • Otros usos: proxy, etc 

 # 5  Conclusiones y problemas encontrados 
 Conclusiones tras conocer la herramienta. Indicar también problemas (y cómo se han solventado).


 # 6  OPCIONAL --- Comparativa con otras herramientas (trabajo de otro equipo)
 ## 6.1   Funciones/utilidades y características. Ventajas y desventajas
 ## 6.2   Plataformas y  requisitos.
 ## 6.3  Conclusión tras la comparativa (si lo consideras necesario)

 # 7  Bibliografía


# ANEXO. Desarrollo del proyecto con SCRUM
## I. Equipo y roles
## II. Reuniones realizadas (events)
## III. Documentos: 
- link al backlog del equipo  -- no olvidar compartir con mctripiana@iesgrancapitan.org --
- Añadir (compartir en drive, link) cualquier otro documento que sea necesario
           
           
