# ari-estado

Estado del trabajo de Claude en el proyecto Ari. Lo lee el widget de la app **Ari Estado**.

- `estado.json`: lo actualiza Claude al empezar cada tarea, al avanzar de paso y al detenerse.
  - `activo`: true mientras Claude trabaja; false cuando se detiene y espera que escribas "sigue".
  - `haciendo`, `paso`, `pasos`, `progreso` (0-100): la tarea y la barra de progreso.
  - `siguiente`: lo que viene después.
  - `pendientes`: cuántas cosas te esperan en el tablero.
  - `actualizado`: hora de la última actualización (UTC). Si pasa mucho tiempo sin cambiar mientras `activo` es true, el widget avisa que la sesión probablemente se cerró.

- `sesion`: enlace a la sesión de Claude Code donde se escribe "sigue".

Este repositorio es **público**: desde Ari Estado 0.3.0 el widget lo lee sin llave. Por eso aquí nunca va nada sensible (ni llaves, ni datos personales, ni pláticas): solo el avance del trabajo. Si algún día vuelve a ser privado, Ari Estado acepta una llave de solo lectura en "Opciones avanzadas".
