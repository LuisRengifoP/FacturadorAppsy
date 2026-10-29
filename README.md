# Facturador de Rutas

Interfaz web para automatizar la facturación de rutas de vendedores sobre un DMS. Pensada para lanzar corridas de facturación, detectar novedades (pedidos que quedaron sin facturar) y enviar un resumen claro por Telegram.

Este repositorio contiene la **interfaz de usuario (UI)** en un único archivo HTML, sin backend ni datos reales. Es la base visual sobre la que se conecta la lógica de facturación.

## Vista previa

La aplicación es un dashboard de una sola página con navegación lateral y cuatro secciones:

- **Corrida** — formulario de ruta/rango, barra de progreso y tabla con el avance de cada vendedor.
- **Novedades** — pedidos que quedaron sin facturar, con el vendedor afectado y la acción sugerida.
- **Historial** — métricas acumuladas, gráfico de pedidos por día y detalle de las últimas corridas.
- **Telegram** — plantilla del mensaje de resumen que se envía al terminar una corrida.

## Características de la UI

- Tema claro y oscuro (automático según el sistema, con botón para alternar).
- Diseño responsive (escritorio, tablet y móvil).
- Tarjetas de métricas, tablas con estados por color y notificaciones (toasts).
- Estados vacíos en todas las secciones mientras no hay datos.
- Cero dependencias de build: HTML, CSS y JavaScript en un solo archivo.
- Tipografías cargadas desde Google Fonts (Poppins, Inter, JetBrains Mono).

## Uso

No requiere instalación. Abre el archivo en cualquier navegador moderno:

```
Facturador de Rutas - UI.html
```

O sírvelo con un servidor estático simple:

```bash
python -m http.server 8000
```

Luego abre `http://localhost:8000/Facturador%20de%20Rutas%20-%20UI.html`.

> Nota: esta versión es solo la interfaz. Los botones **Facturar**, **Solo revisar** y **Probar conexión** muestran mensajes de ejemplo; aún no hay conexión con un DMS real.

## Estructura

```
.
├── Facturador de Rutas - UI.html   # Interfaz limpia, sin datos de prueba
├── Facturador de Rutas.html        # Demo con datos de ejemplo (referencia)
└── README.md
```

## Roadmap

- [ ] Conexión real con el DMS.
- [ ] Guardado de rutas.
- [ ] Envío automático del resumen a Telegram.
- [ ] Persistencia del historial de corridas.

## Licencia

Sin licencia definida. Agrega una (por ejemplo, MIT) antes de publicar si quieres permitir su reutilización.
