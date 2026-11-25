# Despliegue continuo automático

[Volver al menú de prácticas](README.md)

## Despliegue manual y despliegue continuo

**Desplegar** es publicar una versión de una aplicación o de una web para que sus usuarios puedan acceder a ella. Con GitHub Actions podemos preparar un workflow que se encargue de publicarla.

- **Despliegue manual.** Una persona decide cuándo publicar. Por ejemplo, puede iniciar el workflow de publicación con el botón **Run workflow**. GitHub Actions ejecuta los pasos a partir de ese momento.
- **Despliegue continuo.** Cada cambio que llega a la rama principal y supera las comprobaciones se publica automáticamente. Por ejemplo, un workflow puede arrancar al recibir un cambio en `main` y publicar la web si las comprobaciones pasan.

### Práctica: publicar automáticamente la web de mi perfil

1. **Partimos del repositorio de perfil.** Usamos `mftienda/mftienda`, que ya contiene el `README.md` en la raíz de la rama `main`. Ese archivo será la portada de la web.
2. **Publicamos la primera versión.** En **Settings → Pages → Source**, elegimos **Deploy from a branch**, seleccionamos `main` y `/ (root)` y pulsamos **Save**. Cuando termina la primera publicación, abrimos la web. [Ver la web del perfil](https://mftienda.github.io/mftienda/)
3. **Comprobamos el despliegue automático.** Hacemos un cambio visible en `README.md`, guardamos el cambio en un commit y lo subimos a `main`. GitHub Pages inicia la publicación por su cuenta. En **Actions**, esperamos a que **pages build and deployment** termine en verde. Después recargamos la web y comprobamos que aparece el cambio.
