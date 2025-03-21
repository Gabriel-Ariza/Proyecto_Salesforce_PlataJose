# ConstruFurgo S.A.S. - Organigrama

## Estructura Jerárquica

```mermaid
graph TD
    A[CEO] --> B{Gerentes};
    B --> C[Gerente de Compras];
    B --> D[Gerente de Producción];
    B --> E[Gerente de Soporte];
    B --> F[Gerente de Ventas];
    C --> G[Coordinador de Logística];
    C --> H[Ejecutivo de Compras];
    E --> I[Coordinador de Soporte];
    E --> J[Técnico de Ensamblaje];
    F --> K[Administrador de Ventas];
    F --> L[Ejecutivo de Ventas];
```
<br/>


## Configuración de Divisas y Datos de la Empresa en Salesforce para ConstruFurgo S.A.S.

Este documento resume los cambios realizados para la implementación de la empresa ConstruFurgo S.A.S. en Salesforce, enfocándose en los resultados obtenidos.

## 1. Actualización de la Información de la Empresa

* Se ha actualizado la información básica de la organización en Salesforce. Los datos clave incluyen:
    * Nombre de la organización: ConstruFurgo S.A.S.
    * Dirección principal: Av. Boyacá #12-33, Bogotá, Colombia.
    * Configuración regional: Español (Colombia).
    * Zona horaria: (GMT-05:00) Colombia Standard Time (America/Bogota).
* Estos cambios aseguran que la información de la empresa en Salesforce refleje la realidad de ConstruFurgo S.A.S.

### 1.1. Creación de la Cuenta y Contacto

* Se creó una cuenta en Salesforce con la siguiente información:
    * Razón Social: ConstruFurgo S.A.S.
    * Número de Identificación Tributaria (NIT): 901456789-2.
    * Domicilio Principal: Av. Boyacá #12-33, Bogotá, Colombia.
    * Annual Revenue: $5,000,000 USD.
    * Industry: Diseño, fabricación, comercialización y mantenimiento de furgones industriales.
    * SIC Code: 456789 como registro mercantil
* Se creó un contacto asociado a la cuenta ConstruFurgo S.A.S.:
    * Nombre: Juan Pérez López
    * Email: contacto@construfurgo.com
    * Se designo a Juan perez Lopez como representante legal de la empresa.
* Estos registros permiten gestionar la información de la empresa y su representante legal de manera efectiva.


## 2. Configuración de Divisas

1.  **Activación de Divisas:**
    * **2.1** Se han activado las divisas **USD (Dólar Estadounidense)** y **COP (Peso Colombiano)**.

2.  **Habilitación para Usuarios:**
    * **2.2** Esto permite que los usuarios de ConstruFurgo S.A.S. puedan registrar transacciones y oportunidades en ambas divisas.

3.  **Configuración Inicial:**
    * **2.3** Se ha configurado la tasa de conversión inicial entre USD y COP.
    * **2.4** Se han establecido los decimales correspondientes a cada moneda.

4.  **Gestión Avanzada de Divisas:**
    * **2.5** Se ha habilitado la función de **Gestión Avanzada de Divisas** en la organización de Salesforce.
    * **2.6** Esto permite el seguimiento y la actualización diaria de la tasa de cambio (TRM) entre USD y COP.
    * **2.7** Las oportunidades en Salesforce reflejarán los valores convertidos según la TRM del día.

## 3. Visualización de Oportunidades en COP y USD

* Las oportunidades en Salesforce ahora pueden mostrar montos en USD y COP.
* Las conversiones entre divisas se realizan automáticamente, utilizando la TRM actualizada.
* Los informes y paneles pueden mostrar datos financieros en ambas divisas.

## Resultado

Con estos cambios, ConstruFurgo S.A.S. ahora tiene un entorno de Salesforce configurado para manejar transacciones en múltiples divisas y reflejar la tasa de cambio diaria, asegurando la precisión de los datos financieros.

<br/>
<br/>

## Configuración de Roles en Salesforce para ConstruFurgo S.A.S.

Este apartado describe la configuración de roles personalizada para ConstruFurgo S.A.S. en Salesforce, incluyendo la eliminación de roles predeterminados y la implementación de una estructura jerárquica específica.

## 1. Eliminación de Roles Predeterminados

* Se han eliminado los roles predeterminados proporcionados por Salesforce.
* Esto permite una configuración de roles completamente personalizada, adaptada a la estructura organizativa de ConstruFurgo S.A.S.

## 2. Estructura de Roles Personalizada

### 2.1 Descripción de Roles y Dependencias

| **Rol**                     | **Descripción**                                                                                              | **Dependencias**                          |
|-----------------------------|--------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| **CEO**                      | Máxima autoridad de la empresa. Responsable de la dirección estratégica y la toma de decisiones clave. Supervisa directamente a los Gerentes. | -                                         |
| **GERENTE DE COMPRAS**       | Responsable de la adquisición de materiales y servicios necesarios para la producción. Supervisa al Coordinador de Logística y al Ejecutivo de Compras. | Rinde cuentas al CEO.                    |
| **Coordinador de Logística** | Responsable de la gestión de la cadena de suministro y la logística de la empresa.                           | Rinde cuentas al **GERENTE DE COMPRAS**.      |
| **Ejecutivo de Compras**     | Responsable de la ejecución de las compras y la gestión de proveedores.                                      | Rinde cuentas al **GERENTE DE COMPRAS**.      |
| **GERENTE DE PRODUCCIÓN**    | Responsable de la planificación y ejecución de la producción. Supervisa directamente a los Técnicos de Ensamblaje. | Rinde cuentas al CEO.                    |
| **GERENTE DE SOPORTE**       | Responsable de la gestión del soporte técnico y el mantenimiento de equipos. Supervisa al Coordinador de Soporte y a los técnicos de ensamblaje. | Rinde cuentas al CEO.                    |
| **Coordinador de Soporte**   | Responsable de coordinar las actividades de soporte técnico.                                                | Rinde cuentas al **GERENTE DE SOPORTE**.     |
| **Técnico de Ensamblaje**    | Responsable del ensamblaje y mantenimiento de los productos.                                                 | Rinde cuentas al **GERENTE DE SOPORTE**.     |
| **GERENTE DE VENTAS**        | Responsable de la planificación y ejecución de las estrategias de ventas. Supervisa al Administrador de Ventas y al Ejecutivo de Ventas. | Rinde cuentas al CEO.                    |
| **Administrador de Ventas**  | Responsable de la gestión de las operaciones de ventas y el seguimiento de clientes.                        | Rinde cuentas al **GERENTE DE VENTAS**.      |
| **Ejecutivo de Ventas**      | Responsable de la ejecución de las ventas y la atención al cliente.                                          | Rinde cuentas al **GERENTE DE VENTAS**. |

<br/>

## Creación de Usuarios y Perfiles

Se han creado los siguientes perfiles y usuarios en la organización de Salesforce:

### Perfiles Creados

| Nombre del Perfil            | Departamento ideal            | Basado en Licencia de Usuario |
| :--------------------------- | :------------------------- | :----------------------------- |
| Production Manager   | Producción      | Salesforce Platform User        |
| Sales Manager        | Ventas          | Salesforce Platform User        |
| Procurement Specialist | Compras         | Salesforce Platform User        |
| Technical Support    | Soporte         | Standard User                 |

### Usuarios Creados

* **carlosperez@CPwhiteconstrufurgo.com**
    * Rol: Gerente de Producción (Production Manager)
* **mariagomez@MGblueconstrufurgo.com**
    * Rol: Gerente de Ventas (Sales Manager)
* **anamartinez@AMpinkconstrufurgo.com**
    * Rol: Gerente de Compras (Procurement Specialist)
* **gabrielleon@GLredconstrufurgo.com**
    * Rol: Gerente de Soporte (System Administrator)
* **manuelparedes@MPgrayconstrufurgo.com**
    * Rol: CEO (Usuario Estándar)


Estos usuarios serán ideales para validar la correcta implementación de la organización construfurgo S.A.S. en Salesforce

## Beneficios de la Configuración Personalizada

* La estructura de roles personalizada refleja la organización real de ConstruFurgo S.A.S.
* Facilita la asignación de permisos y el control de acceso a datos en Salesforce.
* Mejora la eficiencia y la claridad en la gestión de la empresa.


<br/>
<br/>

# Importación de Datos CSV con Data Loader

## Account

1.  **Creación de Campo Personalizado:**
    * Se creó un campo personalizado llamado `id_cuenta` en el objeto `Account`.
    * Este campo se configuró como tipo "Texto (ID externo)" y se marcó como "Único" e "ID externo" para permitir su uso como campo de búsqueda (lookup) en Data Loader.
2.  **Imagen de Configuración:**

    ![Configuración del campo id_cuenta en Account](https://media.discordapp.net/attachments/1133802881250758676/1352651030856208434/image.png?ex=67dec9f0&is=67dd7870&hm=fee1ff9ded7e7dbb653574f28e00fe2e1df5e0b39deefb8824e0d2a0c6fb8828&=&format=webp&quality=lossless&width=971&height=930)

## Lead

1.  **Inserción de Registros:**
    * Se insertaron 100 registros en el objeto `Lead` utilizando Data Loader.

## Contact

1.  **Inserción de Registros:**
    * Se insertaron registros en el objeto `Contact` utilizando Data Loader.
2.  **Imagen de inserción:**
    ![Inserción de contactos](https://media.discordapp.net/attachments/936302388053168179/1352660820986822850/image.png?ex=67ded30e&is=67dd818e&hm=9b4d49cbbe8e6340ccc5572285281b207d73e777c1e959332c63648475fefcc5&=&format=webp&quality=lossless&width=1860&height=749)

## Cases

1.  **Inserción de Registros:**
    * Se insertaron 100 registros en el objeto `Cases` utilizando Data Loader.

## Oportunidades

1.  **Modificación del Archivo CSV:**
    * Se modificó el archivo CSV para incluir una columna `Close Date` (Fecha de Cierre).
    * Este campo es obligatorio para la creación de registros de `Opportunity`.
2.  **Inserción de Registros:**
    * Se insertaron los registros de `Opportunity` utilizando Data Loader, incluyendo la columna `Close Date`.

![Inserción oportunidades](https://media.discordapp.net/attachments/936302388053168179/1352681032578498611/image.png?ex=67dee5e1&is=67dd9461&hm=fc335b2db801026e6994f31538c2ba0af2c6ea96ec8453525b64d16908c4baf0&=&format=webp&quality=lossless&width=1860&height=800)

# Configuración de Carpetas de Informes por Departamento y Permisos de Acceso

## Introducción

Este documento describe la configuración de carpetas de informes compartidas para cada departamento de la compañía y los permisos de acceso asignados a cada una, incluyendo la creación de subcarpetas confidenciales para el CEO y el gerente del departamento.

## Carpetas de Departamentos y Permisos de Acceso

* **Ventas:**
    * Nombre de la carpeta: `equipo_ventas`
    * Permisos:
        * Rol "CEO": Acceso "Ver" (View)
        * Rol "Administrador de Ventas": Acceso "Ver" (View)
        * Rol "Ejecutivo de Ventas": Acceso "Ver" (View)
    * Subcarpeta Confidencial: `reportes_gerencia`
        * Permisos:
            * Rol "CEO": Acceso "Administrar" (Manage)
            * Rol "Gerente de Ventas": Acceso "Administrar" (Manage)

* **Soporte:**
    * Nombre de la carpeta: `equipo_soporte`
    * Permisos:
        * Rol "CEO": Acceso "Ver" (View)
        * Rol "Técnico de Ensamblaje": Acceso "Ver" (View)
        * Rol "Coordinador de Soporte": Acceso "Ver" (View)
    * Subcarpeta Confidencial: `reportes_gerencia`
        * Permisos:
            * Rol "CEO": Acceso "Administrar" (Manage)
            * Rol "Coordinador de Soporte": Acceso "Administrar" (Manage)

* **Compras:**
    * Nombre de la carpeta: `equipo_compras`
    * Permisos:
        * Rol "CEO": Acceso "Ver" (View)
        * Rol "Gerente de Compras": Acceso "Ver" (View)
        * Rol "Ejecutivo de Compras": Acceso "Ver" (View)
    * Subcarpeta Confidencial: `reportes_gerencia`
        * Permisos:
            * Rol "CEO": Acceso "Administrar" (Manage)
            * Rol "Gerente de Compras": Acceso "Administrar" (Manage)

<br>
<br>


# Reportes y Dashboards de la organización

## Informes y Dashboard de Ventas para el Departamento de Ventas


## Informes de Ventas

Se crearon los siguientes informes para el departamento de ventas:

1.  **Oportunidades Abiertas:**
    * Informe que muestra las oportunidades que aún no se han cerrado.

    ![Reporte](https://media.discordapp.net/attachments/936302388053168179/1352667777625886831/image.png?ex=67ded989&is=67dd8809&hm=9ee04a3fa3a13fd005ded7fb707ac4ea4390dafb8410c18ea8c7f4282418813a&=&format=webp&quality=lossless&width=1858&height=800)

2.  **Oportunidades Perdidas:**
    * Informe que muestra las oportunidades que se han cerrado como perdidas.

    ![Reporte](https://media.discordapp.net/attachments/936302388053168179/1352667864347316266/image.png?ex=67ded99e&is=67dd881e&hm=d24d0418ff0e036bb36b2964a7b25d3e26b3ce6a4e673074207278f6f0e73912&=&format=webp&quality=lossless&width=1840&height=800)

3.  **Oportunidades Ganadas:**
    * Informe que muestra solo las oportunidades que se han cerrado como ganadas.

    ![Reporte](https://media.discordapp.net/attachments/936302388053168179/1352667531659182160/image.png?ex=67ded94e&is=67dd87ce&hm=bf8f442396754b262330abc556aa32fc7c016a727fd272863da69261125ce47e&=&format=webp&quality=lossless&width=1860&height=794)

## Dashboard de Ventas

* Se creó un dashboard que incluye los tres informes anteriores para proporcionar una visión general del estado de las oportunidades de ventas.
* El dashboard es accesible solo para el CEO y el Gerente de Ventas, mediante la configuración de permisos adecuados.

![Reporte](https://media.discordapp.net/attachments/936302388053168179/1352667267699048590/image.png?ex=67ded90f&is=67dd878f&hm=d4022c48dd6c160bc1b9de1fbbb7d3509c77c9d822b2e18029b4558315f0f41c&=&format=webp&quality=lossless&width=1676&height=800)

<br>
<br>

# Informes y Dashboard de Casos para el Departamento de Soporte

## Informes de Casos

Se crearon los siguientes informes para el departamento de soporte:

1.  **Casos Abiertos:**
    * Informe que muestra los casos que aún no se han cerrado.
    * Imagen del reporte:
        ![Reporte](https://media.discordapp.net/attachments/936302388053168179/1352695438918160425/image.png?ex=67def34c&is=67dda1cc&hm=d15eeed0c60589a3d1bc0add7fc9e16a7c60cdc3bc47216a84cac4ef53d02bd5&=&format=webp&quality=lossless&width=1818&height=800)

2.  **Casos Cerrados:**
    * Informe que muestra los casos que se han cerrado.
    * Imagen del reporte:
        ![Reporte](https://media.discordapp.net/attachments/936302388053168179/1352691420066091062/image.png?ex=67deef8e&is=67dd9e0e&hm=3b091aa619cc077476f17a4b4a7e4283578c8168a28608eca6f08e587213620e&=&format=webp&quality=lossless&width=1774&height=800)

3.  **Medios de Apertura de Casos:**
    * Informe que muestra los diferentes medios por los cuales se abren los casos (por ejemplo, correo electrónico, teléfono, portal web).
    * Imagen del reporte:
        ![Reporte](https://media.discordapp.net/attachments/936302388053168179/1352694933420507257/image.png?ex=67def2d3&is=67dda153&hm=b8d7e998bfee437e1c9295a368d92670d6c125431fe004cffabab1f0a7fb0b6c&=&format=webp&quality=lossless&width=1811&height=800)

## Dashboard de Casos

* Se creó un dashboard que incluye los tres informes anteriores para proporcionar una visión general del estado de los casos de soporte.
* El dashboard es accesible solo para el CEO y el Gerente de Soporte, mediante la configuración de permisos adecuados.
* Imagen del dashboard:
    ![Reporte](https://media.discordapp.net/attachments/936302388053168179/1352695660419350589/image.png?ex=67def381&is=67dda201&hm=a7df625b3e7a7a4e54cf9f3381ca41e8c1c2edd1e3cd70467c8604b3b453daad&=&format=webp&quality=lossless&width=688&height=309)


<br>
<br>

# Implementación de Soluciones Personalizadas para cada Departamento de la organización


## Departamentos y Aplicaciones Especializadas

Se han implementado soluciones personalizadas para los siguientes departamentos:

### 1. Ventas

* **Aplicación:** Aplicación de Ventas

    ![imagen](https://media.discordapp.net/attachments/1156413197931249765/1352673273900433499/image.png?ex=67dedea7&is=67dd8d27&hm=451a7233cf2670c73c42a87114f638c337c43f1a5721c887f877e422635c7a45&=&format=webp&quality=lossless&width=1860&height=603)
* **Funcionalidades:**
    * Gestión centralizada de oportunidades y leads.
    * Gestión de compradores y órdenes de compra.
    * Dashboard interactivo con cotizaciones enviadas y pendientes.
    * Registro de actividad comercial y reuniones con clientes.
* **Roles con Acceso:**
    * CEO
    * Gerente de Ventas
    * Administrador de Ventas
    * Ejecutivo de Ventas
* **Vista Personalizada en Leads:**
    * Se ha creado una vista personalizada llamada "Leads que no han sido contactados" para facilitar el trabajo del equipo de ventas.

    ![imagen](https://media.discordapp.net/attachments/936302388053168179/1352661065120485517/image.png?ex=67ded349&is=67dd81c9&hm=3f710169aac36cd1aeb0cebc806ed7631c6789225ee38edfbeb14a9e048b55b6&=&format=webp&quality=lossless&width=1796&height=800)

### 2. Producción

* **Aplicación:** Aplicación de Producción

    ![imagen](https://media.discordapp.net/attachments/1156413197931249765/1352701297488298186/image.png?ex=67def8c1&is=67dda741&hm=53ee2e3f18ddb5d520e0a4daa6b41f774d4a5aa96a31b5624eb6575b42487c06&=&format=webp&quality=lossless&width=1860&height=640)
* **Funcionalidades:**
    * Gestión de órdenes de producción.
    * Seguimiento de inventario de materias primas y productos terminados.
    * Programación de la producción.
    * Control de calidad.
* **Roles con Acceso:**
    * CEO
    * Gerente de Producción


### 3. Soporte

* **Aplicación:** Aplicación de Soporte

    ![imagen](https://media.discordapp.net/attachments/936302388053168179/1352662396623126661/image.png?ex=67ded486&is=67dd8306&hm=73f3c09a89dc77095191e17aceecc61e45754e090ad55a8bebe7c3703404771d&=&format=webp&quality=lossless&width=1860&height=638)

* **Funcionalidades:**
    * Gestión de casos de soporte.
    * Seguimiento de tickets.
    * Base de conocimientos.
    * Informes de rendimiento del equipo de soporte.
* **Roles con Acceso:**
    * CEO
    * Gerente de Soporte
    * Coordinador de Soporte
    * Técnico de Ensamblaje

## Consideraciones Importantes

* **Acceso Exclusivo:** Cada aplicación es accesible únicamente por los miembros del departamento correspondiente, garantizando la seguridad y privacidad de la información.
* **Personalización:** Las aplicaciones están personalizadas para satisfacer las necesidades específicas de cada departamento, optimizando los procesos y la productividad.
* **Vistas Personalizadas:** Se crean vistas personalizadas en los objetos relevantes para facilitar el trabajo de los usuarios, como la vista "Leads que no han sido contactados" en el departamento de ventas.


## Validación de Correos Electrónicos en Leads y Contactos

Se ha implementado una regla de validación para los campos de correo electrónico en los objetos de "Lead" y "Contacto", previniendo la creación de registros con correos inválidos que podrían afectar negativamente las oportunidades de negocio futuras.

Se validan los siguientes aspectos de una dirección de correo electrónico:

* **Parte local (antes de la "@"):**
    * Permite caracteres alfanuméricos (a-z, A-Z, 0-9).
    * Permite los siguientes caracteres especiales: punto (.), guión bajo (_), porcentaje (%), signo más (+), y guión (-).
* **Símbolo "@":**
    * Asegura que la dirección contenga el símbolo "@".
* **Nombre de dominio:**
    * Permite caracteres alfanuméricos y guiones (-).
    * Permite subdominios opcionales.
* **Dominio de nivel superior (TLD):**
    * Asegura que el TLD contenga al menos dos letras.
    * Ejemplos de TLDs validos: .com, .net, .org, .co

**Nombre de la regla de validación:** `Validacion_correo`

**Importancia:**

* Reduce el riesgo de enviar correos electrónicos a direcciones inválidas.
* Optimiza la comunicación con clientes potenciales y contactos.


## Validación de Números de Teléfono en Contactos, Leads y Cuentas

Se ha implementado una regla de validación en los campos de números de teléfono de los objetos "Contacto", "Lead" y "Cuenta". Asegurando que los números de teléfono sigan el formato internacional estándar.

Exige que los números de teléfono cumplan con el siguiente formato:

* **"+" (Signo más):** El número debe comenzar con el signo "+", indicando una llamada internacional.
* **Código de país:** Después del "+", debe haber un código de país de 1 a 3 dígitos.
* **Número local:** El resto del número de teléfono puede contener cualquier cantidad de dígitos.

**Nombre de la regla de validación:** `Validacion_telefono`


**Importancia:**

* Reduce el riesgo de errores al marcar números de teléfono.
* Facilita la integración con sistemas de telefonía y otras aplicaciones.



## Implementación de Reglas de Coincidencia y Duplicados para Leads, Contactos y Cuentas

Se han implementado reglas de coincidencia y duplicados para prevenir la creación de registros duplicados en los objetos Lead, Contacto y Cuenta, asegurando la integridad de los datos.

### Reglas de Coincidencia (Matching Rules)

#### 1. Regla de Coincidencia para Contactos

* **Objeto:** Contacto
* **Descripción:** Comparamos nombres, apellidos y dirección similares. Email exacto.
* **Criterios de Coincidencia:**
    * Apellido: Coincidencia aproximada. 
    * Nombre: Coincidencia aproximada.
    * Dirección (MailingStreet): Coincidencia aproximada.
    * Correo Electrónico: Coincidencia exacta.

#### 2. Regla de Coincidencia para Leads

* **Objeto:** Lead
* **Descripción:** Comparamos nombres y apellidos similares, email exacto y que el nombre de la compañía sea similar.
* **Criterios de Coincidencia:**
    * Nombre: Coincidencia aproximada.
    * Apellido: Coincidencia aproximada .
    * Correo Electrónico: Coincidencia exacta.
    * Compañía: Coincidencia aproximada.

#### 3. Regla de Coincidencia para Cuentas

* **Objeto:** Cuenta
* **Descripción:** Comparamos coincidencias parciales en nombre de cuenta, dirección, exactitud en numero de cuenta, tipo y telefono.
* **Criterios de Coincidencia:**
    * Nombre de la Cuenta: Coincidencia aproximada.
    * Dirección: Coincidencia aproximada.
    * Numero de Cuenta: Coincidencia exacta.
    * Tipo: Coincidencia exacta.
    * Telefono: Coincidencia exacta.


### Reglas de Duplicados (Duplicate Rules)

| Objeto  | Nombre de la Regla          | Seguridad a Nivel de Registro                               | Acción a Ejecutar                                                               | Regla de Coincidencia |
| :------ | :-------------------------- | :----------------------------------------------------------- | :------------------------------------------------------------------------------ | :-------------------- |
| Lead    | Duplicate rule block leads  | Compara sólo los registros a los que el usuario tiene acceso. | Bloquear la creación y edición si se encuentran coincidencias parciales. | leads\_duplicados     |
| Contacto | Duplicate rule block contacts | Compara sólo los registros a los que el usuario tiene acceso. | Bloquear la creación y edición si se encuentran coincidencias parciales. | contactos duplicados  |
| Cuenta  | Duplicate rule block accounts | Compara sólo los registros a los que el usuario tiene acceso. | Bloquear la creación y edición si se encuentran coincidencias parciales. | cuentas\_duplicadas   |

<br/>


# Creación de un mecanismo de respaldo y recuperación de datos

* **Respaldo Automático Diario:**
    * Se ha configurado la función de "Exportación de Datos" de Salesforce para realizar respaldos automáticos cada 24 horas.
    * Esta exportación incluye todos los datos de la organización, incluyendo:
        * Registros de objetos estándar y personalizados.
        * Imágenes, documentos y archivos.
    * Los archivos de respaldo se generan en formato CSV y se almacenan en un servidor seguro.
* **Respaldo Mensual Completo:**
    * Adicionalmente, se genera un archivo de respaldo completo al final de cada mes, a las 2:00 AM.
    * Este archivo contiene una copia consolidada de todos los datos respaldados durante el mes.
    * El archivo mensual se envía automáticamente al Administrador de Salesforce por correo electrónico.
* **Restauración de Datos:**
    * La restauración de datos solo puede ser realizada por el Administrador de Salesforce.
    * El Administrador utilizará la herramienta "Data Loader" o "Workbench" para importar los datos desde los archivos de respaldo.
    * Se ha establecido un protocolo de restauración que incluye:
        * Verificación de la integridad de los archivos de respaldo.
        * Pruebas de restauración en un entorno sandbox antes de la restauración en producción.
        * Documentación detallada del proceso de restauración.

![Configuración data export](https://media.discordapp.net/attachments/1145930948140077106/1351980873230057584/image.png?ex=67defcce&is=67ddab4e&hm=2e01f1bc627391cdae436b9d76008e046c1e3bdc1bcff455958ca38e8636a220&=&format=webp&quality=lossless)

<br>
<br>

# Auditorías de Inicio de Sesión de Usuarios

## Introducción

Este documento describe la generación de un reporte de auditoría de inicios de sesión de usuarios de la organización, que se actualiza mensualmente y se envía automáticamente al CEO.

## Reporte de Auditoría de Inicios de Sesión

* Se genera un reporte de auditoría que registra los inicios de sesión de los usuarios en la organización.
* El reporte incluye información como:
    * Nombre de usuario.
    * Fecha y hora del inicio de sesión.
    * Dirección IP desde la que se inició la sesión.
    * Dispositivo utilizado para el inicio de sesión.
    * Resultado del inicio de sesión (éxito o fallo).
* El reporte se actualiza automáticamente cada 30 días.
* El CEO está suscrito al reporte y lo recibe automáticamente por correo electrónico cada mes.

## Configuración

* La generación del reporte y la suscripción del CEO se configuran en la sección de informes y dashboards de Salesforce.
* Se utiliza el tipo de informe "Historial de inicio de sesión" para crear el reporte de auditoría.
* Se programa la actualización del reporte para que se ejecute mensualmente.
* Se configura la suscripción del CEO al reporte, especificando la frecuencia de envío (mensual) y el formato del correo electrónico.

![Reporte de Auditoría de Inicios de Sesión](https://media.discordapp.net/attachments/936302388053168179/1352661524321144883/image.png?ex=67ded3b6&is=67dd8236&hm=87a345861e5f8b3ec6088d07c32b65520708d3ab28e6942925a9ace0b98268f8&=&format=webp&quality=lossless)

<br/>

## Políticas de Contraseñas (Password Policies)

* Se implementaron políticas de contraseñas para garantizar la seguridad de las credenciales de los usuarios.
* Las políticas incluyen los siguientes requisitos:
    * Longitud mínima de la contraseña.
    * Complejidad de la contraseña (combinación de letras, números y caracteres especiales).
    * Expiración de la contraseña y necesidad de cambio periódico.
    * Historial de contraseñas para evitar la reutilización.
* Estas políticas se aplican a todos los usuarios de la organización.

## Seguimiento del Historial de Datos (History Tracking)

* Se activó el seguimiento del historial de datos en los objetos "Oportunidades" y "Cuentas".
* El seguimiento del historial permite registrar los cambios realizados en campos críticos de estos objetos.
* Esto proporciona una pista de auditoría para el seguimiento de cambios importantes y la identificación de posibles problemas.
* Los campos críticos que se rastrean incluyen:
    * Monto de la oportunidad.
    * Etapa de la oportunidad.
    * Nombre de la cuenta.
    * Dirección de la cuenta.
* El historial de cambios se almacena y se puede consultar para fines de auditoría y análisis.

<br/>

# Flujos y procesos automatizados

##  Asignación Automática de Leads: Notificación al Gerente de Ventas


Se ha implementado la notificación automática al Gerente de Ventas mediante la creación de un Flow, un Email Template y un Email Alert.

* **Flow (Flujo):**
    * El Flow se activa cuando se crea un nuevo registro de Lead.
    * El Flow utiliza un Email Alert para enviar una notificación al Gerente de Ventas.

* **Email Template (Plantilla de Correo Electrónico):**
    * Se ha creado una plantilla de correo electrónico personalizada para la notificación.
    * La plantilla incluye información relevante del Lead, como el nombre, la empresa y el asunto.

* **Email Alert (Alerta de Correo Electrónico):**
    * Se ha creado un Email Alert que utiliza la plantilla de correo electrónico creada.
    * El Email Alert se configura para enviar el correo electrónico al usuario obtenido por el Flow, que es el Gerente de Ventas.
    * El Email Alert se activa desde el Flow cuando se crea un nuevo Lead.

![imagen flujo](https://media.discordapp.net/attachments/1156413197931249765/1352012090872959057/imagen.png?ex=67dc76e1&is=67db2561&hm=62834fe71fb8b312c92ad0dde9b46c5c335687e970629bf47956d83d33956b6c&=&format=webp&quality=lossless)


## Imagen de ejemplo
![ejemplo](https://media.discordapp.net/attachments/1145930948140077106/1351422057266548767/Screenshot_20250318-000814.jpg?ex=67deee9e&is=67dd9d1e&hm=ea2304c443eb645a5bc6859433ef3d220d0c3a88424cb2911439604b3b52a6d9&=&format=webp&width=393&height=895)



## Conversión Automática de Lead a Oportunidad

Se ha implementado la conversión automática de Lead a Oportunidad mediante la creación de un Flow activado por registros en el objeto Lead.

* **Flow (Flujo):**
    * El Flow se activa cuando se crea o actualiza una tarea.
    * El Flow obtiene las interacciones del Lead.
    * Si el Lead tiene menos de 3 interacciones, se actualiza el registro del Lead.
    * Si el Lead tiene 3 interacciones, se convierte automáticamente en una Oportunidad.
    * se establece una condición para dejar de iterar las interacciones cuando ya es una oportunidad.
    * Si la conversión a Oportunidad es exitosa, se genera automáticamente una propuesta comercial.

![imagen flujo](https://media.discordapp.net/attachments/1156413197931249765/1352012090872959057/imagen.png?ex=67dc76e1&is=67db2561&hm=62834fe71fb8b312c92ad0dde9b46c5c335687e970629bf47956d83d33956b6c&=&format=webp&quality=lossless)


## Notificación al Gerente de Soporte por Caso Crítico

Se ha implementado la notificación al Gerente de Soporte cuando se crea un Caso Crítico mediante la creación de un Flow activado por registros en el objeto Caso.

* **Flow (Flujo):**
    * El Flow se activa cuando se crea un nuevo registro de Caso.
    * El Flow verifica si el Caso es Crítico.
    * Si el Caso es Crítico, se envía una Alerta de Correo Electrónico al Gerente de Soporte.

![flujo](https://media.discordapp.net/attachments/1156413197931249765/1352012457736146984/imagen.png?ex=67dc7739&is=67db25b9&hm=89fd6bce1519c052e5ebf4c145a44979f753a5e3d3a0e191144d75fbfb48b883&=&format=webp&quality=lossless)

## Imagen de ejemplo
![ejemplo](https://media.discordapp.net/attachments/1156413197931249765/1351644285644050665/Screenshot_20250318-145130.jpg?ex=67de6c16&is=67dd1a96&hm=beee360d519a3e74c5947ed423c67c056107679e49a0533a9b8f0e5468c01b16&=&format=webp&width=393&height=895)

<br/>

## Envío de Factura al Cerrar Oportunidad Ganada

Se ha implementado el envío automático de factura al cerrar una oportunidad como ganada mediante la creación de un Flow activado por registros en el objeto Oportunidad.

* **Flow (Flujo):**
    * El Flow se activa cuando se actualiza un registro de Oportunidad y la etapa cambia a "Cerrado Ganado".
    * El Flow genera una factura.
    * El Flow obtiene el contacto asociado a la oportunidad.
    * Si el contacto está disponible y tiene correo electrónico, se envía la factura al contacto.
    * Si el contacto no está disponible o no tiene correo electrónico, se verifica si la cuenta asociada tiene correo electrónico.
    * Si la cuenta tiene correo electrónico, se envía la factura al correo electrónico de la cuenta.
    * Si la cuenta no tiene correo electrónico, se envía la factura al usuario que atiende la oportunidad.
    * Se realiza una prueba de envío al administrador.

![flujo](https://media.discordapp.net/attachments/1156413197931249765/1352036169772433471/AN12HXTaPD_NU_omcYUWZ-ppueZRHh3CRAa9So1vsqrbdv-xzuGqb7OfbhBg-KBC4z2ogQHihztN-nFKNDXYsKpp-TCcZS_aSRV_MBSHjnWi81pyJBFkaIGDolcR35IEtWKhje8APt-eLt2alOLfbnZKmrHDFd5enKLkxdYhpWe6l1feKTWRUvysexVRpZXId-m6KP7vj9NMXjqOG521rK00miaxf34GGHPaVcLrElL2AxNOEzLy2ufREwnfvIxmBPm2E_9FtMaCvsWy6Kzt8wVzMxNOL6CESJ4cYAd.png?ex=67dc8d4e&is=67db3bce&hm=0daa2167793abcf814e2dace6b29793dd7afad09e7fdee9bd870c579510d5cec&=&format=webp&quality=lossless)

## Imagen de ejemplo
![ejemplo](https://media.discordapp.net/attachments/1156413197931249765/1352702094611583036/IMG-20250319-WA0101.jpg?ex=67def97f&is=67dda7ff&hm=fedbfd7030374dffadcdf731b0b7c6698c7351810989a297d65769ac33443ef2&=&format=webp&width=393&height=896)


## Proceso de Verificación

1.  **Descarga de Salesforce Mobile:**
    * Se descargó la aplicación Salesforce Mobile desde la tienda de aplicaciones correspondiente (App Store o Google Play).

2.  **Inicio de Sesión:**
    * Se inició sesión en la aplicación Salesforce Mobile utilizando las credenciales del usuario Gerente de Ventas.

3.  **Verificación de Aplicaciones Disponibles:**
    * Se verificó que la única aplicación disponible para el usuario Gerente de Ventas fuera la aplicación de ventas.
    * Se comprobó que no se mostraran otras aplicaciones, como las de soporte, producción o compras.

4.  **Navegación en la Aplicación de Ventas:**
    * Se navegó por las diferentes secciones de la aplicación de ventas para verificar que todas las funcionalidades estuvieran accesibles para el Gerente de Ventas.
    * Se comprobó el acceso a oportunidades, leads, contactos, cuentas y otras funcionalidades relevantes.

## Imagen de Ejemplo

![Salesforce Mobile - Aplicación de Ventas](https://media.discordapp.net/attachments/1156413197931249765/1352723971136688209/Screenshot_20250321-142139.jpg?ex=67df0ddf&is=67ddbc5f&hm=9b3cc1f3b1e83ce25e8c0c2496e1701b4318e1c6696433e5c4af191ba591f24b&=&format=webp&width=393&height=895)


<br/>
