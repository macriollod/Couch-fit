# Couch Fit: cómo obtener tu APK

No necesitas instalar nada en tu computador. GitHub construye el APK por ti, gratis.

1. Crea una cuenta en https://github.com (si no tienes).
2. Crea un repositorio nuevo, privado, con el nombre `couch-fit`.
3. En el repositorio, toca "uploading an existing file" y sube TODO el contenido de esta carpeta
   (incluida la carpeta oculta `.github`; si tu navegador no la deja subir, arrastra la carpeta completa
   o usa GitHub Desktop).
4. Ve a la pestaña **Actions**. Si pide activar los workflows, acepta.
5. Entra a "Construir APK de Couch Fit" y toca **Run workflow**. Tarda unos 5 a 10 minutos.
6. Cuando termine (marca verde), abre la ejecución y baja el archivo **CouchFit-apk** (un zip con `app-debug.apk`).
7. Pasa el APK al celular y ábrelo. Android pedirá permitir "instalar apps desconocidas" para el navegador o el
   gestor de archivos que uses.

Notas
- Es un APK de prueba (debug): sirve para instalar y usar en tu celular, pero no para subir a Play Store.
- Tus datos (perfil, plan, rutinas) se guardan dentro de la app, en el celular.
- Para cambiar la app edita `www/index.html` y vuelve a ejecutar el workflow.
