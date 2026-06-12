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
    "message": "Texto que ve el usuario.",
    "url": null
  }
}
```

`severity`: `info` | `warning` | `critical` (critical no se puede descartar). Para desactivar: `active: false`.
