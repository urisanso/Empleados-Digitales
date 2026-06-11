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

## Cómo crear un nuevo empleado

1. Copiar `clients/_template/`.
2. Completar la configuración del cliente.
3. Seleccionar las skills necesarias.
4. Configurar integraciones y permisos.
5. Definir workflows.
6. Cargar conocimiento autorizado.
7. Completar y ejecutar los tests.
8. Implementar primero en modo interno o borrador.
9. Habilitar automatizaciones gradualmente.

## Reglas de diseño

- Una skill resuelve una capacidad concreta.
- Un workflow combina varias skills.
- La lógica genérica no debe contener datos de clientes.
- Las credenciales nunca se guardan en el repositorio.
- Toda acción nueva comienza como `draft` o `approval_required`.
- Las acciones automáticas deben habilitarse explícitamente.
