# TestGen-Claude-Skill

Una skill para Claude que convierte apuntes, diapositivas o temarios en **tests tipo examen** con soluciones explicadas.

Pensada para estudiantes: preguntas con distractores realistas, reparto proporcional del temario y una explicación que enseña algo cuando se falla.

## Qué hace

- Genera tests de opción múltiple (A-D) a partir del material que le des.
- Mezcla preguntas de recordar, comprender y aplicar (incluidas preguntas con fragmentos de código).
- Separa el test de las soluciones para que puedas hacerlo sin ver las respuestas.
- Explica por qué la respuesta correcta lo es y por qué la opción tentadora falla.
- Corrige tus respuestas y te dice qué temas repasar.

## Instalación

### Claude.ai

1. Descarga este repositorio como ZIP o clonalo.
2. En Claude, ve a **Configuración → Capacidades → Skills** y sube la carpeta comprimida.
3. Activa la skill.

### Claude Code

Copia la carpeta en tu directorio de skills:

```bash
cp -r tests-de-estudio ~/.claude/skills/
```

## Uso

Pega tus apuntes (o adjunta el archivo) y escribe algo como:

- "Hazme un test de 10 preguntas con estos apuntes."
- "Ponme a prueba con el tema de HTTP, nivel difícil."
- "Tengo examen de JavaScript el viernes, hazme un simulacro."

Parámetros que puedes indicar: número de preguntas, tipo, dificultad y asignatura.

## Ejemplo de salida

```
# Test: Protocolo HTTP
3 preguntas · opción múltiple · media

**1.** ¿Qué código de estado HTTP indica que el recurso solicitado no existe?
A) 200
B) 301
C) 404
D) 500

---

## Soluciones y explicaciones

**1. Respuesta: C.** 404 significa "Not Found". El 500 es la tentadora:
indica un error interno del servidor, no un recurso inexistente.
```

## Estructura

```
tests-de-estudio/
├── SKILL.md    # instrucciones de la skill
├── README.md   # este archivo
└── LICENSE     # MIT
```

## Contribuir

Las sugerencias son bienvenidas: abre un issue o un pull request con mejoras al formato, nuevos tipos de pregunta (verdadero/falso, respuesta corta) o casos de uso.

## Licencia

MIT. Consulta el archivo [LICENSE](LICENSE).
