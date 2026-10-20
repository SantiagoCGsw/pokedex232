# Pokédex de Kanto (PWA)

Aplicación web progresiva (PWA) para consultar los 150 Pokémon de Kanto: busca, filtra por tipo y marca los que has visto y capturado. Se puede instalar en el celular como una app.

## 🔗 Demo en línea

**https://pokedex243.netlify.app/**

> La primera vez puede tardar hasta un minuto en cargar: el backend corre en un plan gratuito que se duerme tras unos minutos sin uso y tarda en despertar.

## ✨ Funciones

- Lista de los 150 Pokémon con su imagen y tipos.
- Búsqueda por nombre o número.
- Filtro por tipo y pestañas **Todos / Vistos / Capturados**.
- Ficha de detalle: artwork, descripción, altura, peso, habilidades, estadísticas base y evoluciones.
- En el celular, desliza el dedo a la izquierda o a la derecha para pasar al siguiente o al anterior.
- Tema claro y oscuro automático.
- Instalable y con caché para funcionar con mala conexión.
- Los vistos y capturados se guardan en el dispositivo (`localStorage`).

## 📱 Instalar en el celular

**Android (Chrome)**
1. Abre https://pokedex243.netlify.app/
2. Menú (⋮) → **Instalar app** o **Agregar a la pantalla principal**.

**iPhone / iPad (Safari)**
1. Abre https://pokedex243.netlify.app/ en **Safari**.
2. Toca **Compartir** → **Agregar a pantalla de inicio**.

## 🧩 Tecnologías

- HTML, CSS y JavaScript puro (sin frameworks ni build).
- Service Worker y Web App Manifest para la funcionalidad PWA.
- Backend REST: [pokedex-backend](https://github.com/RickyFreefly/pokedex-backend)
  - API: `https://pokedex-backend-g1ql.onrender.com`
  - Documentación (Swagger): `https://pokedex-backend-g1ql.onrender.com/docs`

## 📁 Estructura

```
├── index.html              # App completa (HTML, CSS y JS)
├── sw.js                   # Service worker (caché)
├── manifest.webmanifest    # Configuración de la PWA
├── icon-192.png
├── icon-512.png
├── apple-touch-icon.png    # Icono para iOS
└── LEEME.txt
```

## 🚀 Ejecutar en local

Las PWA necesitan HTTP/HTTPS, así que no abras `index.html` con doble clic. Desde la carpeta del proyecto:

```bash
npx serve .
# o
python -m http.server 8000
```

Luego abre `http://localhost:8000`.

## 🌐 Despliegue

El sitio está publicado en Netlify. Para actualizarlo, sube los cambios al repositorio o arrastra de nuevo la carpeta a [Netlify Drop](https://app.netlify.com/drop).

Cada vez que cambies archivos, sube el número de versión `V` en `sw.js` para que los dispositivos actualicen la caché.

## 👤 Autor

Santiago C. — [@SantiagoCGsw](https://github.com/SantiagoCGsw)

## 🙏 Créditos

Datos e imágenes proporcionados por el backend del curso (basado en PokéAPI). Pokémon y sus nombres son marcas de Nintendo, Game Freak y Creatures Inc.; este proyecto es solo con fines educativos.
