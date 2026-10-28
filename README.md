# ✠ Conócete y Examen · Repositorio Multi-PWA Católico Tradicional

Este paquete contiene las dos aplicaciones web progresivas (PWA) hermanas, listas para desplegarse directamente en el repositorio de GitHub Pages:

- **`https://crvxvincet-studio.github.io/Conocete/`** (raíz del repositorio)
- **`https://crvxvincet-studio.github.io/Conocete/Examen/`** (subdirectorio `/Examen/`)

## Estructura de archivos del paquete

```text
/ (Raíz del repositorio Conocete)
├── index.html          -> PWA principal «Conócete» (Espejo del Alma, Test de 30 o 12 preguntas intacto, Test complementarios de Educación y Hábitos, Detector de Defecto Dominante y Las 7 Categorías de Vicios × 8 Temperamentos)
├── manifest.json       -> Manifiesto PWA de «Conócete»
├── sw.js               -> Service Worker offline de «Conócete»
├── icon-192.svg        -> Icono vectorial 192x192 de «Conócete»
├── icon-512.svg        -> Icono vectorial 512x512 de «Conócete»
├── README.md           -> Guía de despliegue y arquitectura
├── LICENSE.txt         -> Licencia CC0 1.0 Universal (Dominio Público)
└── Examen/             -> Subdirectorio para la PWA hermana «Examen»
    ├── index.html      -> PWA «Examen» (Acto de contrición breve en cabecera, Preparación al Sacramento de la Penitencia, Distinción entre Sentir, el Deleite voluntario y Consentir, Hoja Breve para pasar al cuaderno con autodestrucción programable de 0 a 30 días, y Corona de los Siete Dolores de María Santísima por San Alfonso María de Ligorio)
    ├── manifest.json   -> Manifiesto PWA independiente para instalar «Examen»
    ├── sw.js           -> Service Worker offline de «Examen»
    ├── icon-192.svg    -> Icono vectorial 192x192 de «Examen»
    └── icon-512.svg    -> Icono vectorial 512x512 de «Examen»
```

## Conexión automática entre ambas aplicaciones

Al vivir bajo el mismo dominio (`crvxvincet-studio.github.io`), ambas aplicaciones comparten de forma local y 100 % privada en el dispositivo del usuario:
1. El tema visual (`Pergamino`, `Marfil` o `Nocturno OLED`) y el tamaño de lectura.
2. El temperamento diagnosticado en **«Conócete»**, para ofrecer advertencias personalizadas al iniciar **«Examen»**.
3. El envío directo del propósito de enmienda desde **«Examen»** hacia la Ficha Personal de **«Conócete»**.
