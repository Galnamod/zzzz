<table border="1">
	<tbody>
		<tr>
			<td>Nombre</td>
			<td colspan="2">Elaboración y revisión del IPERC</td>
		</tr>
		<tr>
			<td>Tarea realizada por el usuario</td>
			<td colspan="2">PRecolectar información de los peligros y clasificar el nivel de riesgo que representa y acciones y medidas a tomar.</td>
		</tr>
		<tr>
			<td>Actor inicializador</td>
			<td colspan="2">Jefe de Área</td>
		</tr>
		<tr>
			<td>Actores participantes</td>
			<td colspan="2">
    <ol>
      <li>Superintendente / Jefe de Área</li>
      <li>Jefe de Sección / Ingeniero supervisor</li>
      <li>Un trabajador expuesto</li>
      <li>Director / Jefe de Sección / Ingeniero de seguridad</li>
    </ol>
    </td>
    </tr>
		<tr>
            <th>Flow of Events</th>
            <td>
            <ol>
                <li>El jefe de mantenimiento ingresa al sistema digital.</li>
                <li>Selecciona el equipo a ser mantenido.</li>
                <li>Configura las tareas de mantenimiento preventivo.</li>
                <li>Asigna personal y recursos (herramientas, tiempo).</li>
                <li>Confirma el plan de mantenimiento.</li>
                <li>El sistema genera las órdenes de trabajo digitalmente.</li>
            </ol>
            </td>
        </tr>
        <tr>
			<th>Excepciones</th>
			<td>
            <ol>
                <li>El equipo no está disponible para mantenimiento.</li>
                <li>Recursos (técnicos, herramientas) no disponibles.</li>
            </ol>
            </td>
		</tr>
		<tr>
			<td>Precondición</td>
			<td colspan="2">El equipo y su historial de mantenimiento deben estar registrados en el sistema</td>
		</tr>
		<tr>
			<td>Postcondición</td>
			<td colspan="2">El plan de mantenimiento queda almacenado y las órdenes de trabajo son asignadas digitalmente</td>
		</tr>
		<tr>
			<td>Casos de uso incluidos</td>
			<td colspan="2">-</td>
		</tr>
		<tr>
			<td>Servicios utilizados</td>
			<td colspan="2">Gestión de equipos, Gestión de órdenes de trabajo, Notificaciones</td>
		</tr>
		<tr>
			<th>Requisitos no funcionales</th>
			<td>
            <ol>
                <li>Interfaz intuitiva y accesible desde dispositivos móviles</li>
                <li>Seguridad en el acceso a los datos</li>
            </ol>
            </td>
		</tr>
	</tbody>
</table>
<br>

## Módulo 4: Gestion del IPERC

![Proceso de Planificacion](../Diagramas/Gestion-IPERC_TO-BE.png)

<table>
  <thead>
    <tr>
      <th>Secuencia</th>
      <th>Actividad</th>
      <th>Descripción</th>
      <th>Responsable</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>Se definen los objetivos y metodologia</td>
      <td>Se determina la profundidad, alcance y limites del trabajo.</td>
      <td>Jefe de seguridad y Jefe de seccion</td>
    </tr>
    <tr>
      <td>2</td>
      <td>Se recopila información de planta y de trabajadores</td>
      <td>Se hacen auditorias en planta y reuniones con trabajadores</td>
      <td>Ingeniero supervisor</td>
    </tr>
    <tr>
      <td>3</td>
      <td>Se determina el proceso para el IPERC</td>
      <td>Se escoge el conjunto de actividades que se buscan analizar.</td>
      <td>Ingeniero de seguridad</td>
    </tr>
    <tr>
      <td>4</td>
      <td>Digitacion semiautomatica de actividades.</td>
      <td>La empresa tiene la mayoria de actividades definidas y el ingeniero digitaliza con la ayuda de los datos de los informes anteriores .</td>
      <td>Ingeniero de seguridad</td>
    </tr>
    <tr>
      <td>5</td>
      <td>Digitacion de la identifiacion del riesgo.</td>
      <td>Se ditaliza en el sistema el peligro y el evento no deseado generado por el riesgo.</td>
      <td>Ingeniero de seguridad</td>
    </tr>
    <tr>
      <td>6</td>
      <td>Digitacion semiautomatica del analisis de riesgo.</td>
      <td>Se digitaliza el afetado, el tipo de daño o contacto causado y la consecuencia. Datos como tipo de daño y afectado corresponden a tablas anexadas.</td>
      <td>Ingeniero de seguridad</td>
    </tr>
    <tr>
      <td>7</td>
      <td>Automatizacion del calculo del valor del riesgo inicial.</td>
      <td>El valor de riesgo inicial se basa en una matriz para calcularla, los datos de probabilidad y severidad corresponden a tablas anexadas.</td>
      <td>Sistema</td>
    </tr>
    <tr>
      <td>8</td>
      <td>Semiautomatizacion del calculo del valor del riesgo residual</td>
      <td>Aun es necesario digitar las medidas de control pero el valor del riesgo residual es automatizable.</td>
      <td>Ingeniero de seguridad</td>
    </tr>
    <tr>
      <td>9</td>
      <td>¿Cual es el nivel de riesgo resultante?</td>
      <td>Cada nivel de riesgo residual, tiene diferentes acciones a tomar.</td>
      <td>Ingeniero de seguridad</td>
    </tr>
    <tr>
      <td>9a</td>
      <td>Analizar costo-beneficio con los controles actuales.</td>
      <td>Si el nivel de riesgo residual es ALARP, se busca hacer una evaluacion cualitativa.</td>
      <td>Ingeniero de seguridad</td>
    </tr>
    <tr>
      <td>9b</td>
      <td>Se gestiona el riesgo con los controles actuales.</td>
      <td>Si el nivel de riesgo residual es bajo o medio, se gestionara el riesgo con los controles actuales.</td>
      <td>Ingeniero supervisor</td>
    </tr>
    <tr>
      <td>9c</td>
      <td>Se realiza una REEVALUACIÓN del riesgo considerando nuevas medidas</td>
      <td>Si el nivel de riesgo residual es alto, se realiara una revaaluacion del riesgo considerando nuevas jerarquias de control.</td>
      <td>Ingeniero de seguridad</td>
    </tr>
    <tr>
      <td>10</td>
      <td>Digitacion de los planes de mejora.</td>
      <td>Se digita los planes de mejora a realizar con un quien, que y cuando.</td>
      <td>Jefe de seccion</td>
    </tr>
    <tr>
      <td>11</td>
      <td>Ordenamiento por prioridad del riesgo residual automatizado</td>
      <td>EL sistema ordena de mayor a menor valor de riesgo residual.</td>
      <td>Sistema</td>
    </tr>
    <tr>
      <td>11</td>
      <td>Almacenamiento automatico y generacion de informes</td>
      <td>EL sistema almacena y genera informes en pdf y demas.</td>
      <td>Sistema</td>
    </tr>
    <tr>
      <td>12</td>
      <td>Aprobar IPERC.</td>
      <td>Aprobacion de los informes y del IPERC generado.</td>
      <td>Superintendiente o Jefe de Seccion</td>
    </tr>
  </tbody>
</table>

---
