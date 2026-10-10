# Ejercicio 3 - Modelo Entidad-Relación de un Sistema de Gestión Médica

## Descripción

Este ejercicio consiste en diseñar un modelo Entidad-Relación (DER) para un sistema de gestión médica. El modelo permite administrar pacientes, turnos médicos, médicos, especialidades, medicamentos y recetas, representando las relaciones entre estos elementos.

## Entidades y atributos

### 1. Paciente

Representa a las personas que reciben atención médica.

* `id_paciente`: identificador del paciente.
* `nombre`: nombre del paciente.
* `apellido`: apellido del paciente.
* `dni`: documento de identidad.
* `domicilio`: dirección del paciente.
* `obra_social`: cobertura médica.
* `historia_clinica`: información clínica del paciente.

### 2. Turno

Representa los turnos solicitados por los pacientes para recibir atención médica.

* `id_turno`: identificador del turno.
* `fecha`: fecha del turno.
* `hora`: horario de atención.
* `estado`: estado del turno.
* `diagnostico`: diagnóstico médico.
* `historia_clinica`: información clínica relacionada.

### 3. Medico

Representa a los profesionales que brindan atención médica.

* `id_medico`: identificador del médico.
* `nombre`: nombre del médico.
* `apellido`: apellido del médico.
* `telefono`: número de contacto.

### 4. Especialidad

Representa las especialidades médicas disponibles.

* `id_especialidad`: identificador de la especialidad.
* `nombre`: nombre de la especialidad.

### 5. Medico_especialidad

Relaciona a los médicos con las especialidades que poseen.

* `id_especialidad`: identificador de la especialidad.
* `id_medico`: identificador del médico.

### 6. Medicamento

Representa los medicamentos que pueden ser recetados.

* `id_medicamento`: identificador del medicamento.
* `nombre_comercial`: nombre comercial.
* `monodroga`: principio activo.
* `laboratorio`: laboratorio fabricante.

### 7. Receta

Representa las recetas médicas asociadas a los turnos de atención.

* `id_turno`: identificador del turno.
* `id_medicamento`: identificador del medicamento.

## Relaciones y cardinalidades

* **Paciente – Turno (Solicita):** un paciente puede solicitar varios turnos, mientras que cada turno corresponde a un paciente.
* **Turno – Médico (Atiende):** un médico puede atender varios turnos, mientras que cada turno es atendido por un médico.
* **Turno – Receta (Genera):** un turno puede generar recetas médicas.
* **Receta – Medicamento (Recetado):** permite relacionar las recetas con los medicamentos indicados.
* **Médico – Especialidad (Posee):** permite asociar médicos con sus especialidades.
* **Médico_especialidad – Especialidad (Ejerce):** representa las especialidades ejercidas por los médicos.

## Objetivo

Diseñar una base de datos que permita organizar la información de un centro médico, gestionar turnos, registrar pacientes, identificar profesionales y sus especialidades, y administrar las recetas y los medicamentos indicados.
