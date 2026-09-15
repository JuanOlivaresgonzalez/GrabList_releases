# DJAssist Grabber

Plugin de [Nicotine+](https://nicotine-plus.org) con una interfaz web para
buscar y descargar los tracks de una playlist desde Soulseek. Vos elegís qué
bajar de cada track — nada se descarga solo.

> **¿No sos técnico?** Abrí **[LEEME.txt](LEEME.txt)**: guía completa, paso a
> paso, de instalación y uso (también queda una copia en
> `Música/DJAssist Grabber/` después de instalar).

## Instalación

**No hace falta usar la Terminal.**

1. Descargá este proyecto (botón verde "Code" → "Download ZIP" en GitHub) y
   descomprimilo
2. Hacé doble click en:
   - **Mac**: `Instalar.command`
   - **Windows**: `Instalar.bat`
3. Seguí las instrucciones en pantalla (si no tenés Python o Nicotine+
   instalados, el instalador te lleva a la página oficial para bajarlos)
4. Abrí Nicotine+ → Preferencias → Plugins → activá **DJAssist Grabber**
5. Abrí [http://127.0.0.1:8765](http://127.0.0.1:8765) en el navegador

Requiere Python 3 instalado en tu compu (el instalador te avisa y te manda a
bajarlo si no lo tenés).

## Qué hace

- Importa playlists en `.txt`, `.csv`, `.m3u`, XML de Rekordbox, o directo
  desde una captura de pantalla (OCR, instalable desde la propia web la
  primera vez que subís una imagen)
- Busca en Soulseek con hasta 4 búsquedas en simultáneo (ajustable)
- Te muestra los candidatos encontrados — vos elegís cuál bajar
- Si no aparece nada en Soulseek, te arma la búsqueda en Bandcamp y
  SoundCloud

## Para desarrollo

Ver [ROADMAP.md](ROADMAP.md). El código del plugin vive en
`plugin/djassist_grabber/`; `tools/sync_plugin.py` lo copia a la carpeta
real de Nicotine+ después de cada cambio.

**Para mandárselo a alguien** (sin acceso al repo):
`python tools/build_zip.py --version 1.1` sube la versión en
`plugin/djassist_grabber/PLUGININFO` y arma `dist/DJAssist-Grabber-v1.1.zip`
con solo lo necesario (LEEME, instaladores y plugin), con los finales de línea
y permisos correctos para Windows y Mac. Sin `--version` usa la versión
actual; no pisa un zip que ya existe con esa versión (salvo `--force`).
Commiteá `PLUGININFO` después de subir la versión.

**Publicar la versión** (para que a todos les aparezca el aviso de
actualización): en
[djassist-grabber-releases](https://github.com/JuanOlivaresgonzalez/djassist-grabber-releases/releases/new)
(repo **público**, solo con los zips) creá una Release con tag `v1.1`,
adjuntá el zip y escribí qué cambió. El plugin consulta la última Release de
ese repo una vez al día y con el botón "Buscar actualizaciones"
(`plugin/djassist_grabber/updates.py`; si el repo se llama distinto, cambiá
`RELEASES_REPO` ahí).
