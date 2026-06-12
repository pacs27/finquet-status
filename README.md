# finquet-status

Avisos de incidencias para la app de Finquet. La app lee `status.json`.

Para activar un aviso: editar `status.json` con `active: true`, un `id` nuevo y el `message`, y commit a `main`.

```json
{
  "schema_version": 1,
  "incident": {
    "id": "2026-06-15-incidencia",
    "active": true,
    "severity": "warning",
    "message": {
      "es": "Texto que ve el usuario.",
      "en": "Text the user sees."
    },
    "url": null
  }
}
```

`message`: objeto por idioma (`es`, `en`, `fr`, `de`, `it`, `nl`, `el`) — la app usa el idioma del usuario con fallback en→es. También admite un string simple.

`severity`: `info` | `warning` | `critical` (critical no se puede descartar, solo minimizar). Para desactivar: `active: false`.
