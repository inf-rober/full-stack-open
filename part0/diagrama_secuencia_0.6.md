```mermaid
sequenceDiagram
    participant Navegador
    participant Servidor
        activate Navegador
        Navegador->>Servidor: https://studies.cs.helsinki.fi/exampleapp/spa
        deactivate Navegador
        activate Servidor
        Servidor-->>Navegador: spa.js, main.css, spa, data.json, favicon.ico
        deactivate Servidor
        activate Navegador
        Note left of Servidor: SPA es el documento HTML
        Navegador->>Servidor: https://studies.cs.helsinki.fi/exampleapp/new_note_spa
        deactivate Navegador
        activate Servidor
        Servidor-->>Navegador: spa.js
        deactivate Servidor
        Note left of Servidor: Se ejecuta un fragmento de JavaScript en spa.js que actualiza solo la lista
```
