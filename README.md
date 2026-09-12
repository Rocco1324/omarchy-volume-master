# Volume master in Omarchy

Widget de barra para Omarchy con controles de audio completos y volumen maestro ampliado hasta 150%.

## Caracteristicas

### Volumen maestro ampliado
- Rango de volumen de salida de 0% a 150%
- Muestra el porcentaje base y el boost por encima de 100% en formato `N% (+X% )`
- Nombres descriptivos del volumen: Whisper, Murmur, Easy listening, Steady groove, Party mode, Concert hall
- Slider con paso de 5% y ajuste con rueda del mouse
- OSD (On-Screen Display) al cambiar volumen

### Control de dispositivos
- Selector de dispositivos de salida (sinks) con iconos contextuales
- Selector de dispositivos de entrada (sources) con medidor de pico
- Deteccion automatica de: parlantes, auriculares, bluetooth, HDMI
- Resolucion de sinks DSP (tunings/EasyEffects) para ajustar el volumen en el dispositivo fisico correcto
- Disponibilidad de sinks con refresco periodico

### Mezclador por aplicacion
- Lista de streams de reproduccion por aplicacion
- Slider individual por app (0% a 150%)
- Mute individual por aplicacion
- Integracion con MPRIS para nombres amigables (ej: Spotify)
- Deteccion de reproductor activo

### Navegacion por teclado
- `j`/`k` - mover cursor entre secciones y filas
- `h`/`l` - bajar/subir volumen en el slider enfocado
- `m` - mutear/seccion o stream seleccionado
- `Enter`/`Space` - activar opcion bajo el cursor
- `Tab` - cambiar entre paneles
- Click derecho en icono - mute global
- Rueda del mouse sobre icono - ajustar volumen

### Interfaz
- Icono dinamico en la barra segun estado (mute, volumen bajo/medio/alto, auriculares)
- Boton de texto con porcentaje en la barra
- Panel desplegable con:
  - Hero section con icono, titulo "Audio", nombre del volumen y switch de mute global
  - Seccion OUTPUT con slider y lista de dispositivos
  - Seccion INPUT con slider y lista de dispositivos
  - Seccion SOURCES con streams por aplicacion
- Tooltips informativos
- Scroll automatico para mantener el cursor visible

### Integracion
- PipeWire para control de audio
- MPRIS para detectar reproductores multimedia
- Servicio omarchy.media para reproductor activo
- OSD nativo de Omarchy
- Compatible con sistemas de audio DSP

## Instalacion

```bash
omarchy plugin add <public-git-repository-url> --enable
```

El plugin usa el dispositivo de salida seleccionado por Omarchy y no requiere privilegios elevados.
