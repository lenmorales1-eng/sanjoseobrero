# Cómo convertir "San José Obrero" en una app instalable (APK)

Este paquete contiene la app web lista para convertirse en una app de Android.
Archivos incluidos:
- `index.html` (la app, ahora con soporte de instalación)
- `manifest.json` (nombre, ícono y colores de la app)
- `sw.js` (permite que funcione sin internet una vez instalada)
- `icon-192.png`, `icon-512.png`, `icon-512-maskable.png` (íconos de la app)

Hay dos caminos. Empieza por el Camino 1 (gratis, 10 minutos). Si necesitas
un archivo .apk de verdad para instalar en varios teléfonos o subir a Play
Store, sigue también el Camino 2.

---

## Camino 1 — Instalarla como app hoy mismo (sin generar ningún archivo)

No sirve para repartir un .apk a otras personas, pero convierte la página
en un ícono de app en el celular, con pantalla completa (sin la barra del
navegador), en minutos:

1. Sube la carpeta completa a un hosting gratis (ver Paso A del Camino 2), o
   simplemente abre `index.html` en Chrome desde el teléfono.
2. Toca el menú (⋮) de Chrome → **"Instalar app"** o **"Agregar a pantalla de inicio"**.
3. Listo — queda un ícono como cualquier otra app.

---

## Camino 2 — Generar el archivo .apk real

### Paso A: Subir los archivos a internet (necesario para el Paso B)
La forma más fácil y gratuita es GitHub Pages:

1. Crea una cuenta gratis en [github.com](https://github.com) si no tienes una.
2. Crea un repositorio nuevo (público), por ejemplo `sanjoseobrero-app`.
3. Sube estos 5 archivos a ese repositorio: `index.html`, `manifest.json`,
   `sw.js`, `icon-192.png`, `icon-512.png` (y el maskable si quieres).
4. Ve a **Settings → Pages**, en "Source" elige la rama `main` y guarda.
5. En 1-2 minutos te dará una URL como:
   `https://tu-usuario.github.io/sanjoseobrero-app/`
   Ábrela y confirma que la app carga bien ahí.

*Alternativa igual de fácil sin necesidad de cuenta técnica: [Netlify Drop](https://app.netlify.com/drop) — arrastras la carpeta y te da una URL al instante.*

### Paso B: Generar la APK con PWABuilder (gratis, de Microsoft)
1. Ve a [pwabuilder.com](https://www.pwabuilder.com)
2. Pega la URL del Paso A y presiona **Start**.
3. PWABuilder analizará la app (debería mostrar el ícono y nombre "San José Obrero").
4. Ve a la pestaña **Android** → **Generate Package**.
5. Deja las opciones por defecto (o revisa que el "Package ID" sea algo como
   `com.sanjoseobrero.app`) y descarga el paquete.
6. Descomprime el .zip que te da PWABuilder — adentro está el archivo
   **.apk** (o .aab si prefieres subirlo a Play Store).

### Paso C: Instalar la APK en un teléfono Android
1. Envía el archivo `.apk` al teléfono (por WhatsApp, correo o USB).
2. Al abrirlo, Android pedirá permiso para "instalar apps de orígenes
   desconocidos" — actívalo solo para esa instalación.
3. Instala y listo, queda como cualquier otra app en el teléfono.

---

## Notas importantes

- **No es necesario Play Store** para usar la APK — se puede instalar
  directamente como se explica en el Paso C. Si más adelante quieres
  publicarla en Play Store, PWABuilder también genera el archivo `.aab`
  que Google pide, pero eso requiere crear una cuenta de desarrollador de
  Google Play (pago único de USD $25).
- La app sigue funcionando 100% igual (memoria fotográfica + informe de
  donación); estos archivos solo le agregan la capacidad de instalarse.
- Si en el futuro cambian los datos del colectivo o el diseño, hay que
  repetir el Paso A (volver a subir los archivos) y el Paso B para generar
  una nueva APK actualizada.
