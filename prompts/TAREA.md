# Tarea: Mi prompt avanzado

## Tarea elegida

## Version 1: prompt basico

```text
Genera casos de prueba para un registro de usuarios.
```

## Version 2

<rol>Actúa como QA Automation Engineer especialista en pruebas funcionales.</rol>
<contexto>Formulario de registro con campos: Nombre completo, Correo electrónico y Contraseña (mínimo 8 caracteres, al menos un número).</contexto>
<tarea>Escribe casos de prueba para este módulo de registro.</tarea>
<formato>Tabla en Markdown con las columnas: ID, Escenario, Datos de entrada, Resultado esperado.</formato>

## Version 3: prompt final

<rol>Actúa como QA Automation Engineer especialista en pruebas funcionales y de seguridad web.</rol>
<contexto>Formulario de registro de usuario con campos: Nombre completo, Correo electrónico y Contraseña (mínimo 8 caracteres, al menos un número y una mayúscula).</contexto>
<tarea>Piensa paso a paso en los caminos felices, errores de validación de campos obligatorios/formatos y casos límite de seguridad simples. Genera 6 casos de prueba estructurados.</tarea>
<formato>Tabla Markdown con las columnas: ID, Escenario, Datos de entrada, Resultado esperado.</formato>

## Tecnicas usadas en el prompt final

| Parte del prompt final                            | Técnica correspondiente |
| ------------------------------------------------- | ----------------------- |
| `<rol>Actúa como QA Automation Engineer...</rol>` | **Role Prompting**      |
| `<contexto>`, `<tarea>`, `<formato>`              | **Prompt Estructurado** |
| `Piensa paso a paso en los caminos felices...`    | **Chain of Thought**    |

## Evaluacion del resultado

| Qué revisar                                               | Cumple (Sí / No) |
| --------------------------------------------------------- | ---------------- |
| ¿Utiliza un rol específico de QA sin usar "experto"?      | Sí               |
| ¿El resultado está presentado en tabla con 4 columnas?    | Sí               |
| ¿Incluye escenarios felices, validaciones y casos límite? | Sí               |
| ¿Se aplicaron al menos 3 técnicas de prompting?           | Sí               |

## Por que elegi estas tecnicas

Elegí estas técnicas porque la tarea de QA exige alta precisión. El rol define el enfoque técnico, la estructura impone un formato rígido en tabla sin ambigüedades, y el pensamiento paso a paso asegura que la IA analice errores límite antes de generar la respuesta.
