# ✠ Conócete — Auxiliar Católico de Temperamento y Formación del Carácter
**Estado del proyecto:** Versión Beta 1 (Fase 1)  
**URL de producción:** `https://crvxvincet-studio.github.io/Conocete/`  
**Aplicación hermana integrada:** `https://crvxvincet-studio.github.io/Conocete/Examen/`

---

## 1. Propósito de «Conócete» (Beta 1 · Fase 1)
**Conócete** es una Aplicación Web Progresiva (PWA) católica tradicional diseñada para el conocimiento del temperamento congénito y la forja del carácter cristiano mediante las virtudes, inspirada en las conferencias del **R.P. Pablo Bianchetti** ([FSSPX Colombia](https://www.youtube.com/@fsspxcolombia)) y fundamentada en las fuentes clásicas de la Cura de Almas (Santo Tomás de Aquino, René Le Senne, Gastón Berger, Mons. Tihamér Tóth y el R.P. Lorenzo Scupoli).

## 2. Arquitectura Multi-PWA del Repositorio
El repositorio aloja dos PWAs independientes pero conectadas bidireccionalmente bajo el mismo origen:

```text
/ (Raíz: Conócete · Beta 1)
├── index.html            -> Aplicación principal «Conócete»
├── manifest.json         -> Manifiesto PWA (instalable en Android, iOS y escritorio)
├── sw.js                 -> Service Worker (conocete-beta1-v1, Stale-While-Revalidate, excluye /Examen/)
├── icon-192.png          -> Icono PNG 192x192
├── icon-512.png          -> Icono PNG 512x512
├── apple-touch-icon.png  -> Icono iOS 180x180
├── icon-192.svg          -> Icono vectorial 192x192
├── icon-512.svg          -> Icono vectorial 512x512
├── README.md             -> Documentación general (Beta 1 - Fase 1)
├── LICENSE.txt           -> Dedicación al Dominio Público (CC0 1.0)
└── Examen/               -> Subdirectorio de la PWA hermana «Examen» (Beta 1 - Fase 1)
    ├── index.html        -> Aplicación «Examen» (Preparación al Sacramento de la Penitencia)
    ├── manifest.json     -> Manifiesto PWA propio de «Examen»
    ├── sw.js             -> Service Worker propio (examen-beta1-v1) con scope /Conocete/Examen/
    ├── icon-192.png      -> Icono PNG 192x192
    ├── icon-512.png      -> Icono PNG 512x512
    ├── apple-touch-icon.png -> Icono iOS 180x180
    ├── icon-192.svg      -> Icono vectorial 192x192
    ├── icon-512.svg      -> Icono vectorial 512x512
    └── README.md         -> Documentación específica de «Examen» (Beta 1 - Fase 1)
```

## 3. Comunicación Bidireccional y Privacidad Local (`localStorage`)
Toda la información vive exclusivamente en el dispositivo del usuario:
- **Clave principal (`conocete_v6_state`)**: Almacena el tema visual (`sepia`, `light`, `oled`), escala de texto (`fontScale`), respuestas del test (`answers30`), temperamento resultante (`activeProfile`, `activeProfileName`), resoluciones de la Regla de Vida (`tasks`), tests complementarios opcionales (`eduAnswers`, `acqAnswers`) y el cuaderno cifrado AES-GCM (`vault`).
- **Sincronización en vivo con `Examen`**: Ambas aplicaciones escuchan los eventos `storage`, `pageshow` y navegación por anclas (`#regla`, `#remedios`, `#resultados`) para compartir temperamento, apariencia y propósitos de enmienda sin recargas manuales.
