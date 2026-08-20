# Historial de versiones

## 1.7 — 20/08/2026

- **Nombre y marca definitivos**: la herramienta pasa de llamarse «Configurador MikroTik» a
  **OCR Mikrotik Clonner**, con el logotipo oficial como icono de la aplicación y en la
  cabecera de la ventana. El ejecutable pasa a llamarse `OCRMikrotikClonner.exe`.
- Primera publicación en abierto.
- La casilla de «Reset de fábrica previo» ya no queda cortada en la ventana: su texto ocupa
  dos líneas y el resto del bloque baja para dejarle sitio.

## 1.6 — 31/07/2026

- **Pestaña «Copiar configuración»**: descarga de un router en marcha el backup, el export y
  todos los certificados con sus claves, en una subcarpeta `identidad_fecha`, y borra del
  router los ficheros generados.
- **Reset de fábrica previo** con bootstrap generado en el momento
  (`run-after-reset=ocr_bootstrap.rsc`), cada comando con `:do on-error` para que un
  certificado que falle no tumbe el resto.
- **Rescate por Telnet**: si `api` y `ftp` están deshabilitados, entra por Telnet, los
  habilita, trabaja y los vuelve a dejar como estaban.
- El `.rsc` se importa **por secciones**, no de una pieza: si una falla, se registra y las
  demás se aplican igual.
- Enlace «Acerca de · Términos de uso» con versión, copyright y condiciones.
- Validado sobre un RB1100AHx2 real con RouterOS 6.47.7 y servidor OpenVPN.
