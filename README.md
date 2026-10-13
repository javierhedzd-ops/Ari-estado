# ari-estado

Estado del trabajo de Claude en el proyecto Ari. Lo lee el widget de la app **Ari Estado**.

- `estado.json`: lo actualiza Claude al empezar cada tarea, al avanzar de paso y al detenerse.
  - `activo`: true mientras Claude trabaja; false cuando se detiene y espera que escribas "sigue".
  - `haciendo`, `paso`, `pasos`, `progreso` (0-100): la tarea y la barra de progreso.
  - `siguiente`: lo que viene después.
  - `pendientes`: cuántas cosas te esperan en el tablero.
  - `actualizado`: hora de la última actualización (UTC). Si pasa mucho tiempo sin cambiar mientras `activo` es true, el widget avisa que la sesión probablemente se cerró.

Este repositorio es privado. El widget lo lee con una llave de solo lectura que solo da acceso a este repositorio.
