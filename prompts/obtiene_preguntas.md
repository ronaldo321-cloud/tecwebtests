# Generador de Preguntas Tipo Test sobre JavaScript

## Rol

Actúa como un docente experto en Desarrollo Web y JavaScript, especializado en la creación de material didáctico y evaluaciones técnicas.

## Objetivo

Genera exactamente **10 preguntas tipo test** sobre el tema indicado al final del prompt.

## Requisitos de las preguntas

- Cada pregunta debe tener un nivel de dificultad adecuado para estudiantes que estén aprendiendo JavaScript.
- Las preguntas deben evaluar comprensión conceptual, sintaxis, funcionamiento y buenas prácticas relacionadas con el tema.
- Evita preguntas ambiguas o con múltiples interpretaciones válidas.
- No repitas conceptos ni enfoques entre preguntas.

## Requisitos de las respuestas

Cada pregunta debe contener exactamente:

- 1 pregunta.
- 4 opciones de respuesta.
- 1 única respuesta correcta.
- Una explicación breve que:
  - Justifique por qué la respuesta correcta es válida.
  - Explique por qué las demás opciones son incorrectas.

## Distribución aleatoria y equilibrada de respuestas correctas

Para evitar sesgos en los tests:

- La respuesta correcta debe distribuirse de forma equilibrada entre las cuatro posiciones posibles.
- En un conjunto de 10 preguntas:
  - La opción **A** debe ser correcta aproximadamente el 25% de las veces.
  - La opción **B** debe ser correcta aproximadamente el 25% de las veces.
  - La opción **C** debe ser correcta aproximadamente el 25% de las veces.
  - La opción **D** debe ser correcta aproximadamente el 25% de las veces.
- No permitas que la respuesta correcta se concentre repetidamente en la misma posición.
- Reordena las opciones cuando sea necesario para cumplir una distribución equilibrada.
- La posición de la respuesta correcta no debe seguir patrones evidentes.

## Formato de salida

Devuelve únicamente un objeto JSON válido sin texto adicional, comentarios ni bloques de código.

Utiliza exactamente la siguiente estructura:

{
  "tema": "Nombre del tema",
  "preguntas": [
    {
      "pregunta": "Texto de la pregunta",
      "opciones": [
        "Opción A",
        "Opción B",
        "Opción C",
        "Opción D"
      ],
      "correcta": 0,
      "explicacion": "Explicación breve de la respuesta correcta."
    }
  ]
}

## Restricciones del JSON

- El campo `correcta` debe contener el índice numérico de la respuesta correcta:
  - 0 = A
  - 1 = B
  - 2 = C
  - 3 = D
- El JSON debe ser completamente válido y parseable mediante `JSON.parse()`.
- No incluyas comas sobrantes.
- No añadas propiedades distintas de las especificadas.
- Genera exactamente 10 elementos dentro del array `preguntas`.

## Tema

Clase String
