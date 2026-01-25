# Estandarización y curación de datos DwC

**Estandarización de registros de biodiversidad a Darwin Core (DwC)**

Sistema de información conformado por una red de socios y colaboradores con intereses compartidos en la gestión, estandarización y publicación de información sobre biodiversidad.

## Objetivos

- Consolidar una base de datos centralizada con información sobre diversidad, distribución y abundancia de organismos.
- Estandarizar y formatear conjuntos de datos bajo la estructura básica y las normas del estándar Darwin Core (DwC).
- Facilitar la interoperabilidad, reutilización y publicación de datos de biodiversidad.

## Público objetivo

- Investigadores y profesionales  
- Estudiantes  
- Gestores de datos de biodiversidad  
- Ciudadanos interesados en ciencia participativa  

## Uso del estándar Darwin Core

Este repositorio utiliza el estándar **Darwin Core (DwC)** para la estructuración y publicación de datos de biodiversidad.  
Darwin Core está diseñado principalmente para documentar **ocurrencias biológicas**, los eventos asociados a su registro y su localización espacial y temporal.

Por esta razón, algunos tipos de datos pueden representarse de manera directa dentro de DwC, mientras que otros se documentan únicamente como **metadatos** o mediante **extensiones**.

La siguiente tabla resume qué tipos de datos pueden representarse en formato DwC y sus principales consideraciones.

## Compatibilidad de tipos de datos con Darwin Core

| Tipo de dato | Compatibilidad con DwC | Descripción / Consideraciones |
|--------------|------------------------|-------------------------------|
| Ocurrencias y distribución | ✅ Alta | Constituyen el núcleo del estándar DwC mediante términos como `occurrenceID`, `scientificName`, `eventDate` y `locality`. |
| Presencia / ausencia | ⚠️ Media | Se documenta con `occurrenceStatus`; las ausencias verdaderas requieren un diseño de muestreo claramente definido. |
| Abundancia y conteos individuales | ✅ Alta | Puede representarse usando `individualCount`, `organismQuantity` y `organismQuantityType`. |
| Biomasa, tamaños y estados de vida | ⚠️ Media | Estados de vida (`lifeStage`) y biomasa pueden incluirse; los datos morfométricos detallados presentan limitaciones. |
| Medidas abióticas | ⚠️ Media | Se incorporan mediante la extensión `MeasurementOrFact`; DwC no es un estándar ambiental específico. |
| Medidas bióticas | ⚠️ Media | Pueden documentarse con `MeasurementOrFact` o campos descriptivos, con capacidad limitada para interacciones complejas. |
| Métodos de muestreo y áreas de estudio | ✅ Alta (metadatos) | Se documentan mediante `samplingProtocol`, `eventRemarks`, `locationID` y metadatos del conjunto de datos. |
| Protocolos de procesamiento de muestras | ❌ Baja | No forman parte del objetivo principal de DwC; se recomienda documentarlos en metadatos (EML) o documentación externa. |

## Consideraciones finales

- Darwin Core **no es un estándar ecológico completo**, sino un esquema orientado a la interoperabilidad de datos de biodiversidad.
- Variables ambientales, métodos detallados y protocolos de laboratorio deben documentarse preferentemente como **metadatos**.
- En proyectos con un fuerte componente ambiental, puede ser recomendable complementar DwC con otros estándares como **EML**, **OBIS-ENV** u otros esquemas especializados.

## Servicios de curación y estandarización

Este repositorio ejemplifica los alcances de la curación y estandarización de datos de biodiversidad bajo el estándar Darwin Core, incluyendo:

- Curación de datos de ocurrencia con o sin información espacial (coordenadas geográficas).
- Estandarización y validación de nombres científicos, incluyendo corrección de errores tipográficos y normalización taxonómica.
- Conversión de fechas a formato ISO 8601, incluyendo registros con formatos heterogéneos o múltiples fechas.
- Normalización de campos clave como localidad, identificadores, número de individuos y responsables de identificación.
- Documentación explícita de decisiones de curación para mantener la trazabilidad de la información original.
- Preparación de conjuntos de datos compatibles con su publicación en infraestructuras como GBIF u OBIS.
