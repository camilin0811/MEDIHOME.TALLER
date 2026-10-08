# MediHome

Modelo de un sistema de atención médica domiciliaria: permite registrar pacientes
y profesionales de la salud, programar servicios a domicilio, dejar constancia de
la atención prestada y tomar mediciones de signos vitales.

## Integrantes

- Andres Camilo Muñoz Bolaños
- Walter Rene Jojoa

## Contenido del repositorio

| Ruta | Descripción |
| --- | --- |
| `src/` | Código fuente en Java de las clases del modelo |
| `MediHome.vpp.bak_000f` | Proyecto de Visual Paradigm con el diagrama de clases UML |

## Clases del modelo

| Clase | Rol |
| --- | --- |
| `Usuario` | Clase base con los datos comunes de identificación, nombre y correo |
| `ProfesionalSalud` | Usuario con registro profesional y especialidad |
| `Paciente` | Usuario con teléfono y dirección |
| `Notificable` | Interfaz que define la operación `notificar` |
| `EquipoAtencion` | Agrupa profesionales por zona de cobertura |
| `ServicioDomiciliario` | Servicio programado en la dirección del paciente |
| `AtencionMedica` | Registro de la atención con observaciones y recomendaciones |
| `MedicionSignosVitales` | Temperatura, frecuencia cardiaca, presión y saturación |

`ProfesionalSalud` y `Paciente` heredan de `Usuario` e implementan `Notificable`.
Un `ServicioDomiciliario` genera una `AtencionMedica`, que a su vez contiene las
mediciones de signos vitales tomadas durante la visita.
