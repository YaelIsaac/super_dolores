# Super Dolores · SuperApp en Flutter con TDD

**Materia:** Desarrollo de Aplicaciones Móviles
**Alumno:** González López Yael Isaac
**Fecha:** 20 de noviembre de 2026

## Descripción

SuperApp didáctica de Dolores Hidalgo que junta varios servicios en una sola app, como WeChat o Rappi: mensajería, monedero para enviar dinero, tienda de comercios locales y viajes con tarifa calculada por distancia y tiempo. La plataforma cobra comisión (5% en comercio y 20% en viajes) y el dinero pasa por una cuenta de custodia. Tiene un programa de lealtad (puntos, niveles, bonos por variedad y rachas), mini-apps que se pueden apagar con un "kill switch" (incluida una de un tercero), notificaciones y una pantalla de métricas de retención (DAU, MAU, cohortes y retención D1/D7). Todo el dominio es Dart puro y se desarrolló con TDD; los servicios son simulados y viven en memoria.

## Estructura del proyecto

<!-- PEGA AQUÍ LA CAPTURA -->

## Pruebas de casos (éxito y fallo)

## Pruebas del dominio (30) · test/dominio_test.dart

Pruebas: dinero y fechas, monedero, mensajería, comercio, transporte (Haversine, tarifa dinámica con tope y máquina de estados del viaje), mini-apps y plataforma.

### Éxito (todas en verde)

<!-- PEGA AQUÍ LA CAPTURA -->

### Fallo (formatearPesos)

<!-- PEGA AQUÍ LA CAPTURA -->

## Pruebas de servicios (21) · test/servicios_test.dart

Pruebas: compras con comisión del 5%, invariante del dinero total del sistema, idempotencia contra doble toque, compras sin saldo, viajes con comisión del 20% y kill switch de mini-apps.

### Éxito (todas en verde)

<!-- PEGA AQUÍ LA CAPTURA -->

### Fallo (compra: cobra, reparte la comisión del 5% y descuenta inventario)

<!-- PEGA AQUÍ LA CAPTURA -->

## Pruebas de retención (31) · test/retencion_test.dart

Pruebas: lealtad (puntos por gasto, idempotencia, niveles, bono por variedad, rachas y canje), notificaciones, sugerencias y analítica (DAU, WAU, MAU, stickiness, cohortes y retención D1/D7).

### Éxito (todas en verde)

<!-- PEGA AQUÍ LA CAPTURA -->

### Fallo (1 punto por cada $10 en compras y viajes)

<!-- PEGA AQUÍ LA CAPTURA -->

## Pruebas de ViewModels (22) · test/vms_test.dart

Pruebas: inicio, monedero, chat, tienda, viajes y métricas.

### Éxito (todas en verde)

<!-- PEGA AQUÍ LA CAPTURA -->

### Fallo (muestra saldo, puntos, nivel y no leídos)

<!-- PEGA AQUÍ LA CAPTURA -->

## Todas las pruebas en verde (104)

<!-- PEGA AQUÍ LA CAPTURA -->

## Evidencia de la aplicación

### Inicio con saldo, puntos y mini-apps

<!-- PEGA AQUÍ LA CAPTURA -->

### Compra en la tienda o viaje pagado con el monedero

<!-- PEGA AQUÍ LA CAPTURA -->

### Métricas de retención

<!-- PEGA AQUÍ LA CAPTURA -->

## Conclusión

Con TDD cada regla de la SuperApp nació de una prueba que primero falló: el dinero nunca se crea ni se pierde (la suma total del sistema no cambia), un doble toque no cobra dos veces, las comisiones se reparten exacto al centavo y los puntos de lealtad premian el uso real, no cualquier clic. Las capturas de fallo demuestran que las pruebas sí detectan errores. Como el dominio es Dart puro, los 104 casos se prueban en segundos sin servidor, y las métricas de retención se calculan con definiciones claras para no engañarse con los números.
