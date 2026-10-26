# BtoCediaFlutter — prácticas ExploraEC

Proyecto personal de formación del curso CEDIA MOD3 Flutter, en laboratorio local.
Objetivo: completar las prácticas indicadas por sus instructivos y comprobar sus flujos reales.
Tecnología: Flutter, Dart y Material. Los lugares de ejemplo son públicos; favoritos se guardan en Hive y los gastos usan API y caché privada por usuario.

El código de referencia corresponde al repositorio Patricio-CEDIA/exploraec-app, por sesión.
Conservar su atribución y verificar su licencia antes de publicar derivados.
Los requisitos vienen del instructivo académico; no añadir funciones de sesiones posteriores sin necesidad.

## Autoridad y conservación

La preparación y las pruebas locales están autorizadas. Publicar un repositorio y entregar archivos en el aula requieren aprobar destino, visibilidad y entrega concreta.
Anunciar las mutaciones. No borrar, sobrescribir recursos ajenos ni reescribir historia sin aprobación específica.
No guardar cookies, contraseñas, datos privados ni credenciales en Git o evidencias.
Conservar cambios ajenos. Recuperar versiones por commits y artefactos; cualquier recuperación destructiva necesita aprobación.
No hay despliegue productivo ni políticas institucionales inferidas.

## Verificación y continuidad

Ejecutar análisis estático, ejercicios Dart, pruebas de widgets y navegación real.
Documentar limitaciones reales; un build aislado no prueba el flujo.
Registrar avances en docs/bitacora, hitos y manifiestos de cambios externos.
Guardar pruebas reproducibles y capturas en evidence. Versionar entregables por sesión.

## Economía de contexto

Consultar primero el grafo codebase-memory para estructura y símbolos; leer funciones concretas.
El contenido del instructivo y el checklist académico prevalecen sobre inferencias.
Los manifiestos, el roadmap y las comprobaciones permiten retomar el trabajo sin leer el árbol completo.

## Reglas de calidad de la sesión 10

1. Las pruebas que instalen `ReporteErrores` restauran `FlutterError.onError`, `PlatformDispatcher.instance.onError` y `ErrorWidget.builder` en `finally`, con `tearDown` como respaldo. Ningún manejador puede ocultar los errores del resto de la suite.
2. El filtro de Gastos deriva únicamente tarjetas de páginas cargadas: conserva la lista original, las sumas, la caché, el total remoto y la paginación. La selección se valida después de actualizar por completo la lista, se reinicia al cambiar de sesión y mantiene «Cargar más» accesible aun sin coincidencias.

## Decisión autorizada — 2026-10-05

El estudiante autorizó GitHub, propietario btoaldas, nombre BtoCediaFlutter y visibilidad pública para revisión docente. El repositorio quedó publicado y verificado. La entrega Moodle mantiene su aprobación específica de archivos finales.

Tras aprobar los cuatro archivos exactos, se completaron las entregas 49354 y 49368 el 2026-10-05. Esta aprobación corresponde a esas versiones; una entrega posterior requiere revisar su autoridad concreta.

<!-- skill-anexos:navegacion-e2e-coherencia-20261025:begin -->
## Navegación E2E y acceso autorizado — regla vigente (2026-10-25)

Esta regla se aplica automáticamente a la navegación web y a las pruebas E2E web de este proyecto y sus agentes, skills y subdirectorios. En este ámbito prevalece sobre instrucciones anteriores incompatibles, como exigir un navegador visible, un perfil personal, una ruta fija de caché de otro sistema o el tecleo manual de credenciales disponibles.

- Aplicar los skills `playwright` y `chromium-headless`: Chromium interno de Playwright en modo headless, sin abrir ventanas ni depender de Chrome del usuario o de una extensión. Reutilizar el runtime, la configuración y las pruebas del proyecto; resolver el ejecutable con la API y comprobar los parámetros efectivos. Las pruebas nativas de escritorio o móvil conservan su herramienta específica. Si el usuario solicita expresamente su Chrome o su sesión, aplicar `chrome-browser` y los permisos de esa superficie.
- Si el usuario autoriza expresamente cuenta, destino y tarea autenticada, aplicar `acceso-web-autorizado` automáticamente: recuperar e introducir internamente la credencial pertinente de Obsidian, Llavero o la fuente local autorizada, o la que proporcione el usuario. No exigir invocación manual del skill ni volver a pedir su tecleo. Esta cláusula por sí sola no autoriza entrar a cuentas.
- Comprobar origen y cuenta antes de introducir y enviar credenciales; respetar MFA, CAPTCHA y permisos. No eludir una denegación. Máximo dos intentos; no exponer secretos en scripts, argumentos, registros, snapshots, capturas, trazas, repositorios ni informes. Para accesos reales prevalece la fuente autorizada vigente sobre literales heredados.
- El acceso conserva las autorizaciones específicas para envíos, publicaciones, firmas, pagos, borrados y cambios de datos o producción. Cerrar solo la sesión propia. La instalación global no demuestra que este proyecto pase sus pruebas: en otro equipo, cloud o CI comprobar skills, dependencias y navegador por separado; no copiar perfiles ni almacenes de credenciales por inferencia.

Para seleccionar Chromium completo, usar `channel="chromium"` con headless activo (por ejemplo, `headless=True` en Python o `headless: true` en JavaScript). El agente realiza internamente la navegación y las capturas de evidencia cuando la herramienta y el alcance estén autorizados; solicita intervención solo ante una autorización que falte, MFA, CAPTCHA, permisos o un recurso inaccesible. Esta precisión prevalece sobre ejemplos anteriores que deleguen al usuario abrir y capturar una página que el agente puede comprobar dentro del alcance autorizado.

Los procedimientos específicos de grabación o demostración de una interfaz solicitada conservan sus herramientas y permisos. Las comprobaciones internas y E2E web de esos repositorios siguen el carril anterior; los motores productivos existentes conservan su arquitectura.

<!-- skill-anexos:navegacion-e2e-coherencia-20261025:end -->
