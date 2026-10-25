# VentaFácil — Sistema de ventas
Documentación del examen práctico: Ciclo de vida de un proyecto informático.

## 1. Objetivo principal
- **Nombre del proyecto:** VentaFácil
- **Problema:** El negocio registra las ventas en cuaderno, lo que genera errores de cálculo, pérdida de facturas y falta de reportes.
- **Objetivo principal:** Desarrollar un sistema que registre ventas, clientes y productos de forma rápida y confiable.
- **Objetivos específicos:**
- Registrar productos con precio y stock
- Registrar clientes y su historial de compras
- Emitir ventas con total automático
- Consultar reportes de ventas por fecha
- **Alcance inicial:** Registro de productos, clientes y ventas con reporte diario. No incluye facturación electrónica ni pagos en línea.

## 2. Análisis funcional
**Usuarios del sistema:**
- Administrador
- Vendedor
- Cliente (consulta)

**Necesidades principales:**
- Vender rápido
- Controlar el stock disponible
- Conocer los ingresos del día

**Requisitos funcionales**

| Código | Requisito |
|---|---|
| RF1 | Registrar, editar y eliminar productos |
| RF2 | Registrar clientes |
| RF3 | Crear una venta con varios productos |
| RF4 | Calcular subtotal, IVA y total |
| RF5 | Generar reporte de ventas por fecha |

**Requisitos no funcionales**

| Código | Requisito |
|---|---|
| RNF1 | Interfaz sencilla, usable en menos de 10 min de capacitación |
| RNF2 | Respuesta de cada pantalla en menos de 3 segundos |
| RNF3 | Acceso con usuario y contraseña |
| RNF4 | Compatible con Chrome, Edge y Firefox |
| RNF5 | Respaldo diario de la información |

## 3. Planificación
| Integrante | Responsabilidad |
|---|---|
| 1 | Líder / coordinación |
| 2 | Análisis funcional |
| 3 | Requisitos |
| 4 | Diseño UI |
| 5 | Desarrollo |
| 6 | GitHub / integración |

**Calendario:** Análisis (10 min) → Diseño (10 min) → Desarrollo (15 min) → Pruebas (5 min) → Publicación (2 min)

## 4. Diseño detallado
- **Arquitectura propuesta (sistema real):** Clean Architecture en C# (Domain, Application, Infrastructure) con capa de presentación Web API y base de datos relacional.
- **Arquitectura del prototipo:** sitio estático (HTML + CSS), sin base de datos, con datos ficticios.
- **Tecnologías:** HTML5, CSS3, GitHub y GitHub Pages (prototipo); C#/.NET, Web API y SQL Server (versión completa).
- **Módulos:** Inicio, Productos, Clientes, Ventas.
- **Navegación:** menú superior → Inicio | Productos | Clientes | Ventas. Cada módulo muestra una tabla y un formulario de registro.

| Módulo | Columnas de la pantalla |
|---|---|
| Productos | Código, Producto, Precio, Stock |
| Clientes | ID, Cliente, Teléfono, Compras |
| Ventas | Factura, Fecha, Cliente, Total |

**Pantallas principales:** (1) Inicio con indicadores, (2–4) una pantalla por módulo con tabla y formulario "Nuevo registro".

## 5. Ejecución
Prototipo en la carpeta de este proyecto:
- `index.html`: estructura, menú y 3 módulos con datos ficticios.
- `style.css`: estilos. La navegación entre módulos usa enlaces ancla (`#modulo`) y `:target`, sin JavaScript.

## 6. Seguimiento y pruebas
| Prueba | Resultado esperado | ¿Cumple? |
|---|---|---|
| Abrir `index.html` | Se ve la página de inicio con indicadores | ☐ |
| Clic en cada opción del menú | Se muestra el módulo correspondiente | ☐ |
| Ver tablas | Aparecen datos ficticios | ☐ |
| Ver en celular (reducir ventana) | El menú y las tablas se adaptan | ☐ |
| Abrir URL de GitHub Pages | Carga igual que en local | ☐ |

## 7. Aceptación
**¿El prototipo demuestra la solución planteada?** Sí: muestra el menú, los módulos principales, tablas con datos de ejemplo y formularios de registro que representan los requisitos definidos.

| Requisito | Descripción | Dónde se demuestra | Verificado |
|---|---|---|---|
| RF1 | Registrar, editar y eliminar productos | Módulo Productos | ☐ |
| RF2 | Registrar clientes | Módulo Clientes | ☐ |
| RF3 | Crear una venta con varios productos | Módulo Ventas | ☐ |
| RF4 | Calcular subtotal, IVA y total | Módulo Productos | ☐ |
| RF5 | Generar reporte de ventas por fecha | Módulo Clientes | ☐ |

## 8. Cierre y mantenimiento
1. Crear el repositorio en GitHub y subir `index.html`, `style.css` y esta documentación.
2. Verificar que el repositorio esté actualizado (último commit visible).
3. Activar GitHub Pages: *Settings → Pages → Branch: main, carpeta /(root)*.
4. Presentar la URL: `https://<usuario>.github.io/<repositorio>/`

**Mantenimiento propuesto:** corregir errores, agregar conexión a base de datos y Web API, añadir inicio de sesión por roles y nuevos reportes.
