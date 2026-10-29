# ✠ Examen — Auxiliar para el Sacramento de la Penitencia
**Estado del proyecto:** Versión Beta 1 (Fase 1)  
**URL de producción:** `https://crvxvincet-studio.github.io/Conocete/Examen/`  
**Aplicación matriz conectada:** `https://crvxvincet-studio.github.io/Conocete/`

---

## 1. Propósito de «Examen» (Beta 1 · Fase 1)
**Examen** es la PWA hermana de **Conócete**, dedicada a disponer el alma para acudir dignamente al **Sacramento de la Penitencia** sin caer en escrúpulos ni en omisiones, conforme a la Teología Moral tradicional (Santo Tomás de Aquino, Catecismo Mayor de San Pío X y San Alfonso María de Ligorio).

## 2. Módulos incluidos en esta Fase 1 (Beta 1)
1. **Acto de Contrición breve en cabecera**: Visible discretamente al inicio para que el fiel lo memorice para cualquier peligro de muerte o necesidad extrema, con opción de desplegar el Acto de Contrición tradicional completo.
2. **I. Disposición**:
   - Las cinco cosas necesarias para una buena confesión.
   - Distinción moral tripartita entre **Sentir** (primer movimiento involuntario), **El Deleite voluntario o *delectación morosa*** (que debe evitarse y cortarse de inmediato porque detenerse a saborear el placer prohibido ya es consentir interiormente) y **Consentir**.
   - Reglas prudenciales para acusarse con brevedad (especie y número, sin narrar historias ni detalles a menos que muden la especie moral o que el Clérigo Confesor lo pregunte) y remedios contra los escrúpulos.
3. **II. Examen de Conciencia**: Recorrido por los Mandamientos de la Ley de Dios, los Mandamientos de la Iglesia y los Deberes de Estado.
4. **III. Mi Hoja Breve y Autodestrucción Programable**:
   - Genera una síntesis concisa (sólo especie y número aproximado de veces) pensada para transcribirse a un cuaderno de papel antes de entrar al confesionario.
   - **Autodestrucción programable (de `0` a máximo `30` días)**: Por defecto (`0 días`) vive únicamente en `sessionStorage` (`examen_v1_session`) y se borra al cerrar la pestaña; opcionalmente puede conservarse en `localStorage` (`examen_v1_state`) por `1`, `3`, `7`, `15` o máximo `30` días, además del botón de destrucción inmediata (`✠ Borrar` / `✠ Ya me confesé · Destruir hoja ahora`).
   - **Puente bidireccional hacia «Conócete»**: Permite enviar el propósito de enmienda directamente a la Regla de Vida de `Conócete` (`conocete_v6_state.tasks`).
5. **IV. Meditación**:
   - **Corona de los Siete Dolores de María Santísima** tomada de *Las Glorias de María* de **San Alfonso María de Ligorio**.
   - Recordatorio doctrinal sobre las disposiciones y el estado de gracia requeridos para recibir dignamente el **Sacramento de la Penitencia**, la **Santísima Eucaristía / Sagrada Comunión**, el **Santo Viático** y la **Extrema Unción**.
