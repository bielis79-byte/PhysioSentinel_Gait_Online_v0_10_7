# PhysioSentinel Gait Online v0.10.7

## Navegación del ciclo más intuitiva

La barra de la v0.10.6 mostraba frames y el usuario tenía que deducir manualmente
qué significaba cada posición respecto a las fases de la marcha.

v0.10.7 cambia el paradigma:

### Barra maestra en segundos
La barra situada bajo el vídeo representa directamente el tiempo transcurrido
dentro del segmento analizado:
- 0.00 s = inicio del segmento;
- el extremo derecho = final del segmento;
- paso mínimo = 1 frame.

### Mapa temporal de fases
A la derecha aparece un mapa con el MISMO eje temporal en segundos.
Dos filas muestran izquierda y derecha a lo largo de todo el segmento.

Al mover la barra:
- cambia el frame del vídeo;
- se desplaza un cursor vertical en el mapa;
- se actualiza fase izquierda;
- se actualiza fase derecha;
- se actualiza el porcentaje dentro del ciclo de cada lado;
- se actualizan los cursores de la curva cinemática normalizada.

Esto elimina la necesidad de traducir mentalmente frame 161, 486, etc. a una fase.

### Navegación por eventos
Se añaden:
- Evento anterior
- Evento siguiente

para saltar directamente a IC/TO detectados.

### Entre ciclos
La pestaña deja de forzar el ciclo más cercano si el frame actual está fuera de
un ciclo válido. En esos instantes muestra `Entre ciclos`, evitando asociar una
fase incorrecta a un frame alejado.

## Conservado
- cadencia/asimetría cinemáticas v0.10.6;
- sincronización a frames reales;
- bloqueo multipersona;
- curvas normalizadas y exportación.
