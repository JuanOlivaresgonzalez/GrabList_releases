# GrabList

Plugin de [Nicotine+](https://nicotine-plus.org) con una interfaz web para
buscar y descargar los tracks de una playlist desde Soulseek. Vos elegís qué
bajar de cada track — nada se descarga solo.

> ### 📖 [Ver el tutorial visual, paso a paso](https://juanolivaresgonzalez.github.io/djassist-grabber-releases/)
> La forma más fácil de arrancar si no sos técnico: instalación y primeros
> pasos, con capturas, sin salir del navegador.
>
> ¿Preferís texto? Abrí **[LEEME.txt](LEEME.txt)**: la misma guía completa,
> paso a paso (también queda una copia en `Música/DJAssist Grabber/`
> después de instalar).

## Instalación

**No hace falta usar la Terminal.**

1. Descargá este proyecto (desde releases en la columna de la derecha de la pagina) y
   descomprimilo
2. Hacé doble click en:
   - **Mac**: `Instalar.command`
   - **Windows**: `Instalar.bat`
3. Seguí las instrucciones en pantalla (si no tenés Python o Nicotine+
   instalados, el instalador te lleva a la página oficial para bajarlos)
4. Abrí Nicotine+ → Preferencias → Plugins → activá **GrabList**
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
