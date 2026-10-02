NEXUS FITNESS · Centro integral de fitness y bienestar
=====================================================

Cómo abrirlo
  1. Descomprimí el .rar (WinRAR, 7-Zip o similar).
  2. Abrí index.html con doble clic. No necesita instalar nada ni conexión
     (la tipografía de Google Fonts es opcional: sin internet usa una de sistema).
  3. Para probar desde el celular o usar la cámara, servilo por http://localhost:
        python3 -m http.server 8080      y entrá a http://localhost:8080

Estructura
  index.html        Pantallas de la app
  css/styles.css    Diseño oscuro con un color por área
  js/app.js         Toda la lógica (datos editables al inicio del archivo)
  js/qrcode.js      Generador de QR (qrcode-generator, licencia MIT)

Qué incluye
  - Acceso: QR dinámico personal que cambia cada 30 s y es de un solo uso,
    más un molinete simulado que lo valida (cámara o pegando el código).
  - Mi rutina de hoy: evaluación inicial, plan por día, registro de pesos,
    videos de técnica y sugerencias al terminar.
  - Tienda y Protein Bar: catálogo, pedido con 10% de socio, batido para
    "cuando termine mi rutina", retiro al salir.
  - Masajes: tipo, profesional, día y horario; archivo de calendario (.ics)
    con aviso 1 hora antes y notificaciones del navegador.
  - Mi ficha: asistencias, rutinas, compras y turnos en un solo historial.

Qué cambiar para usarlo en serio
  - Los datos se guardan en el navegador (localStorage). Para varios socios
    hace falta un backend con base de datos.
  - La firma del QR (SECRET en js/app.js) es de demostración: en producción
    el servidor debe generar y validar el código en el molinete.
  - Precios, ejercicios, profesionales y horarios están al inicio de js/app.js.
