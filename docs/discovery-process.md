# Proceso de relevamiento adaptativo

## Objetivo

Definir qué debe hacer un empleado digital sin partir de un cuestionario fijo y excesivamente específico.

El relevamiento debe comenzar con pocas preguntas amplias. A partir de las respuestas, el diseñador identifica procesos, actores, herramientas, riesgos y oportunidades de automatización. Recién después formula preguntas específicas para completar los detalles faltantes.

## Principio central

```text
Preguntas generales
        ↓
Mapa inicial del negocio
        ↓
Detección de procesos y capacidades
        ↓
Preguntas específicas por proceso
        ↓
Definición de skills, workflows, permisos e integraciones
```

No se debe comenzar con una lista de cien preguntas cerradas, porque:

- muchas no aplicarán al cliente;
- puede generar respuestas superficiales;
- puede omitir procesos no contemplados;
- fuerza al cliente a pensar según la estructura del diseñador;
- dificulta detectar cómo trabaja realmente la organización.

## Etapa 1: entrevista abierta

La primera etapa debe incluir pocas preguntas y pedir respuestas amplias, con ejemplos reales.

### Pregunta 1 — Negocio y contexto

Describí cómo funciona el negocio, qué vende o qué servicio presta, quiénes participan y cómo se organiza actualmente.

### Pregunta 2 — Trabajo cotidiano

Contá qué tareas realizan todos los días o todas las semanas las personas que este empleado digital debería ayudar.

### Pregunta 3 — Problemas actuales

Explicá qué cosas suelen olvidarse, demorarse, repetirse, hacerse mal o depender demasiado de una persona.

### Pregunta 4 — Flujo de información

Describí cómo entra la información, dónde se guarda, quién la consulta y cómo se actualiza.

### Pregunta 5 — Herramientas

Enumerá las aplicaciones, sistemas, planillas, canales y documentos utilizados, indicando para qué sirve cada uno.

### Pregunta 6 — Decisiones y acciones

Explicá qué decisiones toman las personas y qué acciones ejecutan después de cada decisión.

### Pregunta 7 — Comunicación

Describí con quiénes se comunican, por qué canales, qué tipos de mensajes manejan y cuáles son internos o externos.

### Pregunta 8 — Riesgos y límites

Indicá qué errores serían graves, qué información es sensible y qué cosas el empleado digital nunca debería hacer solo.

### Pregunta 9 — Resultado esperado

Describí cómo sería una jornada ideal usando el empleado digital y qué mejoras concretas deberían observarse.

### Pregunta 10 — Casos reales

Contá entre tres y cinco situaciones reales recientes que representen el trabajo que se quiere mejorar.

## Etapa 2: análisis de las respuestas

El diseñador debe transformar las respuestas abiertas en un mapa estructurado.

### Entidades detectadas

Ejemplos:

- clientes;
- oportunidades;
- conversaciones;
- productos;
- repuestos;
- pedidos;
- facturas;
- pagos;
- tareas;
- responsables;
- documentos.

### Procesos detectados

Ejemplos:

- seguimiento comercial;
- preparación de respuestas;
- consulta de stock;
- revisión de pagos;
- actualización de CRM;
- elaboración de reportes;
- derivación interna.

### Sistemas detectados

Ejemplos:

- CRM;
- WhatsApp;
- Telegram;
- correo;
- Google Sheets;
- Calendar;
- sistema contable;
- software de inventario.

### Acciones detectadas

Cada acción debe clasificarse inicialmente como:

- `read_only`;
- `draft`;
- `approval_required`;
- `automatic`;
- `forbidden`.

### Información faltante

El diseñador debe registrar contradicciones, datos ambiguos, reglas no documentadas y decisiones pendientes.

## Etapa 3: generación de preguntas específicas

Las preguntas específicas no deben estar todas predefinidas. Se generan según los procesos detectados.

### Ejemplo: seguimiento comercial

Si el cliente menciona que pierde oportunidades o se olvida de contactar personas, preguntar:

- ¿Qué evento indica que debe hacerse un seguimiento?
- ¿Cuánto tiempo puede pasar sin contacto?
- ¿Cómo se define la prioridad?
- ¿Quién es responsable?
- ¿Qué estados existen en el CRM?
- ¿Qué casos no deben generar recordatorio?

### Ejemplo: preparación de respuestas

Si el cliente quiere ayuda para responder mensajes, preguntar:

- ¿Qué información debe consultarse antes de redactar?
- ¿Qué compromisos no se pueden asumir?
- ¿Qué precios, plazos o descuentos requieren autorización?
- ¿Qué tipos de mensajes deben derivarse?
- ¿El asistente solo redacta o también puede enviar?

### Ejemplo: pagos pendientes

Si el cliente necesita revisar pagos, preguntar:

- ¿Cuál es la fuente oficial del estado de pago?
- ¿Qué estados posibles existen?
- ¿Cómo se identifica cada operación?
- ¿Qué diferencia hay entre informado, recibido y acreditado?
- ¿Quién puede confirmar o modificar un pago?

### Ejemplo: repuestos y stock

Si el cliente trabaja con repuestos, preguntar:

- ¿Cómo se identifica una pieza?
- ¿Qué datos determinan compatibilidad?
- ¿Dónde se consulta stock?
- ¿Qué fuente define el precio vigente?
- ¿Cuándo una consulta debe derivarse a una persona?

## Etapa 4: cierre del relevamiento

El relevamiento termina cuando se pueden definir sin ambigüedad:

- objetivo del empleado digital;
- usuarios;
- entidades;
- procesos;
- skills;
- workflows;
- integraciones;
- fuentes oficiales;
- permisos;
- acciones prohibidas;
- condiciones de derivación;
- pruebas de aceptación.

## Regla de completitud

No existe un número fijo de preguntas.

El relevamiento está completo cuando cada acción importante tiene:

1. un disparador;
2. entradas definidas;
3. una fuente de información;
4. una secuencia;
5. una salida esperada;
6. un nivel de permiso;
7. manejo de errores;
8. condición de derivación;
9. casos de prueba.

## Responsabilidad del diseñador

La entrevista no debe ser ejecutada como un formulario ciego. El diseñador debe:

- interpretar respuestas;
- detectar procesos ocultos;
- pedir ejemplos;
- identificar contradicciones;
- proponer una primera arquitectura;
- validar esa arquitectura con el cliente;
- formular preguntas específicas solamente donde falte definición.
