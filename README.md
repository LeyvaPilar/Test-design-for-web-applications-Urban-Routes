# Test-design-for-web-applications-Urban-Routes
Proyecto 3

## Descripción General del Proyecto

Urban Routes es una aplicación de servicios de transporte que permite a los usuarios reservar diferentes tipos de vehículos según sus necesidades. Durante el tercer sprint, se realizó una evaluación exhaustiva de las funcionalidades principales y secundarias de la aplicación, enfocándose en cuatro áreas críticas:

<a href="https://docs.google.com/spreadsheets/d/1HuMgI36dIGE-J_tjDB96rwcFP2mZ2W60/edit?usp=sharing&ouid=103258639782325772763&rtpof=true&sd=true" target="_blank">
 📊​ Archivo original 
</a>

### Alcance del Análisis

1. **Diseño e Interfaz de Usuario**
   - Validación de 75 elementos de interfaz
   - Pruebas de compatibilidad en Chrome y Firefox
   - Evaluación de elementos visuales y experiencia de usuario
   - Verificación de responsividad y elementos interactivos

2. **Sistema de Método de Pago**
   - Validación de campos de tarjeta de crédito
   - Pruebas de seguridad en transacciones
   - Verificación de formatos y validaciones
   - Evaluación de mensajes de error y confirmación

3. **Lógica del Botón de Reserva**
   - Pruebas de flujo de reservación
   - Validación de estados y transiciones
   - Verificación de condiciones previas
   - Evaluación de casos de error y excepciones

4. **Funcionalidad de Alquiler**
   - Pruebas de proceso completo de alquiler
   - Validación de temporizadores y costos
   - Verificación de cancelaciones y modificaciones
   - Evaluación de estados del vehículo

### Metodología Implementada

- **Enfoque de Pruebas**:
  - Pruebas de regresión
  - Pruebas funcionales
  - Pruebas de interfaz
  - Validación de campos
  - Pruebas de integración

- **Herramientas Utilizadas**:
  - Navegadores: Chrome y Firefox
  - Resoluciones: 1920x1080 y 800x600
  - Sistema de seguimiento: Jira (PLM1G3S)
  - Documentación: Excel para registro y seguimiento

### Métricas Generales

- Total de casos de prueba: 149
- Casos aprobados: 88 (59.06%)
- Casos no aprobados: 37 (24.83%)
- Casos omitidos: 24 (16.11%)
- Bugs identificados: 37
- Severidades críticas: 15
- Severidades medias: 12
- Severidades bajas: 10

### Hallazgos Significativos

1. **Problemas Críticos**:
   - Validaciones inconsistentes en pagos
   - Fallos en el flujo de reserva
   - Problemas de visualización en mapas
   - Errores en temporizadores
   - Inconsistencias en cancelaciones

2. **Áreas de Mejora**:
   - Sistema de validación de tarjetas
   - Flujo de reserva y cancelación
   - Visualización de vehículos en mapa
   - Gestión de estados de reserva
   - Manejo de temporizadores

3. **Impacto en Usuario Final**:
   - Experiencia de usuario afectada en pagos
   - Confusión en proceso de reserva
   - Problemas de visibilidad de vehículos
   - Inconsistencias en cancelaciones
   - Dificultades en validación de documentos

Este análisis proporciona una base sólida para la identificación y priorización de correcciones necesarias antes del lanzamiento de la siguiente versión de Urban Routes.

Análisis detallado de cada pestaña:

# Tab 1: Lista de Comprobación del Diseño

## Resumen de Resultados
| Estado | Chrome | Firefox |
|--------|---------|----------|
| Aprobado | 57 | 57 |
| No Aprobado | 11 | 11 |
| Omitido | 7 | 7 |
| Total de Casos | 75 | 75 |

## Principales Hallazgos

| Categoría | Descripción | Estado | Bug ID |
|-----------|-------------|---------|---------|
| Navegación | La pantalla permite eliminar direcciones | No Aprobado | PLM1G3S-1 |
| Interacción | Usuario no puede elegir automóvil en mapa | No Aprobado | PLM1G3S-2 |
| Visualización | Problemas con coches disponibles en mapa | No Aprobado | PLM1G3S-3 |
| Funcionalidad Premium | Opciones de divertirse con fruta | No Aprobado | PLM1G3S-4 |
| UI/UX | Problemas con copas frías | No Aprobado | PLM1G3S-5 |
| Branding | Marca de agua "PLATAFORMA" | No Aprobado | PLM1G3S-6 |

# Tab 2: Lista de Comprobación de Método de Pago

## Resumen de Validaciones
| Categoría | Total | Aprobados | No Aprobados |
|-----------|--------|------------|--------------|
| Campos de Tarjeta | 28 | 13 | 15 |
| Funcionalidad | 15 | 15 | 0 |
| Validaciones | 6 | 3 | 3 |

## Principales Issues

| ID | Descripción | Severidad |
|----|-------------|-----------|
| PLM1G3S-15 | Validación incorrecta de 11 caracteres | Alta |
| PLM1G3S-16 | Validación incorrecta de 13 caracteres | Alta |
| PLM1G3S-17 | Espacios no se añaden automáticamente | Media |
| PLM1G3S-18 | Botón activo con datos incompletos | Alta |
| PLM1G3S-19 | Acepta letras en número de tarjeta | Alta |

# Tab 3: Casos de Prueba para el Botón de Reserva

## Resultados de Pruebas
| ID | Escenario | Estado | Observaciones |
|----|-----------|--------|---------------|
| p-1 | Campos completos | Aprobado | Funcionamiento correcto |
| p-2 | Sin licencia | No Aprobado | PLM1G3S-31 |
| p-3 | Sin método de pago | No Aprobado | PLM1G3S-32 |
| p-4 | Borrado de direcciones | Omitido | PLM1G3S-33 |
| p-5 | Campos incompletos | Omitido | PLM1G3S-34 |

# Tab 4: Casos de Prueba para el Alquiler

## Casos de Prueba
| ID | Escenario | Estado | Bug ID |
|----|-----------|--------|---------|
| p-1 | Reserva completa | Aprobado | - |
| p-2 | Campos vacíos | No Aprobado | PLM1G3S-35 |
| p-3 | Temporizador | Aprobado | - |
| p-4 | Cancelación | Omitido | PLM1G3S-36 |
| p-5 | Tiempo de espera | No Aprobado | PLM1G3S-37 |

## Resumen de Issues Críticos
1. Validaciones de tarjeta inconsistentes
2. Problemas con el flujo de reserva
3. Fallas en el temporizador
4. Problemas de cancelación
5. Validaciones de campos incompletas

## Documentos a considerar 
Archivos

Figma [Desing](https://www.figma.com/design/I6nSmK36O9DINiDCYZsZeS/Urban-Routes-ES)  
Requisitos [Functionality](https://practicum-content.s3.us-west-1.amazonaws.com/new-markets/qa-sprint-3/ES/v6/Requisitos_para_la_funcionalidad_Compartir_un_auto.pdf)
