# Reflexión (300 a 500 palabras)

**Equipo:** Julian Esteban Cadena Rojas (COH2)  
**Integrantes:** Julian Esteban Cadena Rojas
**Features entregadas (ids):** defrost, ambient_light
**Enlace al pull request:** https://github.com/ignacioalvmar/prompt-drive/pull/24

## Qué quería lograr

La acción más muda del estudio para mí fue el vidrio empañado: nunca vi que el asistente activara el desempañador ni encontré un testigo que me confirmara que estaba encendido. Se me complicó mucho que el asistente me entendiera, y dentro del carro no vi nada que me indicara si estaba pasando algo. Quería implementar estas features de una manera mucho más visual y clara, para evitar dudas o confusiones.

## Qué diseñé y qué pasó

Me centré en que los efectos fueran evidentes, por eso escogí dos features que se pueden ver dentro de la simulación. En el desempañador fue importante añadir sonido, porque así quien maneja sabe que está funcionando sin necesidad de mirar el testigo. También busqué realismo, por ejemplo que el vidrio se desempañara de abajo hacia arriba, de forma gradual, y no que simplemente tuviera dos estados, empañado y desempañado. En la luz ambiental quería no deslumbrar al conductor y que fuera elegante, como los autos actuales que usan una línea que atraviesa el tablero, cosa que me pareció más sutil y cercana a la realidad. Después de verla funcionando, cambié la luz ambiental: al inicio iluminaba buena parte del habitáculo, pero resultó invasiva y terminé implementando la línea LED que quedó al final.

## Dónde la IA me ayudó y dónde me engañó

La IA me ayudó sobre todo con el problema de las capas 2D. No sabía que tenían coordenadas fijas y que, como el simulador permite cambiar de cámara y de lado del conductor, terminaban descolocadas. La IA me ayudó a entender que, con una capa 3D, que hiciera parte del modelo del auto, se podía cambiar la vista sin que el empañamiento y la luz ambiental se movieran de su lugar.

Me engañó cuando le pedí que el vidrio empañado no tapara la pantalla central; me afirmó haber solucionado el problema, pero al probarlo vi que seguía prácticamente igual. Lo resolví adjuntando una captura y escribiendo un prompt más específico. Con eso la IA entendió el problema y dio una solución eficaz.

## Qué haría con un segundo día

Refinaría las features: que también se empañaran las ventanas del conductor y de los pasajeros, y que la luz ambiental atravesara, además del tablero, todas las puertas del carro, como en la vida real. Por tiempo no alcancé a implementarlo.

## Qué aprendí sobre la retroalimentación en el carro, o sobre cómo trabajo yo

Aprendí que el feedback que da un carro debe transmitir la información de la forma más clara, rápida y simple posible, porque el conductor tiene que estar atento a la vía. La simpleza depende del tipo de función: en una función de seguridad como el desempañador hay que dejar claro cuándo está funcionando, con señales visuales y audibles.

Sobre cómo trabajo, aprendí que hay que ser muy específico con la IA y darle un margen de trabajo bien definido para evitar que alucine. También hay que revisar qué está implementando exactamente y comprobar por uno mismo que funcione, en vez de confiar en que ya está resuelto.
