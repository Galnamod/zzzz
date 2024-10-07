## Registro_IPERC
**Semántica**: Registro que contiene los detalles de un IPERC asociado a un proceso específico, incluyendo fecha de registro y otros detalles.

| Atributo        | Naturaleza (tipo de valor) | Formato     | Valores válidos  | Unidad | Derivada de | Semántica (descripción)                           | Ontología (rol en el negocio)                              |
|-----------------|----------------------------|-------------|------------------|--------|-------------|--------------------------------------------------|------------------------------------------------------------|
| id_reg_iperc    | INT                        | 999999      | NOT NULL         | ----   | ----        | Identificador único del registro IPERC           | Control e identificación del IPERC                         |
| id_proceso      | INT                        | 999999      | NOT NULL         | ----   | ----        | Identificador del proceso asociado               | Relación con el proceso evaluado en el IPERC               |
| fecha_registro  | DATE                       | DD/MM/YYYY  | Fecha válida     | ----   | ----        | Fecha en la que se registró el IPERC             | Control de tiempo y versiones del IPERC                    |
| Cant_riesgos_analizados | INT                 | 9999        | ----             | ----   | ----        | Cantidad de riesgos evaluados en el IPERC        | Mide el alcance del análisis en un registro                |

---

## Equipo Evaluador
**Semántica**: Grupo de personas responsables de la evaluación de riesgos y de realizar el análisis de los mismos en el proceso IPERC.

| Atributo         | Naturaleza (tipo de valor) | Formato     | Valores válidos  | Unidad | Derivada de | Semántica (descripción)                               | Ontología (rol en el negocio)                              |
|------------------|----------------------------|-------------|------------------|--------|-------------|------------------------------------------------------|------------------------------------------------------------|
| id_equipo_evaluador | INT                      | 999999      | NOT NULL         | ----   | ----        | Identificador único del equipo evaluador             | Identificación del grupo evaluador                         |
| codigo_empleado  | INT                        | 999999      | NOT NULL         | ----   | ----        | Código del empleado que forma parte del equipo       | Relaciona el equipo evaluador con los empleados que lo integran |
| cant_empleados   | INT                        | 2 digitos   | NOT NULL         | ----   | ----        | Cantidad de empleados que conforman el equipo         | Indica el número de personas asignadas al equipo evaluador |

---

## Registro por Riesgos
**Semántica**: Relación de riesgos dentro del registro IPERC, identificando el análisis, la valoración y el plan de acción de mejora por cada riesgo.

| Atributo        | Naturaleza (tipo de valor) | Formato     | Valores válidos  | Unidad | Derivada de | Semántica (descripción)                           | Ontología (rol en el negocio)                              |
|-----------------|----------------------------|-------------|------------------|--------|-------------|--------------------------------------------------|------------------------------------------------------------|
| id_registro_riesgo | INT                        | 999999      | NOT NULL         | ----   | ----        | Identificador único del registro del riesgo      | Control e identificación del riesgo en el IPERC            |
| id_analisis     | INT                        | 999999      | NOT NULL         | ----   | ----        | Referencia al análisis del riesgo                | Relación directa con el análisis del riesgo evaluado       |
| id_valoracion_inicial | INT                    | 999999      | NOT NULL         | ----   | ----        | Referencia a la valoración inicial               | Relación directa con la valoración inicial del riesgo      |
| id_valoracion_residual | INT                  | 999999      | NOT NULL         | ----   | ----        | Referencia a la valoración residual              | Relación directa con la valoración final del riesgo        |
| id_plan_mejora  | INT                        | 999999      | NOT NULL         | ----   | ----        | Referencia al plan de acción de mejora           | Relación directa con el plan de mejora asignado al riesgo  |

---

## Proceso
**Semántica**: Unidad funcional dentro de la empresa en la que se lleva a cabo una serie de actividades relacionadas con el IPERC.

| Atributo        | Naturaleza (tipo de valor) | Formato     | Valores válidos  | Unidad | Derivada de | Semántica (descripción)                           | Ontología (rol en el negocio)                              |
|-----------------|----------------------------|-------------|------------------|--------|-------------|--------------------------------------------------|------------------------------------------------------------|
| id_proceso      | INT                        | 999999      | NOT NULL         | ----   | ----        | Identificador único del proceso                  | Control e identificación de procesos en el IPERC           |
| id_equipo_evaluador  | INT                        | 999999      | NOT NULL         | ----   | ----        | Identificador del equipo evaluador               | Relaciona el proceso con el equipo encargado de la evaluación |
| descripcion_proceso     | CHAR                       | X (255)     | NOT NULL         | ----   | ----        | Descripción del proceso                          | Descripción detallada del proceso evaluado en el IPERC     |

 ---

## Actividades
**Semántica**: Las acciones dentro de un proceso que contribuyen a la operación o evaluación del IPERC.

| Atributo        | Naturaleza (tipo de valor) | Formato     | Valores válidos  | Unidad | Derivada de | Semántica (descripción)                           | Ontología (rol en el negocio)                              |
|-----------------|----------------------------|-------------|------------------|--------|-------------|--------------------------------------------------|------------------------------------------------------------|
| id_actividad    | INT                        | 999999      | NOT NULL         | ----   | ----        | Identificador único de la actividad              | Control de las actividades que se realizan en un proceso   |
| descripcion_actividad   | CHAR                       | X (255)     | NOT NULL         | ----   | ----        | Descripción detallada de la actividad            | Descripción detallada de las actividades en el proceso     |
| id_proceso      | INT                        | 999999      | NOT NULL         | ----   | ----        | Identificador del proceso asociado               | Relación directa con el proceso evaluado en el IPERC       |

---

## Tareas
**Semántica**: Las tareas específicas dentro de una actividad que deben ser realizadas en el proceso de evaluación del IPERC.

| Atributo        | Naturaleza (tipo de valor) | Formato     | Valores válidos  | Unidad | Derivada de | Semántica (descripción)                           | Ontología (rol en el negocio)                              |
|-----------------|----------------------------|-------------|------------------|--------|-------------|--------------------------------------------------|------------------------------------------------------------|
| id_tarea        | INT                        | 999999      | 6 digitos        | ----   | ----        | Identificador único de la tarea                  | Identificación y control de las tareas                     |
| descripcion_tarea       | CHAR                       | X (255)     | NOT NULL         | ----   | ----        | Descripción detallada de la tarea                | Descripción específica de la tarea a realizar              |
| puesto_trabajo  | CHAR                       | X (255)     | NOT NULL         | ----   | ----        | Puesto de trabajo que ejecuta la tarea           | Define la relación con el equipo humano                    |
| cond_operacional| CHAR                       | X (255)     | NOT NULL         | ----   | ----        | Condiciones operacionales de la tarea            | Detalle de las condiciones necesarias para realizar la tarea|
| id_actividad    | INT                        | 999999      | NOT NULL         | ----   | ----        | Identificador de la actividad                    | Relación directa con la actividad a la que pertenece la tarea|


## Identificación del Riesgo
**Semántica**: Proceso de identificación de riesgos asociados a una tarea o actividad, incluyendo la descripción del peligro y el evento no deseado.

| Atributo             | Naturaleza (tipo de valor) | Formato     | Valores válidos  | Unidad | Derivada de | Semántica (descripción)                           | Ontología (rol en el negocio)                              |
|---------------------|----------------------------|-------------|------------------|--------|-------------|--------------------------------------------------|------------------------------------------------------------|
| id_riesgo           | INT                        | 999999      | 6 digitos        | ----   | ----        | Identificador único del riesgo                   | Control de los riesgos identificados                       |
| descripción_peligro | CHAR                       | X (255)     | NOT NULL         | ----   | ----        | Descripción del peligro asociado                 | Detalle del peligro asociado a la tarea                    |
| evento_no_deseado   | CHAR                       | X (255)     | NOT NULL         | ----   | ----        | Evento no deseado                                | Evento que puede producirse como consecuencia del riesgo   |

---

## Análisis del Riesgo
**Semántica**: Proceso de análisis de las consecuencias, tipo de contacto y afectados por los riesgos identificados en una tarea.

| Atributo        | Naturaleza (tipo de valor) | Formato     | Valores válidos  | Unidad | Derivada de | Semántica (descripción)                           | Ontología (rol en el negocio)                              |
|-----------------|----------------------------|-------------|------------------|--------|-------------|--------------------------------------------------|------------------------------------------------------------|
| id_analisis       | INT                        | 999999      | NOT NULL         | ----   | ----        | Identificador único del análisis de riesgo           | Referencia única para cada análisis de riesgo                   |
| id_riesgo       | INT                        | 999999      | NOT NULL         | ----   | ----        | Identificador único del riesgo analizado         | Referencia a los riesgos identificados                     |
| afectado        | CHAR                       | X (255)     | NOT NULL         | ----   | ----        | Descripción del afectado                         | Descripción de las personas o áreas afectadas              |
| id_tipo_contacto   | CHAR                       | XXXX     | 4 digitos         | TAB   | ----        | Tipo de contacto que podría provocar el riesgo   | Clasificación del contacto con el peligro                  |
| id_tipo_peligro | CHAR                        | XXXXXX      | 6 digitos         | TAB   | ----        | Identificador del tipo de peligro                 | Clasificación del tipo de peligro que puede generar el riesgo |
| consecuencia    | CHAR                       | X (255)     | NOT NULL         | ----   | ----        | Consecuencia del riesgo                          | Da información sobre las posibles consecuencias            |

---

## TAB: Tipos de contacto

| Código          | Descripción                 |
|-----------------|-----------------------------|
| TC01 | TC 01 GOLPEAR CONTRA (corriendo hacia o tropezando con) |
| TC02 | TC 02 GOLPEADO POR (objeto en movimiento) |
| TC03 | TC 03 CAÍDA AL MISMO NIVEL (resbalar, tropezar, volcarse) |
| TC04 | TC 04 CAÍDA A DISTINTO NIVEL (el cuerpo cae) |
| TC05 | TC 05 ATRAPADO EN (enganchado, agarrado) |
| TC06 | TC 06 CON OBJETOS PUNZANTES O CORTANTES |
| TC07 | TC 07 APLASTADO/CHANCADO ENTRE O DEBAJO DE OBJETOS  |
| TC08 | TC 08 ENERGÍA (neumática, radiación, etc.) |
| TC09 | TC 09 MATERIALES QUÍMICOS |
| TC10 | TC 10 MATERIALES BIOLÓGICOS |
| TC11 | TC 11 ERGONÓMICOS |
| TC12 | TC 12 PSICOSOCIALES |

---

## TAB: Tipos de peligro

| Código          | Descripción                 |
|-----------------|-----------------------------|
| TC01.01               | Materiales       |
| TC01.02               | Pisos, hastiales  y carga          |
| TC02.01                 | TC 02.01 Operación de vehículos y equipos móviles    |
| TC02.02               | TC 02.02 Estabilidad de presas y depósitos |
| TC02.03               | TC 02.03 Estabilidad de macizo rocoso |
| TC02.04               | Carro minero |
| TC02.05               | Tubería, manguera de aire comprimido o accesorios |
| TC02.06               | Herramientas |
| TC02.07               | Materiales (que caen) |
| TC02.08               | Proyección de partículas |
| TC02.09               | Proyección de balas |
| TC02.10               | Equipo de izaje, grúas o carga |
| TC03.01               | Pisos resbaladizos |
| TC03.02               | Piso Desnivelado |
| TC04.01               | TC 04.01 Izaje en piques |
| TC04.02               | Subir / Bajar Escaleras |
| TC04.03               | Espacios abiertos |
| TC04.04               | Andamios y plataformas elevadas |
| TC04.05               | Tolvas / Echaderos |
| TC05.01               | TC 05.01 Fajas transportadoras |
| TC05.02               | Partes móviles o giratorias |
| TC06.01               | Herramientas punzo cortantes |
| TC06.02               | Mallas electrosoldadas |
| TC07.01               | Carga suspendida |
| TC07.02               | Succión (tolvas, echaderos, labores antiguas, subsidencias) |
| TC02.03               | Material de excavaciones y zanjas |
| TC07.04               | Materiales apilados |
| TC08.01               | TC 08.01 Energía eléctrica |
| TC08.02               | TC 08.02 Transporte de personal |
| TC08.03               | Tormenta eléctrica |
| TC08.04               | Equipos / Instalaciones neumáticos o hidráulicos (gases comprimidos, calderos, otros) |
| TC08.05               | Temperaturas extremas  (calor, frío) |
| TC08.06               | Radiación (solar, radioactiva, soldadura, otros) |
| TC08.07               | Ruido (que sobrepase el LMP) |
| TC09.01               | TC 09.01 Gases interior mina (Ventilación) |
| TC09.02               | TC 09.02 Explosivos |
| TC09.03               | TC 09.03 Materiales químicos peligrosos |
| TC09.04               | Otros gases |
| TC09.05               | Otros químicos |
| TC09.06               | Humo (combustión, soldadura, otros) |
| TC09.07               | Hidrocarburos |
| TC09.08               | Material inflamable / Combustible |
| TC09.09               | Polvo |
| TC10.01               | Fluidos Corporales |
| TC10.02               | Animales |
| TC10.03               | Vectores (roedores, insectos, otros) |
| TC10.04              | Microorganismos |
| TC10.05               | COVID-19 |
| TC11.01               | Iluminación (excesiva/deficiente) |
| TC11.02               | Vibraciones |
| TC11.03               | Movimientos repetitivos |
| TC11.04               | Manipulación manual de cargas |
| TC11.05               | Posturas |
| TC12.01               | Agresiones físicas y verbales |
| TC12.02               | Delincuencia común |
| TC12.03               | Acoso laboral (hostilización) |
| TC12.04               | Carga de trabajo (horarios, sobretiempo, descanso, otros) |
| TC12.05               | Nivel de Cultura de Seguridad (Liderazgo) |
| TC12.06               | Hostigamiento sexual |

---

## Valoración del Riesgo Inicial
**Semántica**: Valoración del riesgo antes de implementar controles, basada en su probabilidad y severidad.

| Atributo            | Naturaleza (tipo de valor) | Formato     | Valores válidos  | Unidad | Derivada de | Semántica (descripción)                           | Ontología (rol en el negocio)                              |
|---------------------|----------------------------|-------------|------------------|--------|-------------|--------------------------------------------------|------------------------------------------------------------|
| id_valoracion_inicial| INT                        | 999999      | NOT NULL         | ----   | ----        | Identificador único de la valoración inicial      | Referencia a la valoración del riesgo antes de aplicar controles |
| id_tipo_severidad   | CHAR                        | XX      | 2 digitos        | TAB   | ----        | Severidad del riesgo                             | Clasificación del riesgo según su impacto                 |
| id_tipo_probabilidad| CHAR                        | XXXXX      | 5 digitos        | TAB   | ----        | Probabilidad de que ocurra el riesgo             | Estimación de la probabilidad de ocurrencia               |
| id_tipo_riesgo      | CHAR                        | XX      | 2 digitos        | TAB   | ----        | Clasificación del tipo de riesgo                 | Categorización del riesgo para su evaluación y control    |

---

## TAB: Tipos de severidad
| Código | Descripción  |
|--------|--------------|
| CA      | Catastrófico  |
| MO     | Mortalidad   |
| PE      | Permanente   |
| TE      | Temporal   |
| ME      | Menor   |

---

## TAB: Tipos de probabilidad
| Código | Descripción  |
|--------|--------------|
| P-ALT     | Común  |
| P-MED     | Ha sucedido   |
| P-BAJ     | Podría suceder   |
| P-RAR     | Raro que suceda   |
| P-IMP     | Prácticamente imposible  que suceda   |

**La tabla aparece conjunta con las tablas de la siguiente entidad**

---

## Valoración del Riesgo Residual
**Semántica**: Valoración del riesgo después de aplicar los controles establecidos, considerando los tipos y cantidad de controles, así como el tipo de riesgo resultante.

| Atributo               | Naturaleza (tipo de valor) | Formato     | Valores válidos  | Unidad | Derivada de | Semántica (descripción)                              | Ontología (rol en el negocio)                              |
|------------------------|----------------------------|-------------|------------------|--------|-------------|-----------------------------------------------------|------------------------------------------------------------|
| id_valoracion_residual  | INT                        | 999999      | NOT NULL         | ----   | ----        | Identificador único de la valoración residual        | Identificación única de la valoración posterior a los controles|
| id_valoracion_inicial   | INT                        | 999999      | NOT NULL         | ----   | ----        | Referencia a la valoración inicial                  | Relaciona con la valoración inicial del riesgo antes de controles|
| id_control              | INT                        | 999999      | NOT NULL         | ----   | ----        | Identificador del control aplicado                  | Relaciona los controles aplicados al riesgo residual        |
| cantidad_controles      | INT                        | 9999        | NOT NULL         | ----   | ----        | Número de controles aplicados                       | Número total de controles aplicados al riesgo               |
| id_tipo_riesgo          | CHAR                        | XX      | 2 digitos         | TAB    | ----        | Clasificación del tipo de riesgo post-control        | Tipo de riesgo residual clasificado después de los controles aplicados|

---

## TAB: Tipos de riesgo
| Código | Descripción  |
|--------|--------------|
| BA      | BAJO  |
| ME     | MEDIO   |
| AL      | ALTO   |

---

## Control
**Semántica**: Detalles de los controles aplicados para reducir o mitigar el riesgo, incluyendo los tipos de control y estrategias aplicadas.

| Atributo            | Naturaleza (tipo de valor) | Formato     | Valores válidos  | Unidad | Derivada de | Semántica (descripción)                           | Ontología (rol en el negocio)                              |
|---------------------|----------------------------|-------------|------------------|--------|-------------|--------------------------------------------------|------------------------------------------------------------|
| id_control          | INT                        | 999999      | 6 digitos        | ----   | ----        | Identificador único del control aplicado          | Control y trazabilidad de los controles aplicados          |
| id_tipo_Qcontrol        | CHAR                       | X           | TAB              | ----   | ----        | Identificador del tipo de calidad del control aplicado | Clasificación cualitativa de la calidad del control aplicada |
| descripcion_control | CHAR                       | X (255)     | NOT NULL         | ----   | ----        | Descripción del control aplicado                  | Detalle del control aplicado en el riesgo                  |
| id_tipo_med_control | CHAR                        | XXX      | TAB        | ----   | ----        | Tipo de medida de control aplicada                | Clasificación del tipo de medida aplicada                  |
| id_tipo_estgia_control| CHAR                      | X      | TAB        | ----   | ----        | Estrategia de control aplicada                    | Definición de la estrategia empleada para el control del riesgo|

---

## TAB: Tipos de calidad del control 
| Código          | Porcentaje (%) | Descripción                                                                            |
|-----------------|----------------|----------------------------------------------------------------------------------------|
| A               | 100%            | **TOTAL**: Los controles eliminan prácticamente la probabilidad o impacto del riesgo    |
| B               | 90%             | **ALTA**: Los controles limitan significativamente la probabilidad o impacto del riesgo |
| C               | 80%-60%         | **MEDIA**: Los controles limitan la probabilidad o impacto, pero no drásticamente       |
| D               | 50%-30%         | **BAJA**: Los controles muestran debilidades significativas                            |
| E               | 20%-10%         | **MUY BAJA**: Controles inexistentes o poco efectivos                                  |


---
## TAB: Tipos de medida de control

| Código | Descripción  |
|--------|--------------|
| ELI      | Eliminacion  |
| SUS     | Sustitucion   |
| INH      | Ingenieria   |
| ADM      | Administrativo   |
| EPP      | EPP   |

---

## TAB: Tipos de estrategia de control

| Código | Descripción  |
|--------|--------------|
| P      | Preventivo  |
| M     | Mitigacion   |

---

## Plan de Acción de Mejora
**Semántica**: Conjunto de acciones que se implementan para reducir los riesgos residuales identificados en el análisis de riesgos.

| Atributo             | Naturaleza (tipo de valor) | Formato     | Valores válidos  | Unidad | Derivada de | Semántica (descripción)                                 | Ontología (rol en el negocio)                              |
|----------------------|----------------------------|-------------|------------------|--------|-------------|--------------------------------------------------------|------------------------------------------------------------|
| id_plan_mejora        | INT                        | 999999      | NOT NULL         | ----   | ----        | Identificador único del plan de mejora                  | Controla los planes de acción diseñados para mitigar riesgos|
| id_valoracion_residual | INT                        | 999999      | NOT NULL         | ----   | ----        | Identificador de la valoración del riesgo residual      | Referencia a la valoración residual para aplicar el plan    |
| accion_que            | CHAR                       | X (255)     | NOT NULL         | ----   | ----        | Descripción de la acción a tomar                        | Describe las acciones específicas para reducir los riesgos  |
| cantidad_empleados    | INT                        | 2 digitos   | NOT NULL         | ----   | ----        | Número de empleados involucrados en la acción           | Indica cuántos empleados son necesarios para implementar el plan|
| fecha_cuando          | DATE                       | DD/MM/YYYY  | Fecha válida     | ----   | ----        | Fecha en la que se debe implementar la acción           | Control de tiempos para la implementación de las mejoras    |

---
## TareasXIdentRiesgo
**Semántica**: Relación que conecta las tareas con los riesgos identificados en las actividades del IPERC.

| Atributo     | Naturaleza (tipo de valor) | Formato     | Valores válidos  | Unidad | Derivada de | Semántica (descripción)                               | Ontología (rol en el negocio)                            |
|--------------|----------------------------|-------------|------------------|--------|-------------|------------------------------------------------------|----------------------------------------------------------|
| id_tarea     | INT                        | 999999      | NOT NULL         | ----   | ----        | Identificador único de la tarea                       | Conecta una tarea específica con los riesgos identificados |
| id_riesgo    | INT                        | 999999      | NOT NULL         | ----   | ----        | Identificador único del riesgo identificado           | Relaciona la tarea con el riesgo que implica              |

---

## PlanaccionxEmpleado
**Semántica**: Relación que conecta los planes de acción de mejora con los empleados responsables de implementarlos.

| Atributo        | Naturaleza (tipo de valor) | Formato     | Valores válidos  | Unidad | Derivada de | Semántica (descripción)                               | Ontología (rol en el negocio)                            |
|-----------------|----------------------------|-------------|------------------|--------|-------------|------------------------------------------------------|----------------------------------------------------------|
| id_plan_mejora  | INT                        | 999999      | NOT NULL         | ----   | ----        | Identificador único del plan de acción de mejora      | Relaciona un plan de acción con los empleados encargados  |
| codigo_empleado | INT                        | 999999      | NOT NULL         | ----   | ----        | Identificador único del empleado                      | Relaciona a un empleado con el plan de mejora que implementará |

---
