# Trikyname.github.io

La página de desarrollador de **Álvaro Colom (Trikyname)**, servida en
<https://trikyname.github.io>.

## Por qué este repo importa más de lo que parece

Es la **user page**, o sea la que posee la RAÍZ del dominio `trikyname.github.io`.
De eso dependen dos cosas que no se pueden mover a otro repo:

- **`app-ads.txt`** — AdMob coge el campo *Website* de la ficha de Play y crawlea
  `<dominio>/app-ads.txt`, **ignorando la ruta**. Sólo la user page puede servir ese fichero
  en la raíz; desde una project page (`/crystalysis-site/`) es imposible.
  ⚠ **No lo muevas, no lo renombres y no lo envuelvas en HTML.**
- **El campo *Website* de Play**, que apunta aquí y es público: quien lo pulse aterriza en
  esta página.

## Qué NO vive aquí

El sitio del juego, que es otro repo: [`crystalysis-site`](https://github.com/Trikyname/crystalysis-site)
(landing, press kit, política de privacidad y borrado de datos). Las URLs de privacidad y de
borrado están **registradas en Play Console y en Data Safety**, así que no se tocan.

## Nota de diseño

Esta página **no usa la paleta de Crystalysis** a propósito: el estudio no se viste del juego,
o el día que haya un segundo juego distinto el sitio miente. El único color de la página es el
key art del propio juego. El hueco de la marca está reservado y vacío hasta que exista.
