# Propuesta de análisis de riesgos

> **Estado:** propuesta docente sencilla, pendiente de revisión. Las valoraciones son iniciales; deben validarse con responsables, inventarios y evidencias de la organización.

## 1. Contexto, objetivo y alcance

La empresa asesora a personas autónomas y pymes, tiene 150 personas empleadas en dos sedes y quiere ampliar su actividad digital. Para mantener el ejercicio acotado, se elige como alcance el proceso de atención y prestación de servicios a clientes, junto con sus dependencias principales: datos de clientes, CRM/ERP, correo, servidores de archivos, web y tienda en línea, nube, copias de seguridad y proveedores relevantes. El análisis se centra en proteger la información y mantener ese proceso.

Se consideran las dos sedes, los procesos y las personas, los equipos, servidores, redes, sistemas CRM/ERP, correo, almacenamiento en la nube, web y tienda en línea, además de los proveedores externos que prestan servicios relevantes. No se presupone que una medida esté ausente cuando la descripción no lo confirma; esos puntos se marcan para verificar.

## 2. Método de valoración

La guía de INCIBE propone seis fases: definir el alcance; identificar activos; identificar amenazas; identificar vulnerabilidades y salvaguardas; evaluar el riesgo; y tratarlo. Para esta propuesta, la valoración se mantiene sencilla y usa los conceptos de activo, amenaza, vulnerabilidad, impacto y probabilidad. El nivel de riesgo se estima como:

> **Riesgo = Probabilidad × Impacto**

Para mantener el ejercicio sencillo se adapta la valoración a tres niveles:

| Nivel | Probabilidad | Impacto |
|---|---|---|
| 1 - Bajo | El escenario parece poco probable con la información disponible. | Efecto limitado y recuperable en poco tiempo. |
| 2 - Medio | El escenario es posible. | Interrupción o pérdida relevante, pero acotada. |
| 3 - Alto | El escenario es probable o existen debilidades que lo favorecen. | Puede afectar de forma grave a la actividad, a datos protegidos, a clientes o a la reputación. |

| Resultado | Prioridad didáctica |
|---|---|
| 1-2 | Bajo: mantener controles y revisar. |
| 3-4 | Medio: planificar una mejora y hacer seguimiento. |
| 6-9 | Alto: priorizar su tratamiento. |

Impacto considera la confidencialidad, integridad y disponibilidad, así como interrupción del servicio, obligaciones legales, costes y confianza de clientes. La escala de tres niveles es una adaptación para esta actividad, no una escala oficial de INCIBE. Las puntuaciones no sustituyen una valoración con datos reales.

## 3. Activos principales

| Activo | Tipo | Importancia para la actividad |
|---|---|---|
| Datos personales de clientes y proveedores | Información primaria | Su exposición o pérdida puede afectar a las personas, a las obligaciones legales y a la confianza. |
| Información de gestión, facturación, ventas y compras | Información y procesos | Es necesaria para prestar servicios y gestionar la empresa. |
| Propiedad intelectual y documentación de proyectos | Información primaria | Su modificación o divulgación puede causar perjuicios económicos y reputacionales. |
| CRM, ERP y aplicaciones internas | Aplicaciones y procesos | Soportan relaciones con clientes y procesos internos. |
| Servidores de archivos, aplicaciones y correo | Infraestructura y servicios | Permiten almacenar, compartir y procesar información. |
| Web y tienda en línea | Servicio externo y canal de negocio | Facilitan el contacto con clientes y forman parte de la estrategia de crecimiento digital. |
| Servicios de almacenamiento en la nube | Servicio y repositorio de información | Dan soporte al acceso y almacenamiento de datos fuera de las sedes. |
| Equipos de usuario y dispositivos móviles | Hardware y personas usuarias | Son puntos de acceso a la información y a los sistemas corporativos. |
| Redes, routers, Wi-Fi y cortafuegos | Comunicaciones | Conectan sedes, usuarios y servicios; una configuración incorrecta puede afectar a varios activos. |
| Copias de seguridad | Información y capacidad de recuperación | Permiten recuperar información y actividad tras un incidente. |
| Sedes y servicios de seguridad física | Instalaciones y terceros | Protegen equipos, documentación y personas frente a incidentes físicos. |

## 4. Controles y debilidades conocidas

La descripción de la actividad indica estos controles existentes:

- Las copias de seguridad las gestiona el personal TIC, se guardan en la sede principal y existe un procedimiento básico documentado.
- Una empresa externa gestiona el antivirus y su actualización. El procedimiento está documentado, pero no aprobado por la dirección.
- El cumplimiento del RGPD se ha abordado mediante una consultoría, está documentado y aprobado formalmente.
- El cortafuegos separa una zona segura y otra pública; la red está segmentada por departamentos.
- La seguridad física está externalizada en ambas sedes.

Debilidades conocidas o aspectos que deben comprobarse:

- No existen políticas de seguridad por escrito.
- La web está externalizada y la empresa no tiene visibilidad suficiente de su estado de securización.
- El conocimiento sobre la información del cortafuegos y la segmentación depende de la persona administradora de red.
- No se indica si las copias están fuera de la sede principal, protegidas frente a modificación o probadas mediante restauraciones.
- Deben verificarse medidas de acceso a cuentas, uso de autenticación multifactor, gestión de permisos, actualizaciones, registros, configuración de la nube, control de visitas y compromisos de seguridad de los proveedores. No se afirma que estas medidas falten: la descripción no aporta esa evidencia.

## 5. Evaluación de cuatro escenarios prioritarios

Cada escenario relaciona un activo con una amenaza que puede aprovechar una vulnerabilidad y generar una consecuencia.

| ID | Activo + amenaza + vulnerabilidad → consecuencia | P | I | Riesgo | Justificación inicial |
|---|---|---:|---:|---:|---|
| R1 | Servidores de archivos y aplicaciones + ransomware + las copias se almacenan en la sede principal y no consta si se prueban las restauraciones → indisponibilidad de información y procesos de atención a clientes. | 2 | 3 | 6 - Alto | El antivirus está actualizado por un proveedor, pero una infección que alcance los sistemas y las copias tendría un impacto grave. |
| R2 | Web y tienda en línea + ataque o fallo del proveedor + falta de visibilidad de la seguridad del servicio externalizado → exposición de datos o interrupción del canal de atención y venta. | 2 | 3 | 6 - Alto | La dependencia externa y la falta de visibilidad están descritas; hay que concretar controles y compromisos del proveedor. |
| R3 | Datos personales y de negocio en correo, CRM/ERP o nube + robo o uso indebido de credenciales + normas de seguridad no formalizadas y controles de acceso/MFA pendientes de verificar → acceso no autorizado o divulgación de información. | 2 | 3 | 6 - Alto | El impacto potencial es alto por el tipo de información. La probabilidad es provisional hasta comprobar los controles de identidad y acceso. |
| R4 | Copias de seguridad y sistemas de la sede principal + incendio, fallo grave o incidente que afecte a la sede + copias conocidas ubicadas en la misma sede → pérdida simultánea de sistemas y capacidad de recuperación. | 2 | 3 | 6 - Alto | La ubicación de las copias sí está descrita; la existencia de otras copias o medidas de continuidad debe confirmarse. |

Las puntuaciones ordenan el trabajo, no son mediciones estadísticas. Deben revisarse si el equipo obtiene información nueva. En particular, R1 y R4 deben analizarse sin dar por hecho que no existen copias adicionales o pruebas de restauración. El conocimiento concentrado sobre la red y los controles de acceso físico quedan como aspectos a verificar si se amplía el alcance.

## 6. Tratamiento recomendado y riesgo residual estimado

| ID | Tratamiento y medidas propuestas | Estimación residual orientativa |
|---|---|---|
| R1 | **Reducir:** aprobar políticas básicas; revisar actualizaciones y protección de equipos; limitar privilegios; mantener una copia separada y protegida frente a modificación; probar restauraciones y preparar una respuesta a ransomware. | P=1, I=3 → 3, medio. Aunque baje la probabilidad, el impacto de un incidente grave seguiría siendo alto. |
| R2 | **Reducir y compartir:** acordar con el proveedor las responsabilidades de seguridad, las actualizaciones, las copias, la notificación de incidentes y la recuperación; solicitar evidencias periódicas y revisar dependencias. | P=1, I=3 → 3, medio. Sigue existiendo dependencia de un servicio externo. |
| R3 | **Reducir:** formalizar normas de acceso; verificar MFA en servicios críticos; aplicar mínimo privilegio y revisar permisos; registrar accesos relevantes; formar al personal y revisar el acceso a datos en la nube. | P=1, I=3 → 3, medio. El impacto potencial de una exposición de datos no desaparece. |
| R4 | **Reducir:** disponer de copias separadas de la sede principal, protegidas frente a borrado o cifrado; probar recuperación y documentar prioridades de continuidad. | P=1, I=3 → 3, medio. Una interrupción de la sede aún podría afectar a la actividad. |

El riesgo residual es una **estimación posterior a las medidas propuestas**, no una constatación de que ya estén implantadas. La decisión de aceptar un riesgo residual corresponde a la dirección, después de conocer su impacto y las medidas disponibles.

## 7. Conclusiones

Los activos más críticos son los datos personales y de negocio, la información de proyectos, los procesos soportados por CRM/ERP, los servidores de archivos y aplicaciones, la web y la tienda en línea, y las copias necesarias para recuperar la actividad.

Los escenarios que conviene priorizar son la indisponibilidad por ransomware y recuperación insuficiente (R1), la exposición o interrupción de web/tienda en línea externalizadas (R2), el acceso indebido a información mediante cuentas (R3) y la pérdida simultánea de sistemas y copias en la sede principal (R4). Sus puntuaciones son iniciales y deben ajustarse con evidencias.

Las debilidades confirmadas son la falta de políticas escritas, la escasa visibilidad sobre la seguridad de la web externalizada, la concentración del conocimiento de red y la ubicación de las copias en la sede principal. También debe aclararse si se realizan restauraciones de prueba y si existen copias separadas, autenticación multifactor, permisos revisados, registros suficientes y procedimientos de acceso físico.

Como punto de partida para el PDS, se recomienda priorizar la resiliencia de las copias y las pruebas de recuperación; acordar y revisar requisitos de seguridad con proveedores; formalizar reglas de acceso y respuesta a incidentes; y documentar la red y las responsabilidades. Para cada actuación, el PDS deberá concretar responsable, plazo, recursos e indicador de seguimiento.

## Referencias

- INCIBE, [Gestión de riesgos: una guía de aproximación para el empresario](https://www.incibe.es/sites/default/files/contenidos/guias/doc/guia_ciberseguridad_gestion_riesgos_metad.pdf), especialmente los conceptos de activo, amenaza, vulnerabilidad, impacto y probabilidad, la valoración `impacto × probabilidad` y las opciones de tratamiento.
- INCIBE, [¡Fácil y sencillo! Análisis de riesgos en 6 pasos](<Recursos/3.1. Análisis de riesgos en 6 pasos.pdf>).
- MAGERIT v3, *Libro II: Catálogo de elementos*, incluido en `Recursos/` como referencia complementaria.
