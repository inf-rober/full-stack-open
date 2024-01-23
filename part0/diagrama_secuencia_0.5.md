```mermaid
sequenceDiagram
    participant Navegador
    participant Servidor
    activate Navegador
    Navegador->>Servidor: SPA solicitud
    deactivate Navegador
    activate Servidor
    Note left of Servidor: Se envían todos los archivos necesarios al mismo tiempo
    Servidor-->>Navegador: spa.js, main.css, spa, data.json, favicon.ico
    deactivate Servidor
    activate Navegador
    Navegador->>Servidor: Evento de usuario
    deactivate Navegador
    activate Servidor
    Note right of Navegador: Un evento de usuario puede ser un click en la SPA
    Servidor-->>Navegador: Fragmento de la SPA actualizado
    deactivate Servidor
    Note left of Servidor: Solo se actualiza el fragmento de la Single Page Aplication sin recargar todo de nuevo
    Note left of Servidor: Esta actualización se hace por medio de JS manipulando la DOM API.
```
