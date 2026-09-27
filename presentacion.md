# Sistema POS para Negocio Local — Propuesta de Desarrollo

> Documento de presentación para cliente. Base para armar una presentación (slides o demo en vivo).

---

## 1. El problema

Los negocios pequeños (abarrotes, cafeterías, taquerías, tienditas) operan a diario con:

- Tickets de papel y cálculos a mano.
- Inventario contado "de memoria" o en un cuaderno.
- Sin registro de qué se vende, cuándo y cuánto.
- Errores de cobro y desviaciones de dinero difíciles de detectar.
- Los sistemas POS comerciales cuestan demasiado: licencias mensuales, suscripciones a la nube, hardware propietario (lectores, cajas registradoras, suscripciones).

**Resultado:** el dueño no tiene control real de su negocio.

---

## 2. La solución

Un sistema de punto de venta (POS) que funciona con los equipos que el negocio **ya tiene**:

| Equipo | Rol en el sistema | Costo extra |
|---|---|---|
| Laptop del negocio | Servidor + base de datos | Ninguno |
| Tablet o celular del mesero | Tomar pedidos de mesas | Ninguno |
| Celular del cajero | Cobrar y emitir tickets | Ninguno |

**Todo conectado por la red Wi-Fi propia del negocio. Sin nube. Sin mensualidades. Sin hardware nuevo obligatorio.**

---

## 3. Prototipo funcional — ya construido

No es una idea en papel: hay un **prototipo operativo** que se puede demostrar en vivo.

### Lo que ya funciona hoy

- **Login con 4 roles y permisos diferenciados**
  - Dueño: ve todo, gestiona administradores, configura el sistema.
  - Administrador: controla operación diaria e inventario.
  - Cajero: cobra ventas de mostrador y pedidos de mesa.
  - Mesero: toma pedidos y avisa a caja (no ve montos ni cobros).
- **Inventario completo**: alta de productos con código de barras, reposición por lote, alertas de stock bajo.
- **Venta de mostrador**: escaneo de código → carrito → cobro → ticket en pantalla → descuento automático de inventario.
- **Pedidos de mesa**: mesero arma el pedido → notificación en tiempo real al cajero → cobro ligado al pedido → mesa se libera sola.
- **Dashboard del dueño**: ventas del día y de la semana, producto más vendido, últimos tickets.
- **Multi-dispositivo real**: tablet y celular entran por navegador a la red local. Probado con flujo completo mesero → caja → cobro.

### Demo sugerida (10 minutos en vivo)

1. Entrar desde la laptop como **dueño** → mostrar dashboard e inventario.
2. Entrar desde la tablet como **mesero** → tomar pedido en una mesa → "enviar a caja".
3. Entrar desde el celular como **cajero** → aparece la notificación → cobrar → ticket en pantalla.
4. Regresar a la laptop → el dashboard ya refleja la venta y el stock descontado.

> Ese momento en que el pedido "viaja" de la tablet al celular frente al cliente vende el sistema solo.

---

## 4. Por qué este enfoque gana

| Sistema POS comercial | Este sistema |
|---|---|
| Mensualidad por suscripción | Pago único por desarrollo |
| Depende de internet externo | Funciona sin internet (red local) |
| Hardware propietario | Usa celulares y tablets que ya tienen |
| Licencias por sucursal/dispositivo | Dispositivos ilimitados en la red |
| Datos en servidores de terceros | Los datos quedan en la laptop del negocio |

---

## 5. Ruta de desarrollo (del prototipo al sistema real)

El prototipo es la **fase 0**. El sistema completo se construye por fases, cada una entregable y usable:

### Fase 1 — Base sólida (operativa real)
- Impresión real en ticketera térmica.
- Lector de código de barras USB real (el sistema ya lo simula: conectarlo es directo).
- Manejo de errores y respaldos automáticos de la base de datos.
- Categorías, descuentos, propinas, devoluciones.

### Fase 2 — Control del negocio
- Cortes de caja por turno (cuadratura de efectivo).
- Reportes: ventas por día/semana/producto/categoría/mesero.
- Control de horarios y comisiones del personal.

### Fase 3 — Administración remota (opcional)
- Panel del dueño desde fuera del negocio (acceso seguro por internet).
- Notificaciones (venta grande, stock agotado, cierre de caja).
- Respaldo de datos en la nube opcional.

> Cada fase se presenta con demo funcional, igual que esta. El cliente paga avance visible, no promesas.

---

## 6. Tecnología (transparente y confiable)

- **Python + Flask** — lenguaje estándar de la industria, fácil de mantener.
- **SQLite** — base de datos local en un solo archivo, sin servidores costosos que administrar.
- **HTML multiplataforma** — funciona en cualquier navegador: Windows, Android, iOS.

Ventaja para el cliente: **no depende de un proveedor cerrado**. El código es suyo y cualquier desarrollador Python puede darle mantenimiento.

---

## 7. Siguiente paso

Propuesta concreta para iniciar:

1. **Prueba piloto gratuita** del prototipo en el negocio del cliente (1 semana, datos de prueba).
2. Levantar **requerimientos reales** del negocio (cuántas mesas, cuántos productos, turnos).
3. Cotizar la **Fase 1** con alcance cerrado y fecha de entrega.

---

## Anexo — Qué mostrar en la presentación

- Capturas o demo en vivo del login, dashboard, captura de pedido y ticket.
- Esta tabla de roles y permisos (genera confianza: el sistema distingue dueño/admin/cajero/mesero).
- El mensaje clave: **"Su negocio ya tiene las computadoras. Póngalas a trabajar."**
