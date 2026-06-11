# Empleados Digitales

Framework base para crear asistentes digitales modulares, reutilizables y seguros.

El objetivo es que todos compartan la misma arquitectura y que cambien solamente la lógica del negocio, las aplicaciones conectadas, los permisos, los workflows y el conocimiento de cada cliente.

## Fórmula de implementación

```text
Empleado digital
=
Core común
+ Configuración del cliente
+ Skills reutilizables
+ Workflows
+ Integraciones
+ Conocimiento
+ Permisos
+ Tests
```

## Enfoque por defecto

Estos asistentes deben funcionar primero como copilotos internos:

- consultan CRM, planillas, calendarios y sistemas internos;
- resumen conversaciones;
- detectan seguimientos pendientes;
- preparan respuestas;
- alertan sobre pagos, tareas y oportunidades;
- proponen acciones;
- esperan aprobación antes de ejecutar acciones sensibles.

No deben responder automáticamente a clientes salvo habilitación expresa, alcance limitado y pruebas aprobadas.

## Estructura

```text
core/          Reglas comunes obligatorias
clients/       Configuración específica de cada cliente
skills/        Capacidades reutilizables
workflows/     Procesos que combinan skills
integrations/  Contratos y configuración de aplicaciones
knowledge/     Información consultable del negocio
tests/         Pruebas funcionales y de seguridad
templates/     Plantillas limpias para crear módulos
docs/          Documentación de arquitectura y despliegue
scripts/       Automatizaciones auxiliares
```

## Qué querés hacer

```text
Quiero crear un nuevo empleado
→ leer docs/discovery-process.md

Quiero agregar una nueva capacidad
→ leer skills/README.md

Quiero conectar una nueva aplicación
→ leer integrations/README.md

Quiero definir un proceso de negocio
→ leer workflows/README.md

Quiero cargar información del negocio
→ leer knowledge/README.md

Quiero configurar un cliente
→ leer clients/README.md

Quiero probar una implementación
→ leer tests/README.md
```

## Reglas de diseño

- Una skill resuelve una capacidad concreta.
- Un workflow combina varias skills.
- La lógica genérica no debe contener datos de clientes.
- Las credenciales nunca se guardan en el repositorio.
- Toda acción nueva comienza como `draft` o `approval_required`.
- Las acciones automáticas deben habilitarse explícitamente.
