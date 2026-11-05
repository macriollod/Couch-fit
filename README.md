# Couch Fit 🏋️

App de fitness personal: elige el grupo muscular, mira qué equipo necesitas y sigue un plan semanal pensado para tus objetivos. Sin anuncios, sin cuentas, sin internet: todo corre en el celular.

## ¿Qué hace?

- **Mapa de ejercicios por músculo**: elige el grupo muscular que quieres trabajar y la app te muestra ejercicios para ese grupo.
- **Filtro por equipo disponible**: marca si entrenas con peso corporal, mancuernas, barra, banda, cuerda de saltar, barra de dominadas, etc., y la app ajusta lo que te sugiere.
- **Rutinas**: arma y guarda tus propias rutinas combinando los ejercicios que elijas.
- **Plan semanal**: define cuántos días entrenas y qué objetivo buscas (fuerza, resistencia, pérdida de grasa, tonificación), y la app organiza una planificación semanal con alternativas editables.
- **Acerca de mí**: tu espacio para anotar metas personales y ver tu progreso.

Todo el contenido (ejercicios, textos, estructura) es original, pensado para evitar depender de apps de terceros y su publicidad.

## Diseño

- Paleta de colores: naranja, blanco hueso y café suave.
- Tipografías: Nunito y Outfit (via @fontsource), buscando una letra cuidada pero legible.
- Pensada mobile-first para usarse como app instalada en Android.

## Tecnología

- Interfaz en HTML, CSS y JavaScript puro (`www/index.html`), sin frameworks.
- Empaquetada como app Android nativa con [Capacitor](https://capacitorjs.com/) (`@capacitor/core`, `@capacitor/android`).
- El APK se genera automáticamente con GitHub Actions (ver `.github/workflows`), sin necesidad de instalar Android Studio en tu computador.
- Los datos del usuario (perfil, metas, rutinas, plan semanal) se guardan localmente en el propio celular; la app no usa servidores ni cuentas.

## Cómo obtener el APK

1. Entra a la pestaña **Actions** de este repositorio.
2. Abre el workflow **Construir APK de Couch Fit** y toca **Run workflow**.
3. Espera entre 5 y 10 minutos a que aparezca la marca verde ✅.
4. Abre esa ejecución, baja hasta **Artifacts** y descarga **CouchFit-apk** (contiene `app-debug.apk`).
5. Pasa el APK a tu celular, ábrelo e instálalo (Android pedirá permitir "instalar apps desconocidas" para esa fuente).

Más detalle paso a paso en [`LEEME.md`](./LEEME.md).

> **Nota:** es un APK de depuración (debug), pensado para instalar y usar en tu propio celular. No está firmado para publicarse en Google Play.

## Estado del proyecto

- [x] Pantalla de inicio, mapa de ejercicios y equipo disponible
- [x] Sección Rutinas
- [x] Plan semanal con alternativas editables
- [x] Sección "Acerca de mí"
- [ ] Pulir y ampliar la sección Rutinas
- [ ] Revisar si vuelve a agregarse una pestaña de Historial

## Estructura del repositorio

```
Couch-fit/
├── www/index.html        # Toda la app (HTML + CSS + JS)
├── icons/                 # Íconos de la app
├── capacitor.config.json  # Configuración de Capacitor
├── package.json           # Dependencias (Capacitor, fuentes)
├── .github/workflows/     # Workflow que construye el APK
└── LEEME.md               # Guía para generar el APK paso a paso
```

---

Proyecto personal de fitness, hecho a medida y sin publicidad.
