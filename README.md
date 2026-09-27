# Demo interactiva — Sistema POS para Negocio Local

**👉 https://ariel-rengifo.github.io/sistema-pos/**

Página exclusiva de demostración del sistema POS: el visitante registra su nombre y contraseña, elige rol (dueño / administrador / cajero / mesero) y explora las pantallas reales del sistema con datos de muestra:

- **Mesero** (vista tablet): mesas de colores → pedido → enviar a caja
- **Cajero** (vista laptop): notificación de mesa → cobro → ticket simulado → stock descontado → mesa liberada
- **Administrador** (vista laptop): alta de productos, reposición por lote, creación de personal
- **Dueño** (vista laptop): dashboard de ventas, top producto, stock bajo, gestión de administradores

Todo corre en el navegador (HTML/CSS/JS puro, sin dependencias). Los pedidos y ventas comparten estado dentro de la sesión: lo que el mesero envía, el cajero lo cobra.

El sistema real instalado corre con Python + Flask + SQLite en una Mini PC del negocio (mismo flujo, datos reales, impresora y lector físicos).
