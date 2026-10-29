---
name: TestGen
description: Convierte apuntes, diapositivas, resúmenes o temarios en tests tipo examen (opción múltiple, verdadero/falso y preguntas cortas) con soluciones explicadas. Úsala siempre que el usuario pida un test, simulacro, preguntas de repaso, autoevaluación o "ponme a prueba" sobre algún material de estudio, aunque no diga la palabra "test". También cuando pegue apuntes y diga que tiene un examen cerca.
---

# Tests de estudio

Genera tests de repaso a partir del material que aporte la persona. El objetivo es que sirvan para estudiar de verdad: preguntas parecidas a las de un examen real, con errores plausibles como distractores y una explicación que enseñe algo cuando se falla.

## Antes de generar

1. **Identifica el material.** Si hay apuntes pegados o archivos adjuntos, trabaja solo con ellos. Si no hay nada, pide el tema o el material en una sola pregunta. Inventar contenido que no está en los apuntes hace que la persona estudie cosas que no le van a entrar.
2. **Fija los parámetros con valores por defecto razonables** y no preguntes por cada uno:
   - Número de preguntas: 10 (si el material es corto, menos).
   - Tipo: opción múltiple de 4 opciones (A-D) con una sola correcta.
   - Dificultad: mezcla de recordar, comprender y aplicar.
   - Si la persona indica otro número, tipo o nivel, respétalo.
3. **Detecta el contexto del examen** si lo menciona (asignatura, fecha, formato del profesor) y adapta el estilo: un examen de código pide preguntas de "¿qué imprime este fragmento?", uno teórico pide definiciones y comparaciones.

## Cómo escribir buenas preguntas

- Una pregunta evalúa una sola idea. Si hace falta una "y" para explicarla, divídela.
- Los distractores deben ser errores que alguien cometería de verdad (confundir dos conceptos parecidos, un valor límite mal recordado, un orden invertido). Un distractor absurdo no enseña nada.
- Evita "todas las anteriores" y "ninguna de las anteriores": permiten acertar sin saber.
- Reparte las respuestas correctas entre A, B, C y D sin patrón visible.
- Mantén las opciones de longitud parecida; si la correcta es siempre la más larga, se acierta por intuición.
- Cuando el material lo permita, incluye preguntas de aplicación con un caso o fragmento de código, no solo definiciones.
- Cubre el material de forma proporcional: no concentres todas las preguntas en el primer tema.

## Formato de salida

Entrega primero el test completo sin soluciones y después la plantilla de corrección, para que la persona pueda hacerlo sin ver las respuestas:

```
# Test: [Tema]
[N] preguntas · [tipo] · [dificultad]

**1.** Enunciado
A) ...
B) ...
C) ...
D) ...

(...resto de preguntas...)

---

## Soluciones y explicaciones

**1. Respuesta: C.** Por qué es correcta, y en una línea por qué la tentadora (B) falla.
```

Cada explicación debe responder a "¿por qué esta y no la que yo habría elegido?". Añade, cuando sea útil, una referencia al apartado de los apuntes de donde sale.

## Cierre

Termina con una línea que ofrezca el siguiente paso útil: repetir el test con otras preguntas, subir la dificultad, o centrarse en los temas que la persona suela fallar. Si la persona responde con sus respuestas, corrígelas, indica la nota y resume qué temas conviene repasar.

## Ejemplo

**Entrada:** apuntes sobre el modelo cliente-servidor HTTP, "hazme 3 preguntas".

**Salida (extracto):**

**1.** ¿Qué código de estado HTTP indica que el recurso solicitado no existe?
A) 200
B) 301
C) 404
D) 500

**Soluciones:** **1. Respuesta: C.** 404 significa "Not Found". El 500 es la tentadora: indica un error interno del servidor, no un recurso inexistente.
