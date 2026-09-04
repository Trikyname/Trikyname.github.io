# Marca Trikyname · assets

Sale del sistema de identidad hecho en Claude Design (`Trikyname Brand System.dc.html`, v1,
04/09). **La hoja manda; esto es su implementación.** Si los dos discrepan, gana la hoja.

## El símbolo

Una galleta mordida, con tres pepitas y tres migas. El nombre tiene dos orígenes y la marca
coge el segundo: *tricky* (difícil de resolver) y **Triki**, el monstruo de las galletas.

🔴 **El mordisco y las pepitas son agujeros de verdad** (`<mask>`), no círculos pintados del
color del fondo. En la hoja de diseño van rellenos de `#1F1610` porque allí el fondo siempre es
ése; como asset suelto eso revienta en cuanto alguien lo pone sobre blanco y sale un agujero
negro. Ya nos pasó con el wordmark de Crystalysis: **un logo no puede saber sobre qué lo van a
poner.**

Los SVG usan `currentColor`, así que una sola ruta sirve para claro y para oscuro.

## Los ficheros

| Fichero | Para qué |
|---|---|
| `trikyname-mark.svg` | El símbolo. Para **≥48 px**. Con migas. |
| `trikyname-mark-small.svg` | Para **≤32 px**: pepitas engordadas y sin migas. Ver abajo. |
| `trikyname-mark-1024.png` | Crema, transparente. Formularios, prensa, festivales. |
| `trikyname-mark-dark-1024.png` | Cacao, transparente. Sobre fondo claro y en papel. |
| `trikyname-icon-512.png` | Icono de desarrollador (Play, IGF, Steam). |
| `trikyname-avatar-400.png` | Avatar de redes. Cuadrado; X lo recorta a círculo solo. |
| `trikyname-favicon-64.png` | Favicon. |
| `trikyname-header-1500x500.png` | Cabecera de X. **Pareja del avatar** — ver abajo. |
| `trikyname-header-1500x500-alpha.png` | La misma con alfa, para cuando el fondo lo ponga otro. |
| `trikyname-splash-1920x1080.png` | Pantalla de arranque de los juegos. |

⚠ **La versión pequeña no es la grande reducida.** Las pepitas pasan de r5 a r9 y las migas se
van. A 16 px las pepitas del tamaño grande se cierran solas y la galleta queda como un círculo
liso; engordándolas siguen leyéndose. Las migas a ese tamaño son suciedad, no migas.

## El avatar y la cabecera son UNA pieza en dos ficheros

Se ven juntos —X superpone el avatar sobre la esquina inferior izquierda de la cabecera—, así que
repetir el símbolo a dos tamaños queda pobre. **Se complementan en vez de repetirse:**

- El **avatar** es la galleta con el mordisco. Es la única pieza **con fondo pintado**: X lo
  recorta a círculo y el Cacao de dentro hace de plato.
- La **cabecera** es lo que pasa **fuera** del mordisco: un solo arco de migas que nace abajo a la
  izquierda —justo donde el avatar la tapa— y crece hasta la pepita verde pegada al wordmark.
  Arriba a la derecha, una línea de estado: qué hay publicado y qué viene.

⚠ **La esquina inferior izquierda de la cabecera va vacía a propósito.** Es la que tapa el avatar.

🔴 **La cabecera se sube CON FONDO PINTADO aunque el diseño la define transparente**, y no es un
descuido: X reencoda las cabeceras y el alfa se pierde. Sobre tema claro, crema sobre blanco es
una cabecera en blanco. Pintada se ve idéntica sobre el tema oscuro, que es para el que está
pensada. La versión con alfa está ahí para todo lo demás.

🔵 **Y el avatar ocupa el 79,5 % del lienzo, no el 68 %.** Ese 68 salió de un cálculo correcto
para otro caso: un símbolo suelto sobre un cuadrado, donde las esquinas de su caja se salen del
recorte circular. Aquí el fondo **es** el plato, así que lo único que tiene que caber dentro del
círculo son las **migas**, y las tres caen holgadas.

## Reglas mínimas

- **Margen:** ¼ del diámetro de la galleta.
- **Tamaño mínimo:** 16 px, y ahí ya sin migas.
- **Nunca** en cursiva, y el nombre **siempre en minúsculas**: `trikyname`.

## Color y tipografía

| | |
|---|---|
| Noche `#0F0B08` | fondo |
| Cacao `#1F1610` | tarjetas, pepitas |
| Masa `#F7EFE2` | galleta, texto |
| Pepita `oklch(.8 .15 140)` | acento: enlaces, botones, la miga de la animación |
| Horno `oklch(.8 .15 40)` | segundo acento: avisos |

**Fredoka 600** para el wordmark y los titulares. **Nunito 400/600** para el texto.
El humor lo pone el símbolo, no la letra.

🔴 **Y esto NO es la paleta de Crystalysis, a propósito.** El juego es cian frío sobre negro
azulado; el estudio es crema sobre marrón cálido. Un estudio vestido de su único juego miente el
día que saque uno distinto.

## Cómo se regeneran

Los PNG salen de los SVG con Chrome headless; no se editan a mano. Si cambia el símbolo, se
cambia el SVG y se vuelven a generar todos, que es lo que impide que se desincronicen.
