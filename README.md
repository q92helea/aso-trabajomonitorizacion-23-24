# ASO_TrabajoMonitorizacion

# 1  Las herramientas de monitorización de servidores.
       
## 1.1  Introducción general.
## 1.2  Las herramientas  a estudiar
           

 # 2  La herramienta XXX
 ## 2.1  Historia
 ## 2.2  Funciones/utilidades y características. Ventajas y desventajas
	Nota: hablar de versiones gratuitas y pago (funcionalidades de pago)
 ## 2.3  Plataformas posibles donde instalar  requisitos (agentes y máquinas desde las que se monitoriza).
	Sistemas y distros con versiones necesarias.  
 ## 2.4  Requisitos tanto de agentes como de máquinas de monitoreo.
 ## 2.5  Esquema de Red (entorno). Máquinas, dirección de la red, IP’s, S.O. de las máquinas, servicios instalados. 
![esquema](Diagrama sin título.drawio)
## 2.6  Instalación y configuración en máquinas a monitorizar.
### Instalación y Configuración de Icinga en un Servidor Windows

**Preparación del servidor:**

* **Actualice el sistema operativo:** Asegúrese de tener la última versión de Windows Server instalada.
* **Instale el paquete de .NET Framework 4.8:** Icinga requiere .NET Framework para funcionar.
* **Instale el módulo de Windows PowerShell ISE:** Se utiliza para ejecutar scripts de PowerShell para la configuración.
* **Descargue los archivos de instalación:** Obtenga la última versión de Icinga desde el sitio web oficial: <se quitó una URL no válida>.

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
           
           
