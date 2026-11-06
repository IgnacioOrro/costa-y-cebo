# Costa y Cebo

Planificador de pesca recreativa desde costa para toda España: eliges un punto en el mapa, el día y la especie, y te da la mejor ventana horaria, el cebo, la marea, los periodos solunares y la talla mínima.

Es una página estática (`public/index.html`) que se publica como Worker de Cloudflare con assets estáticos.

## Publicar

```bash
npx wrangler deploy
```

O conecta el repositorio en Cloudflare (Workers & Pages → Create → Import a repository) y cada push a `main` se publica solo.

## Datos y licencias

- Constantes armónicas de marea: TICON-4 (Hart-Davis, M., Dettmering, D., Seitz, F., 2025, SEANOE, https://doi.org/10.17882/109129), vía la base de datos Neaps (https://github.com/openwatersio/tide-database). Licencia **CC BY-NC 4.0**: uso no comercial y con atribución.
- Predictor de mareas: `@neaps/tide-predictor` (MIT).
- Línea de costa: Natural Earth (dominio público), vía `world-atlas`.
- Tallas mínimas: RD 560/1995, RD 347/2011 y Reglamento (UE) 2019/1241. Orientativas; la norma autonómica puede ser distinta en aguas interiores.

Las mareas son astronómicas y orientativas. No usar para navegación.
