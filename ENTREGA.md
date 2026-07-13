# Entrega — Ejercicio OpenSpec

## 1. Evidencia de instalación

### `openspec --version`
 ``` /ai4devs-openspec-sandbox-202607$ openspec --version
 1.6.0
 ```
 

### `ls -R openspec/`
 ```/ai4devs-openspec-sandbox-202607$ ls -R openspec/
 openspec/:
 changes  config.yaml  specs
 
 openspec/changes:
 archive

 openspec/changes/archive:

 openspec/specs:
 ```
 

## 2. Parte A — Los 3 Pilares

**Micro-tarea:** Función que detecte si un string es palíndromo

**Pilar 1 — Herramienta:** Visual Studio Code + Claude Code (ya cuento con la suscripción)

**Pilar 2 — Contexto:**
- Lenguaje: [Web]
- Framework: ninguno
- Restricciones: no aceptar strings con números
- Omitido conscientemente: el framework

**Pilar 3 — Prompt:**
 Objetivo: Genera una web donde ingrese un string y que identifique si el string ingresado es un palíndromo.
 Criterio de éxito:
 - String ingresada "oso". Texto de salida "SÍ es un palíndromo"
 - String ingresada "tela". Texto de salida "NO es un palíndromo"

 Restricciones:

 Si el string ingresado tiene caracteres que no son letras, dar el texto de salida "Error, solo debes ingresar palabra o frases con letras"

**Resultado:** No funcionó a la primera. Claude Code propuso dos condiciones adicionales:
- Aceptar espacios (para permitir frases como "anita lava la tina")
- Ignorar acentos al comparar ("único" se evalúa como "unico")

Mejora que haría si volviera a hacerlo: definir desde el prompt inicial si acepto frases con espacios o solo palabras sueltas, y si los acentos deben romper o no el palíndromo — en vez de dejar que la herramienta me lo preguntara después.

## 3. Observaciones de la exploración de OpenSpec

1. Esta versión (1.6.0) no genera `openspec/project.md` como "constitución" del proyecto — usa `config.yaml` en su lugar. 
2. Las carpetas `changes/` y `specs/` nacen completamente vacías — OpenSpec no viene con ejemplos precargados, es un lienzo en blanco que se llena con el primer `/opsx:propose`.
3. El contexto del proyecto en `config.yaml` es opcional, no obligatorio — trae ejemplos comentados (stack, convenciones, reglas por artefacto)

