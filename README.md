# Super Dolores · SuperApp en Flutter con TDD

**Materia:** Desarrollo de Aplicaciones Móviles
**Alumno:** González López Yael Isaac
**Fecha:** 20 de noviembre de 2026


## Estructura del proyecto

<img width="113" height="380" alt="image" src="https://github.com/user-attachments/assets/fe5b911c-3cc8-430e-95f5-e38d35b3fdaa" />

## Pruebas de casos (éxito y fallo)

## Pruebas del dominio (30) · test/dominio_test.dart

Pruebas: dinero y fechas, monedero, mensajería, comercio, transporte (Haversine, tarifa dinámica con tope y máquina de estados del viaje), mini-apps y plataforma.

### Éxito (todas en verde)

<img width="399" height="423" alt="image" src="https://github.com/user-attachments/assets/9d18d0e6-42f2-4047-aae3-88591416bc8a" />

### Fallo (formatearPesos)

<img width="406" height="345" alt="image" src="https://github.com/user-attachments/assets/531d8a72-2471-4710-a946-847ade88ce10" />

## Pruebas de servicios (21) · test/servicios_test.dart

Pruebas: compras con comisión del 5%, invariante del dinero total del sistema, idempotencia contra doble toque, compras sin saldo, viajes con comisión del 20% y kill switch de mini-apps.

### Éxito (todas en verde)

<img width="398" height="394" alt="image" src="https://github.com/user-attachments/assets/5b194ae0-a0e8-4414-bc5f-17763da2af56" />

### Fallo (compra: cobra, reparte la comisión del 5% y descuenta inventario)

<img width="398" height="319" alt="image" src="https://github.com/user-attachments/assets/089669f9-5933-44e0-afd5-358b69c04ad8" />

## Pruebas de retención (31) · test/retencion_test.dart

Pruebas: lealtad (puntos por gasto, idempotencia, niveles, bono por variedad, rachas y canje), notificaciones, sugerencias y analítica (DAU, WAU, MAU, stickiness, cohortes y retención D1/D7).

### Éxito (todas en verde)

<img width="401" height="433" alt="image" src="https://github.com/user-attachments/assets/6dff70ef-f637-4374-a99f-4cc69f166555" />

### Fallo (1 punto por cada $10 en compras y viajes)

<img width="404" height="322" alt="image" src="https://github.com/user-attachments/assets/27a667e9-b7e6-4204-a5d6-b83ac84cda9a" />

## Pruebas de ViewModels (22) · test/vms_test.dart

Pruebas: inicio, monedero, chat, tienda, viajes y métricas.

### Éxito (todas en verde)

<img width="398" height="412" alt="image" src="https://github.com/user-attachments/assets/ee57dfb6-fa88-472c-879d-58e703186d89" />

### Fallo (muestra saldo, puntos, nivel y no leídos)

<img width="401" height="350" alt="image" src="https://github.com/user-attachments/assets/b1780998-dbdd-4b51-8186-7bac38156eb7" />

## Todas las pruebas en verde (104)

<img width="392" height="55" alt="image" src="https://github.com/user-attachments/assets/8a817b44-436f-4405-8857-7c02f4937154" />

## Evidencia de la aplicación

### Inicio con saldo, puntos y mini-apps

<img width="300" height="650" alt="WhatsApp Image 2026-11-20 at 14 06 01" src="https://github.com/user-attachments/assets/94c2e3f2-85c6-4c80-a98b-f5f8e0ffda28" />

### Compra en la tienda o viaje pagado con el monedero

<img width="300" height="650" alt="WhatsApp Image 2026-11-20 at 14 06 01 (1)" src="https://github.com/user-attachments/assets/23839fb1-e32d-40ed-bf2b-e2978591df5a" />

### Métricas de retención

<img width="300" height="650" alt="WhatsApp Image 2026-11-20 at 14 06 01 (2)" src="https://github.com/user-attachments/assets/a32a9e09-85a8-4ddf-a31a-b39d17bf31a7" />
