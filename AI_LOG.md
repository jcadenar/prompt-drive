# Registro de uso de IA

**Asistentes usados**

Se usó Claude Opus 5.5 y Claude Code (modelo Claude Opus 5.5) dentro de VS Code, en primer lugar para entender la estructura del proyecto y cómo funcionaba, después para ubicar qué archivos debía y podía modificar y cuáles no. Elegí dos features y el asistente de IA se encargó de implementarlas, mientras yo testeaba lo que hacía, depuraba con capturas y le indicaba cambios a realizar. 

**Tres prompts que me sirvieron** (pégalos o resúmelos, y di qué salió de cada uno):

1. "Pregunta. Los graficos solo pueden tener posicion fija? es que por ejemplo el simulador permite mover el lado del piloto de derecha a izquierda y alejar o acercar la camara, entonces los gráficos ya no coinciden.": Este prompt me permitió entender la diferencia entre una capa 2D y 3D, y por qué con la 2D todo desencajaba al cambiar la posición de la cámara. Esto permitió darle otro enfoque a la solución. 

2. "El problema persiste y es que el empañado invade la pantalla central como se ve en la imagen": Sirvió para corregir el tema del vidrio empañado y que no se interpusiera con la vista de la pantalla central del carro. El resultado fue una capa más limpia y definida, acorde al modelo 3D del carro y que no interfería con la visión de la pantalla central. 

3. "Por favor. Revisa el repo, el read.me y trae basicamente todas las intrucciones y como funciona el simulador": Este prompt me permitió entender cómo funcionaba a nivel interno el simulador, y ver en términos generales cómo y dónde modificar el repositorio y cómo se debía realizar la entrega. 

**Uno que me engañó** 

"El empañado invade la pantalla central.": Con este prompt el asistente me dio una copia invisible de la pantalla que solo escribía profundidad, y me confirmó que estaba arreglado, cosa que no era cierta, pues yo al probarlo pude ver que el error persistía. Estaba mal porque, en el modelo, la pantalla atraviesa el parabrisas, así que el empañamiento quedaba delante. Lo pude detectar con mi propia captura. 

**Porcentaje aproximado del texto final del system prompt que escribió la IA sin cambios:**

En este reto no escribí un system prompt, así que lo respondo para lo que entregué:

- **Código** (`src/feedback/features/defrost.js` y `ambient_light.js`): cerca del 100 % lo escribió la IA. Yo no edité el código a mano; mi trabajo fue probar cada versión en el simulador, mandar capturas y pedir cambios (opacidad del empañamiento, tiempo de despeje, brillo de la luz, pasar de 2D a 3D).
- **Notas de diseño** (`docs/feedback/defrost.md` y `ambient_light.md`): alrededor del 60 %. Las secciones 1 a 3 (lo que viví en el estudio, lo que debe percibir quien maneja y las alternativas) las escribí yo; las secciones 4 a 6 las redactó parcialmente la IA a partir de lo que hicimos, y yo las revisé, quité partes y cambié términos.
- **Reflexión y este registro:** 0 %, los escribí yo.

