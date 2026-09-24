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