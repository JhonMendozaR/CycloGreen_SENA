# Prompts

## Descripción
Describe de manera detallada como es el flujo de funcionamiento de la aplicación, cómo interactúan los módulos entre si.
(Adjuntamos el docuemtno pdf → Reto SenaSoft)

### Respuesta
El flujo de funcionamiento de la aplicación se organiza en torno a dos roles principales: Usuario y Administrador, y cada módulo interactúa de manera integrada para garantizar el control de alquiler de bicicletas y la promoción de eventos. Primero, el módulo de autenticación permite a los usuarios registrarse o iniciar sesión, validando sus credenciales. Una vez autenticado, el módulo de bicicletas gestiona el inventario: muestra disponibilidad, permite seleccionar una bicicleta, registrar el alquiler y calcular la tarifa inicial. Cuando el usuario devuelve la bicicleta, este mismo módulo la marca como disponible y genera el valor final a pagar, aplicando descuentos automáticos según el módulo de estratos socioeconómicos. Paralelamente, el módulo de eventos habilita a los usuarios a inscribirse en ciclopaseos y a los administradores a publicarlos. Para la parte administrativa, el módulo de reportes consolida la información de alquileres y devoluciones para calcular las ganancias netas mensuales. Además, el módulo de geolocalización permite visualizar en un mapa interactivo la ubicación de las bicicletas en uso. Todos estos módulos se comunican entre sí mediante la capa backend, que centraliza la lógica de negocio, y la base de datos, que almacena usuarios, bicicletas, alquileres, tarifas y eventos. Finalmente, la capa frontend ofrece a usuarios y administradores una interfaz clara para interactuar con el sistema, mientras que el módulo de integración asegura la coherencia de la información en tiempo real, de modo que la disponibilidad, las tarifas y los reportes se actualicen automáticamente.

## Estructura
Quiero que actúes como un arquitecto de software y me generes un documento .md muy completo y detallado.

El documento debe describir de forma clara y estructurada un proyecto fullstack que tiene como propósito la gestión de alquiler de bicicletas y eventos de ciclopaseo para funcionarios y aprendices del SENA.

**Contenido del .md**

1. Introducción al proyecto
- Breve descripción del propósito.
- Objetivos generales y específicos.

2. Tecnologías usadas
- Frontend: HTML, CSS, JavaScript
- Backend: Java + Spring Boot
- Base de datos: PostgreSQL
- Control de versiones: GitHub
- Extras: Postman (pruebas), Figma (UI), IA (generación de código/documentación).

3. Arquitectura general del sistema
- Explica cómo interactúan el frontend, backend y base de datos.
- Incluye un diagrama en mermaid mostrando los módulos y su comunicación.

4. Estructura de carpetas (backend Java Spring Boot)
Describe en detalle la función de cada carpeta y lo que contiene:
- Entity: entidades principales con atributos clave.
- Repository: interfaces que gestionan el acceso a datos.
- DTO: objetos de transferencia de datos para comunicación entre capas.
- Service (Interface): define la lógica de negocio en interfaces.
- Impl (Service Implementation): implementaciones concretas de los servicios.
- Exception: manejo centralizado de errores y validaciones.
- Controller: controladores REST que exponen los endpoints.
- Config: configuración general (seguridad, CORS, base de datos, etc.).
👉 Aquí necesito que detalles qué archivo concreto debería existir dentro de cada carpeta y qué responsabilidad tendría.

5. Modelo de datos y relaciones
- Entidades: Usuario, Administrador, Bicicleta, Alquiler, Evento, ParticipaciónEvento, Reporte.
- Explicación de sus relaciones.
- Incluye un diagrama ER en mermaid con cardinalidades.

6. Flujo de funcionamiento
- Explica paso a paso cómo interactúa un usuario en el sistema (registro, autenticación, alquiler, devolución, participación en eventos).
- Explica las acciones de un administrador (gestión de bicicletas, publicación de eventos, generación de reportes).
- Incluye un diagrama de secuencia en mermaid.

7. Módulos funcionales
Para cada módulo del sistema, describe:
- Qué hace.
- Qué endpoints tendrá (al menos listar, crear, actualizar, eliminar, consultar).
- Qué datos envía y recibe (entrada/salida).
Módulos:
- Autenticación
- Gestión de usuarios
- Gestión de bicicletas
- Alquiler de bicicletas
- Eventos de ciclopaseo
- Reportes
- Geolocalización (mapa interactivo)
Buenas prácticas de desarrollo
- Uso de control de versiones con GitHub (naming conventions, branching, PRs).
- Pruebas con Postman.
- Documentación con OpenAPI/Swagger.
- Diseño UI/UX en Figma antes de implementar.
Plan de desarrollo
- Fases: análisis, diseño, desarrollo, pruebas, despliegue.
- Roles del equipo (frontend, backend, QA, diseño).
- Metodología recomendada (ágil/scrum).

**Extra**
El .md debe incluir diagramas en mermaid (arquitectura, ER, flujo de secuencia).
Debe estar estructurado de forma profesional y lista para ser usada como documentación base del proyecto.
