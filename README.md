# Bajo la piel

Sitio estático listo para GitHub Pages. Publicar el contenido de esta carpeta en main, raíz (/).

- index.html: inicio.
- experiencia.html: interacción.
- reflexión.html: reflexión (nombre UTF-8 con acento).
- estilo.css: estilos compilados.
- main.js: aplicación y animaciones, módulo ES compilado; incluye React.
- artwork/: imágenes originales y máscaras utilizadas.
- data/cenapred-report.json: informe oficial fechado, no señal en vivo.

No necesita npm ni servidor Node en producción. Para probar localmente, servir esta carpeta por HTTP (por ejemplo python3 -m http.server 8080). Abrir como file:// no es compatible con módulos ES y fetch.

## Datos
GitHub Pages no ejecuta el intermediario de CENAPRED. Esta edición utiliza un informe oficial incluido en data/cenapred-report.json, con fecha y procedencia visibles. El navegador revisa el archivo cada 15 minutos, pero solo cambia al publicar una nueva versión del JSON. La caducidad se calcula en el navegador y nunca se sustituye una consulta fallida por una simulación. El modo Demostración sigue siendo una opción explícita y etiquetada.

Para actualizar: en el proyecto fuente ejecutar npm run actualizar-informe y npm run entrega; volver a publicar. Para actualización automática se necesita una tarea de GitHub Actions que consulte CENAPRED y publique el JSON, o un servicio HTTPS externo con CORS autorizado. No se incluye ni se necesita ninguna clave privada.
