# Webapp estática para Vercel

Este proyecto ahora funciona como una webapp estática basada en los HTML originales.

## Rutas

- `/` portada de la app
- `/bogota` informe de Bogotá
- `/lima` informe de Lima

## Vista local

Puedes levantarlo con un servidor estático simple desde la raíz del proyecto:

```bash
python3 -m http.server 8000
```

Luego abre:

- `http://localhost:8000/`
- `http://localhost:8000/bogota.html`
- `http://localhost:8000/lima.html`

## Despliegue en Vercel

La configuración está en `vercel.json` y usa `cleanUrls` para exponer las rutas `/bogota` y `/lima`, además de redirigir automáticamente las URLs largas antiguas.

## Publicarlo ahora

Opción recomendada:

1. Sube esta carpeta a un repositorio de GitHub.
2. En Vercel, crea un proyecto nuevo e importa ese repositorio.
3. Deja la detección de framework en `Other` o sin framework si Vercel no detecta nada.
4. No pongas `Build Command`.
5. No pongas `Output Directory`.
6. Despliega.

La home quedará en `/` y los alias limpios funcionarán como `/bogota` y `/lima`.
