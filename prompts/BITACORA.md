# Bitacora de tecnicas avanzadas

Laboratorio 07: Tecnicas Avanzadas de Prompting.
Herramienta de IA usada: Gemini

## Ejercicio 2: Zero-shot, one-shot y few-shot

| Tipo      | Aciertos (de 5) | Formato de la respuesta                          | Todas con el mismo formato (Si/No) |
| --------- | --------------- | ------------------------------------------------ | ---------------------------------- |
| Zero-shot | 5               | Tabla                                            | Si                                 |
| One-shot  | 5               | Lista numerada con formato `"Texto" -> Etiqueta` | Si                                 |
| Few-shot  | 5               | Texto limpio `"Texto" -> Etiqueta` (sin números) | Si                                 |

## Ejercicio 3: Chain of Thought

| Pedido      | Respuesta de la IA | Muestra los pasos (Si/No) | Correcta (Si/No) |
| ----------- | ------------------ | ------------------------- | ---------------- |
| Directo     | 318.60             | No                        | Si               |
| Paso a paso | S/ 318.60          | Si                        | Si               |

**Reflexión:**
Ver el razonamiento paso a paso es útil porque permite auditar cada cálculo intermedio y detectar fácilmente si hubo algún error en la lógica, en lugar de confiar únicamente en una respuesta directa.

## Ejercicio 4: Role prompting

| Version        | Vocabulario (sencillo/tecnico)                                    | Usa ejemplos o codigo                                            | A quien le sirve mas                             |
| -------------- | ----------------------------------------------------------------- | ---------------------------------------------------------------- | ------------------------------------------------ |
| A. Sin rol     | Técnico intermedio (espacio reservado en memoria, tipos de datos) | Sí, analogía de la caja y código en Python                       | A estudiantes que buscan una explicación directa |
| B. Rol docente | Sencillo y didáctico (lenguaje cotidiano)                         | Sí, analogías de estantes y ejemplo de videojuego (puntos/vidas) | A principiantes que nunca han programado         |
| C. Rol senior  | Técnico avanzado (RAM, Heap, Scope, Garbage Collector)            | Sí, snippet en Java y buenas prácticas de desarrollo             | A desarrolladores o practicantes de ingeniería   |

**Reflexión:**
Asignar un rol específico ayuda a ajustar la profundidad técnica, el tono y las analogías de la respuesta para que se adapten exactamente al nivel de conocimiento del usuario destinatario.

## Ejercicio 5: Descomposicion

Paso 1: La IA me dio los 5 requisitos principales del sistema de inventario.

Paso 2: La IA diseño las clases necesarias y sus atributos con tipos de datos.

Paso 3: La IA genero el codigo Java de la clase Producto con constructor, getters y setters.

Paso 4: La IA reviso el codigo y propuso 3 mejoras: validar precio, validar stock y agregar toString().

Comparacion: El pedido de una sola vez dio una respuesta general. Al dividirlo en pasos obtuve una solucion mas ordenada, detallada y coherente.

## Ejercicio 6: Prompt estructurado y autocritica

```text
<rol>Actua como analista de pruebas de software.</rol>
<contexto>Login web con correo y contrasena. La cuenta se bloquea despues de 3 intentos fallidos.</contexto>
<tarea>Piensa paso a paso que puede fallar y escribe 6 casos de prueba.</tarea>
<formato>Tabla con las columnas: ID, escenario, datos de entrada, resultado esperado.</formato>

Mensaje de autocrítica enviado:
Revisa tu tabla: faltan casos limite como campos vacios, correo sin @ o contrasena con espacios? Agrega los que falten e indica cuales agregaste.
```
