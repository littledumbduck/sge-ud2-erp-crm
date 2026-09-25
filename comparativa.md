## 2. Licencias y modelos

### Diferenciación de modelos de software

* **Software Libre (FSF - Free Software Foundation):**
  Definido desde una perspectiva ética y filosófica por la Free Software Foundation centrada en los derechos y libertades del usuario. Para ser considerado software libre, debe garantizar las cuatro libertades fundamentales:
  1. *Libertad 0:* Ejecutar el programa con cualquier propósito.
  2. *Libertad 1:* Estudiar cómo funciona el programa y modificarlo para adaptarlo a las necesidades (acceso obligatorio al código fuente).
  3. *Libertad 2:* Redistribuir copias para ayudar a otros.
  4. *Libertad 3:* Distribuir copias de versiones modificadas para beneficio de toda la comunidad.
  *Fuente:* [Free Software Foundation - What is Free Software?](https://www.gnu.org/philosophy/free-sw.html) En la fuente, se cita desde la web del Sistema Operativo GNU, un sistema operativo código abierto dentro de la iniciativa de Free Software Foundation (https://www.fsf.org/).

* **Código Abierto (OSI - Open Source Initiative):**
  Definido mediante la *Open Source Definition* (OSD) a través de 10 criterios (redistribución libre, acceso al código fuente, permitir trabajos derivados, no discriminación de personas o grupos, entre otros). Su enfoque es técnico, metodológico y pragmático: promueve el código abierto como un modelo de desarrollo colaborativo superior que aporta robustez, auditoría comunitaria y agilidad al software empresarial.
  *Fuente:* [Open Source Initiative - The Open Source Definition](https://opensource.org/osd)

* **Software Propietario (Privativo):**
  Aquel cuyo código fuente es privado y cerrado. Los derechos de autor y explotación pertenecen en exclusiva al fabricante. El usuario adquiere únicamente una licencia o derecho de uso limitado bajo un contrato (EULA/Términos de servicio), quedando prohibida su modificación, distribución, redistribución o ingeniería inversa.
  *Fuente:* Diapositivas de la unidad (Tema 2 - Sistemas ERP-CRM).

---

### ¿Por qué «libre» no significa «gratuito»?

La expresión histórica de la FSF lo resume claramente: *«Free software is a matter of liberty, not price. Think of free as in free speech, not free beer»* (libre como en libertad de expresión, no gratuito como una cerveza de cortesía).

La libertad define los derechos de acceso, auditoría y modificación del código fuente por parte del usuario, no el precio financiero de venta o adquisición. En el ecosistema empresarial:
* El software libre puede venderse o cobrarse por su distribución inicial o por servicios asociados (instalación, parametrización, desarrollo a medida, formación y soporte técnico).
* El coste total de propiedad (TCO) nunca es cero: requiere inversión en infraestructura (servidores, redes), mantenimiento preventivo, seguridad, copias de seguridad y tiempo de personal técnico.

---

### Consecuencias prácticas de las licencias: Copyleft y AGPL en uso por red

* **Copyleft (fuerte frente a débil):**
  * *Copyleft fuerte (GPL):* Exige que cualquier trabajo derivado o modificación que se distribuya mantenga obligatoriamente la misma licencia libre original.
  * *Copyleft débil / permisivo (LGPL):* Como en **Odoo Community** o **ERPNext** (licencia GNU LGPLv3), permite enlazar módulos o librerías externas sin obligar a que todo el software dependiente adopte la misma licencia, facilitando el desarrollo de módulos comerciales complementarios.
* **AGPL (GNU Affero General Public License) y el uso por red:**
  * Las licencias GPL tradicionales cerraban el requisito de liberación al concepto clásico de «distribución» de binarios. En entornos Cloud/SaaS, muchas empresas evitaban liberar mejoras porque el software se ejecutaba en servidores remotos sin distribuirse físicamente al cliente.
  * La cláusula 13 de la licencia **AGPLv3** (utilizada, por ejemplo, en **SuiteCRM**) soluciona esta brecha obligando a que cualquier modificación realizada en un software que ofrezca servicios interactivos a través de una red deba ponerse a disposición de los usuarios remotos con su código fuente completo.

---

### Implicaciones prácticas: Edición Community frente a Enterprise

El sector de los ERP y CRM abiertos utiliza frecuentemente el modelo de negocio **Open Core**:

| Aspecto | Edición Community | Edición Enterprise |
| :--- | :--- | :--- |
| **Licenciamiento** | Libre / Código abierto (ej. LGPLv3). | Propietaria / Comercial por suscripción. |
| **Coste de licencias** | Sin coste por licencias de usuario. | Pago periódico por usuario/mes o módulos activos. |
| **Soporte y garantías** | Sin garantía formal del desarrollador; soporte autogestionado o comunitario. | Soporte oficial del fabricante con SLAs, parches y resolución de incidencias. |
| **Funcionalidades** | Núcleo operativo estándar y módulos básicos esenciales. | Módulos avanzados (contabilidad localizada completa, apps móviles nativas, automatizaciones avanzadas, conectores bancarios). |
| **Mantenimiento y actualización**| Las migraciones de versión y parches corren a cargo de la empresa. | Herramientas automatizadas de migración y soporte asistido de versión por el proveedor. |

---

## 3. Fichas técnicas

### 1. ERP Libre: Odoo Community

* **Licencia exacta:** GNU LGPLv3 (GNU Lesser General Public License v3.0).
* **Versión vigente:** Odoo 18.0 (rama estable actual).
* **Lenguaje del servidor:** Python (versión 3.10 o superior).
* **SGBD compatibles:** PostgreSQL (versión 13.0 o superior).
* **Modalidad:** Instalación local (*on-premise*), autoalojado en servidor propio/VPS o en contenedores Docker.
* **Módulos principales:** Ventas, CRM, Facturación estándar, Compras, Inventario, Punto de Venta (PoS), Fabricación básica y Gestión de Proyectos.
* **Requisitos mínimos del sistema:**
  * CPU: 2 vCPU recomendadas para entornos estándar de producción.
  * Memoria RAM: Mínimo 2 GB (4 GB a 8 GB recomendados según concurrencia).
  * Almacenamiento: 10 GB de espacio en disco más volumen para base de datos y adjuntos.
  * Sistema Operativo: Distribuciones Linux basadas en Debian/Ubuntu recomendadas.
* **Fuente oficial y fecha de consulta:**
  * [Odoo GitHub Repository & Technical Documentation](https://github.com/odoo/odoo) (Fecha de consulta: 24 de septiembre de 2026).

---

### 2. ERP Propietario: Microsoft Dynamics 365 (Business Central)

* **Licencia exacta:** Propietaria / Comercial por suscripción de usuario (SaaS por usuario/mes: licencias *Essentials* o *Premium*).
* **Versión vigente:** 29.0 Preview, Application Build 29.0 Update 29.0 for Business Central 2026 release wave 2.
* **Lenguaje del servidor:** Lenguaje AL ejecutado sobre el entorno de ejecución .NET Core / Azure Services.
* **SGBD compatibles:** Microsoft Azure SQL Database (en modalidad SaaS administrada por Microsoft); Microsoft SQL Server en despliegues locales (*on-premise*).
* **Modalidad:** Principalmente Nube (SaaS en Microsoft Azure), con opción de despliegue híbrido o local (*on-premises*).
* **Módulos principales:** Gestión financiera y contable, Cadena de suministro, Gestión de inventario y almacén, Ventas y cobros, Compras y pagos, Gestión de proyectos y Fabricación/Servicios (en edición Premium).
* **Requisitos mínimos del sistema:**
  * Modalidad SaaS: Navegador web moderno compatible (Microsoft Edge, Google Chrome) y conexión a internet.
  * Modalidad On-Premise: Servidor con Windows Server 2022/2025, 4 núcleos x64, 16 GB RAM y Microsoft SQL Server 2019/2022 Standard o Enterprise.
* **Fuente oficial y fecha de consulta:**
  * [Microsoft Learn: Documentación de Dynamics 365 Business Central](https://learn.microsoft.com/es-es/dynamics365/business-central/) (Fecha de consulta: 24 de septiembre de 2026). ACLARACIÓN: este es el enlace oficial de la documentación de Microsoft Dynamics 365 Business Central. También encuentro el link de la versión general (https://learn.microsoft.com/es-es/dynamics365/) donde encuentro más información que he ido contrastando para poder encontrar toda la información relevante para poder rellenar el apartado. Para más info también consulto con webs externas ya que veo toda la información bastante ambigüa (https://www.davisa.es/business-central-espana-guia-2026/)

---

### 3. CRM Libre: SuiteCRM

* **Licencia exacta:** GNU AGPLv3 (GNU Affero General Public License v3.0).
* **Versión vigente:** SuiteCRM 8.10.2 7.15.2 security maintenance release.
* **Lenguaje del servidor:** PHP (PHP 8.2 / 8.3) sobre el framework Symfony en el backend.
* **SGBD compatibles:** MySQL (8.0+) y MariaDB (10.6+).
* **Modalidad:** Instalación local (*on-premise*), servidor web privado (Apache/Nginx) o nube privada autogestionada.
* **Módulos principales:** Cuentas y Contactos, Oportunidades de venta, Clientes potenciales (*Leads*), Casos/Tickets de atención al cliente, Campañas de marketing por correo, Cotizaciones y Gestión de proyectos comerciales.
* **Requisitos mínimos del sistema:**
  * Servidor Web: Apache 2.4 o Nginx con extensiones PHP (`php-mbstring`, `php-zip`, `php-gd`, `php-curl`, `php-xml`).
  * CPU: 2 núcleos x86_64.
  * Memoria RAM: Mínimo 4 GB.
  * Espacio en disco: Mínimo 10 GB (SSD recomendado).
* **Fuente oficial y fecha de consulta:**
  * [SuiteCRM Official Documentation & Release Notes](https://docs.suitecrm.com/) (Fecha de consulta: 24 de septiembre de 2026). 

---

### 4. CRM Propietario: Salesforce Sales Cloud

* **Licencia exacta:** Propietaria / Suscripción Cloud multi-inquilino (*Multi-tenant SaaS*) bajo contrato de servicio cerrado.
* **Versión vigente:** Salesforce Summer / Winter '26 Release (actualizaciones automáticas continuas en la plataforma Lightning).
* **Lenguaje del servidor:** Apex (lenguaje propietario orientado a objetos ejecutado en la plataforma multi-tenant de Salesforce Force.com).
* **SGBD compatibles:** Base de datos relacional propietaria en la nube gestionada internamente por la infraestructura de Salesforce (arquitectura basada en clústeres Oracle y tecnologías de almacenamiento distribuido administradas; no accesible directamente por el usuario).
* **Modalidad:** 100% Nube (SaaS).
* **Módulos principales:** Gestión de cuentas y contactos (*Lead & Contact Management*), Flujos de canal de ventas (*Opportunity Management*), Previsión de ventas (*Sales Forecasting*), Automatización del flujo de trabajo (*Process Builder & Flow*), Automatización de marketing y Analítica predictiva (Einstein AI).
* **Requisitos mínimos del sistema:**
  * No requiere infraestructura ni instalación en servidor por parte del cliente.
  * Cliente: Navegador web actualizado (Google Chrome, Microsoft Edge, Mozilla Firefox) y conexión a internet de banda ancha.
* **Fuente oficial y fecha de consulta:**
  * [Salesforce Sales Cloud Technical Overview & Help](https://developer.salesforce.com/docs) (Fecha de consulta: 24 de septiembre de 2026). Documentación bastante simple de recopilar ya que la web cuenta con una IA la cual resuelve todo tipo de dudas sobre el software.

  ---
  ---

  ## 5. Fe de erratas

  * **Errata 1**: En la diapositiva 3, en el título marca Software Libre vs Propietario. Sin embargo, luego en el cuerpo no habla sobre el software libre, sino el de código abierto.

  * **Errata 2**: En la diapositiva 7, las capturas de pantalla de las interfaces de los programas mencionados no corresponden a los programas reales, sino a imágenes generadas por Inteligencia Artificial simulando las interfaces.

  * **Errata 3**: En la diapositiva 9, dice que SuiteCRM fue desarrollado por la comunidad SugarCRM. Realmente fue desarrollado en 2013 por Sales Agility.