# Webs para negocios

Catálogo con las **6 demos** de webs para negocios: cada ficha tiene su captura, su demo en vivo y su repositorio.

**Catálogo publicado:** https://avilacarlosdev.github.io/webs-para-negocios/

| Demo | Rubro | En vivo | Repositorio |
|---|---|---|---|
| CraveNow | Delivery | [agencia-web-delivery-demo.vercel.app](https://agencia-web-delivery-demo.vercel.app) | [web-delivery-demo](https://github.com/AvilaCarlosDev/web-delivery-demo) |
| Noble Barber | Barbería | [agencia-web-barberia-demo.vercel.app](https://agencia-web-barberia-demo.vercel.app) | [web-barberia-demo](https://github.com/AvilaCarlosDev/web-barberia-demo) |
| RutaFija | Taxi | [agencia-web-taxi-demo.vercel.app](https://agencia-web-taxi-demo.vercel.app) | [web-taxi-demo](https://github.com/AvilaCarlosDev/web-taxi-demo) |
| Siena Flower | Floristería | [agencia-web-floristeria-demo.vercel.app](https://agencia-web-floristeria-demo.vercel.app) | [web-floristeria-demo](https://github.com/AvilaCarlosDev/web-floristeria-demo) |
| ObraMax | Ferretería | [agencia-web-ferreteria-demo.vercel.app](https://agencia-web-ferreteria-demo.vercel.app) | [web-ferreteria-demo](https://github.com/AvilaCarlosDev/web-ferreteria-demo) |
| SportZone | Deportes | [agencia-web-deportes-demo.vercel.app](https://agencia-web-deportes-demo.vercel.app) | [web-deportes-demo](https://github.com/AvilaCarlosDev/web-deportes-demo) |

## Cómo está hecho

- Página estática de un solo archivo (`index.html`), sin dependencias ni build.
- Las capturas (`assets/*.jpg`, 1280×720) se copian de `docs/portada.jpg` de cada repositorio; si una demo cambia, se vuelve a copiar.
- Revelado de fichas con `IntersectionObserver`, con `prefers-reduced-motion` respetado.

## Actualizar capturas

```bash
for d in delivery barberia taxi floristeria ferreteria deportes; do
  magick ../web-$d-demo/docs/portada.jpg -resize 1280x720 -quality 82 assets/$d.jpg
done
```
