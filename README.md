# Sistema POS para Negocio Local

Punto de venta para negocios pequeños: **Mini PC como servidor**, el cajero con **laptop o tablet** y el mesero con **tablet o celular**, todo conectado por la red local del negocio. **Sin nube, sin mensualidades.**

## Página promocional con demo interactiva

👉 **https://ariel-rengifo.github.io/sistema-pos/**

La página incluye una **demo interactiva** del sistema: el visitante crea su cuenta, entra como mesero (toma pedidos en mesas desde una vista de tablet) o como cajero (cobra y emite tickets en una vista de laptop), y recorre el flujo real mesa → pedido → cobro → ticket, con datos de muestra.

## Características del sistema

- Login con 4 roles y permisos (dueño / administrador / cajero / mesero)
- Inventario con código de barras y alertas de stock bajo
- Venta de mostrador con ticket simulado y descuento automático de stock
- Flujo de pedidos: mesero (tablet) → caja (laptop/tablet) → mesa liberada
- Multi-dispositivo real por red local

## Stack

Backend: Python + Flask + SQLite · Frontend: HTML/CSS/JS · Demo publicada en GitHub Pages

## Contenido del repo

- `index.html` — página promocional + demo interactiva (HTML puro, sin dependencias)
- `presentacion.md` — documento de presentación para clientes

## Cómo correr el prototipo real instalado

El prototipo funcional (Flask + SQLite) corre en la Mini PC del negocio siguiendo `iniciar_servidor.bat`; los demás dispositivos entran por navegador a la IP local.
