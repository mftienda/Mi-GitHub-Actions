# Práctica 3: desplegar manualmente una aplicación web

[Volver al menú de prácticas](README.md)

Imagina que ya tienes publicada la versión 1.0 de una web y estás preparando la 1.1. Quieres subir los cambios al repositorio, revisarlos y elegir cuándo estarán disponibles para los usuarios.

En esta práctica usamos un **despliegue manual**. Tú decides cuándo lanzar la publicación y GitHub Actions se encarga de ejecutarla.

## Pasos de la práctica

1. **Partimos de una web que ya funciona.** Usamos el repositorio de la aplicación y publicamos una versión inicial. Para una web estática podemos usar GitHub Pages y seleccionar **GitHub Actions** como fuente de publicación.
2. **Preparamos un workflow de publicación manual.** En el archivo YAML usamos `workflow_dispatch` para habilitar el botón **Run workflow**. El flujo comprueba que el proyecto se pueda preparar y publica la web si la comprobación pasa.
3. **Subimos un cambio visible.** Por ejemplo, cambiamos el número de versión que se muestra en la portada de «1.0» a «1.1» y subimos el cambio a `main`. Visitamos la web pública y comprobamos que todavía muestra la versión 1.0.
4. **Publicamos cuando estemos listos.** En **Actions**, seleccionamos el workflow de publicación, pulsamos **Run workflow** y elegimos `main`. Cuando la ejecución termine en verde, recargamos la web y comprobamos que ahora muestra la versión 1.1.

Si la aplicación ya tiene un flujo que publica con cada cambio en `main`, realiza la práctica en una copia para poder observar la espera entre subir el cambio y decidir publicarlo.
