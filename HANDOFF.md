# HANDOFF · Menger Studio (web)

Última actualización: 31-10-2026 · Equipo: gargamel

## Estado actual
- **Web pública (en pruebas):** https://mengerspong3.github.io/menger-studio/ (este repo, GitHub Pages desde `main` /). Verificada en móvil (375 px) y escritorio (1280 px), 7 idiomas, sin scroll lateral.
  - 4 juegos con carátula, vídeo corto de gameplay, «Pruébalo» con QR y opinión con caritas. Sin créditos ni licencias, sin enlaces a repos privados, sin publicidad ni cookies. Aviso «BETA» arriba.
  - FractalBlast jugable en `play/fractalblast/` (export web de Godot 4.7.2, sin hilos). Probado: arranca en móvil.
  - Descargas: Rodamons Linux y APK de Narthex desde la release de `mengerspong3/menger-studio-builds`.
- **Intranet:** Artifact privado https://claude.ai/artifact/R18NU6JsZhyoj2GF2ViqBc (estado, créditos, buzón propio). Su código ya no está en el repo público de builds (commit 07ec537; sigue en el historial de 4c634db). Código en el repo privado `mengerspong3/menger-studio-intranet` (clonar en `~/Projects/Jocs/MengerStudio/web/`). Enlaza a la web pública; la pública no enlaza a la intranet.

## Último trabajo hecho
- Intranet subida a `menger-studio-intranet` y con enlace «Web pública» en la barra y el pie.
- Vídeos (en `video/`, MP4 sin sonido):
  - Rodamons: build Linux con `-rd-players 1` y `-rd-players 4` (la IA conduce), grabado con `ffmpeg -f x11grab`.
  - FractalBlast y MathDungeon: Godot `--write-movie` con los scripts de `tools/grabar/` (conducen la nave / juegan solos).
  - Narthex: pasillo del prototipo web (`tools/grabar/narthex_pasillo.html`, usa `ascii.js` y `corridor.js` de fosforo) en Firefox kiosk + x11grab. No es la AR real.
- Plantillas de exportación web de Godot 4.7.2 instaladas en `~/.local/share/godot/export_templates/4.7.2.stable/` (solo las web).

## Pendiente / siguiente paso
(Formulario activo: FormSubmit con alias `2fc831a756eb0a747ed2f9cf4f4f800a`, llega al correo de formularios de Luis.)
1. FractalBlast web muestra el botón «DBG» del panel de depuración; habría que ocultarlo en exportaciones release (cambio en el repo de FractalBlast).
2. Vídeo de Narthex con la AR real: grabar la pantalla del Pixel 9a (`adb shell screenrecord`) y sustituir `video/narthex.mp4`.
3. Builds de Windows (Rodamons) y web de MathDungeon para quitar «Próximamente».

## Dudas abiertas
- Los sprites de MathDungeon sin origen claro (Enemy_Animations_Set, RPG_Hero) salen en el vídeo: Luis dijo incluirlo igual.
