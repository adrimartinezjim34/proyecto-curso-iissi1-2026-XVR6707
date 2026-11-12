# ETSIILADOS.SL

## Miembros del grupo L7

1. Moya Delgado, Fidel
1. Martínez Jiménez, Adrián
1. Morón Iglesias, Manuel
1. Macías Sánchez, Marcos

## 1. Introducción al problema

  Somos los dueños de la empresa Etsiilados la cual se basa en manejar un almacén de bebidas alcohólicas. Recibimos productos de distintos proveedores, los almacenamos y los distribuimos a múltiples establecimientos como bares, restaurantes y tiendas especializadas en nuestros productos.
Hasta el momento, el almacén se había administrado de forma manual, a base de mantener los registros apuntados en albaranes físicos y atendiendo los pedidos de los clientes mediante llamadas telefónicas, lo cual dificulta y ralentiza la gestión de pedidos y del stock.
Nuestro anterior sistema de gestión tenía varios fallos tanto para los clientes, como para los empleados de la empresa:

- Los clientes sólo podían ser atendidos por llamada y durante el horario de oficina, impidiendoles conocer el stock de productos disponibles, y una vez habiendo realizado el pedido, no podían conocer el estado del mismo sin consultar a la empresa por teléfono.

- Los trabajadores no podían conocer el stock disponible con certeza y tenían que revisar albaranes o contar a mano, provocando errores, pérdidas de tiempo y la aceptación de pedidos que contienen productos agotados, además la atención de las llamadas produce interrupciones en el flujo de trabajo y facilitaba las equivocaciones al contar inventario y apuntar pedidos.
  
Todo esto genera retrasos, errores y clientes insatisfechos. Por eso Etsiilados necesita un sistema informático que gestione el stock en tiempo real y permita a los clientes hacer y seguir sus pedidos de forma sencilla. 


## 2. Glosario de términos

Albarán: Nota de entrega que firma la persona que recibe una mercancía

## 3. Visión general del sistema
  El sistema de gestión ETSIILADOS a desarrollar deberá centralizar la información necesaria para controlar el almacén de bebidas destiladas. Gestionará productos con sus datos comerciales y su stock mínimo; lotes y ubicaciones para conocer la procedencia y la posición física de cada unidad; existencias para calcular la cantidad disponible de cada lote en cada ubicación; clientes y empleados con sus datos identificativos y de contacto; pedidos realizados por los clientes; y movimientos de entrada y salida con la fecha, el empleado responsable y el detalle de los productos afectados.

  La información se almacenará de forma centralizada y segura, de modo que el stock se actualice al confirmar cada movimiento y pueda consultarse en tiempo real. El sistema conservará el historial de operaciones para garantizar la trazabilidad de la mercancía y evitar descuadres de inventario.

  La aplicación deberá ofrecer una interfaz sencilla e intuitiva, accesible únicamente para todos los usuarios, dando mayor control respecto a los movimientos según sean o no autorizados. Según su rol(cliente o empleado), podrán realizar pedidos únicamente o gestionar y actualizar el almacen.

### 3.1. Requisitos generales
#### R.G.01. Digitalización del almacén. 
Como administrador del almacén Etsiilados, quiero disponer de un sistema completamente digital para gestionar el almacén y eliminar procesos manuales.

#### R.G.02. Pedidos online
Como Cliente, quiero realizar pedidos online y disponer de su seguimiento para conocer el estado de este sin realizar llamadas extra.

#### R.G.03. Control de proveedores.
Como Gestor de tienda, quiero conocer la información de los proveedores, para tener un catálogo fiable.

#### R.G.04. Atención al cliente
Como cliente, quiero poder mantener contacto con el personal del almacén para la consulta de dudas o incidencias en los pedidos.
  

### 3.2. Usuarios del sistema
Gestor de tienda

Administrador del almacén

Cliente

## 4. Catálogo de requisitos

### 4.1. Requisitos funcionales

#### R.F.01. Productos a punto de cumplir
Como Administrador del almacén,quiero recibir un aviso en mi móvil cuando haya mercancía que vaya a caducar en menos de 48 horas,
para ponerla a la venta y evitar tener que tirarla.

#### R.F.02. Disponibilidad 24/7
Como Gestor de tienda, quiero que la disponibilidad del sistema sea lo más cercana posible a 24/7 para facilitar las compras de los clientes

#### R.F.03 Registrar pedidos
Como cliente, quiero registrar pedidos de productos del almacén para mantener constancia de lo pedido.

#### R.F.04. Cancelación de pedidos
Como Cliente, quiero poder cancelar un pedido mientras no haya sido enviado, en caso de error o incidencia, para evitar pagar productos que no necesito.

#### R.F.05 Cancelación de pedidos
Como Gestor de tienda, quiero poder cancelar un pedido cuando no se pueda realizar por falta de stock o incidencia, para evitar fallos en la gestión.


#### 4.1.1. Requisitos de información

##### R.I.01. Información de los productos

Como usuario del sistema, quiero disponer de la información de cada producto para conocer sus características y consultar su disponibilidad en el almacén.

La información que se almacenará será:

- Código, nombre y categoría del producto.
- Stock mínimo establecido.
- Existencias actuales, calculadas a partir de las cantidades disponibles en sus lotes y ubicaciones.

**Prueba de aceptación**

**Casos positivos**

- Al consultar un producto existente, se muestran todos sus datos y la cantidad disponible coincide con la suma de sus existencias.
- Si un producto está almacenado en varios lotes o ubicaciones, el sistema refleja correctamente su stock total.

**Casos negativos**

- Al introducir un código que no corresponde a ningún producto, el sistema informa de que no existen resultados.
- No se permite registrar dos productos con el mismo código.

##### R.I.02. Información del inventario

Como administrador del almacén, quiero consultar la información de los lotes, ubicaciones y existencias para localizar la mercancía y conocer la cantidad disponible en cada zona.

La información que se almacenará será:

- Código del lote y producto al que pertenece.
- Código y descripción de la ubicación.
- Cantidad disponible de cada lote en cada ubicación.

**Prueba de aceptación**

**Casos positivos**

- Al consultar un lote, se muestra su producto y el reparto de unidades entre las distintas ubicaciones.
- La suma de las cantidades del lote por ubicación coincide con su disponibilidad total.

**Casos negativos**

- No se admite más de un registro de existencia para la misma pareja de lote y ubicación.
- No se permiten cantidades negativas en las existencias.

##### R.I.03. Información de los pedidos

Como cliente, quiero disponer de la información de mis pedidos para comprobar qué productos he solicitado y conocer su estado.

La información que se almacenará será:

- Identificador del cliente que realiza el pedido.
- Fecha de solicitud y estado del pedido.
- Producto, proveedor y cantidad solicitada en cada línea.

**Prueba de aceptación**

**Casos positivos**

- Al consultar un pedido, se muestran el cliente, la fecha, el estado y todas sus líneas.
- Cada línea identifica claramente el producto, el proveedor seleccionado y la cantidad solicitada.

**Casos negativos**

- No se admite un pedido sin cliente o sin ninguna línea.
- Se rechaza una línea si la cantidad no es válida o el proveedor indicado no ofrece ese producto.

##### R.I.04. Información de los proveedores

Como gestor de tienda, quiero consultar la información de los proveedores para conocer sus datos de contacto y los productos que suministra cada uno.

La información que se almacenará será:

- NIF y razón social.
- Teléfono y correo electrónico.
- Productos ofrecidos por el proveedor.

**Prueba de aceptación**

**Casos positivos**

- Al consultar un proveedor, se muestran sus datos y el catálogo de productos que ofrece.
- Un mismo producto puede aparecer asociado a varios proveedores.

**Casos negativos**

- No se permite registrar más de un proveedor con el mismo NIF.
- Al consultar un NIF inexistente, el sistema informa de que el proveedor no está registrado.

##### R.I.05. Información de los movimientos de almacén

Como administrador del almacén, quiero disponer del historial de movimientos para conocer las entradas y salidas realizadas y mantener la trazabilidad del inventario.

La información que se almacenará será:

- Identificador, fecha y hora, tipo de movimiento y empleado responsable.
- Estado de consolidación e importe de la venta cuando corresponda.
- Cantidad movida y existencia afectada en cada detalle, incluyendo su producto, lote y ubicación.

**Prueba de aceptación**

**Casos positivos**

- Al consultar un movimiento, se muestran sus datos generales, el empleado responsable y todos sus detalles.
- Un movimiento consolidado permite identificar qué cantidades se añadieron o retiraron y de qué ubicaciones.

**Casos negativos**

- No se admite un movimiento sin empleado responsable o sin al menos un detalle.
- Si se consulta un identificador inexistente, el sistema no muestra información de otros movimientos.

##### R.I.06. Información de los empleados

Como administrador del almacén, quiero disponer de la información de los empleados para identificar a los responsables de las operaciones y controlar su acceso al sistema.

La información que se almacenará será:

- Nombre y apellidos.
- Nombre de usuario y rol.
- Estado de la cuenta, que podrá ser activa o inactiva.

**Prueba de aceptación**

**Casos positivos**

- Al consultar un empleado, se muestran sus datos, su rol y el estado actual de la cuenta.
- Desde un movimiento se puede identificar al empleado que lo registró.

**Casos negativos**

- No se permite registrar dos empleados con el mismo nombre de usuario.
- Una cuenta inactiva no puede acceder al sistema.

### 4.1.2. Reglas de negocio

#### R.N.01. Venta Mínima
Como Gestor de tienda, quiero que se establezca una venta mínima de 20€.
Para que haya un margen de rentabilidad amplio.

#### R.N.02.Tiempo Máximo Cancelación
Como Gestor de tienda, quiero que los pedidos sin incidencias no puedan ser cancelados una vez pasadas las 24 horas para ahorrar dinero y tiempo.

#### R.N.03.Un cliente no puede realizar dos pedidos simultáneos
Como Gestor de tienda, quiero que cada cliente solo pueda tener un pedido activo para que no pueda realizar otro hasta recibir el que tiene en curso. 

#### R.N.04. Stock mínimo para venta
Como Administrador del almacén, quiero que cada producto tenga un stock mínimo de 3 unidades, para saber cuando se puede vender o no el producto.

### 4.2. Mapa de historias de usuario (opcional)

### 4.3. Requisitos no funcionales (opcional)

**R.N.F. 01. Título requisito no funcional**
Como [tipo de usuario]
quiero [servicio]
para [razón]

-- fin entregable 1 --

## 5. Modelo conceptual
<img width="3024" height="4032" alt="Modelado Conceptual" src="https://github.com/user-attachments/assets/4e30d2ac-cb8e-4d91-8b0d-65a6e54e7188" />


### 5.1. Diagramas de clases UML

- con restricciones.

### 5.2. Escenarios de prueba

- con descripción textual y diagrama de objetos UML.

## 6. Matrices de trazabilidad

- Matriz de trazabilidad entre los elementos del modelo conceptual y los requisitos.

|       | EntidadX   | AsociaciónX  | RestricciónX  | Entidad2 ...   | 
|:------|:-----------|:-----------|:-----------|:-----------|
| RI-1  | X          | X          | X          | X          |
| RI-2  |            | X          |            | X          |
| RF-1  |            | X          |            | X          |
| RF-2  | X          |            | X          | X          |
| RN-1  |            | X          |            |            |
| RN-2  | X          | X          | X          |            |
| ...   |            |            |            |            |

-- fin entregable 2 --

## 7. Modelo relacional en 3FN

- Relaciones obtenidas al aplicar la transformación del modelo conceptual.

### 7.1.  Justificación de la estrategia de transformación de jerarquías

- si se identificaron jerarquías en el MC.


### 8. Matriz de trazabilidad MC/SQL (opcional):

- Restricciones sobre el MC / Elementos del modelo tecnológico (SQL) (Triggers, checks, etc.)
- Incluir Reglas de negocio — Constraints/Triggers en las matrices de trazabilidad para el entregable 3

|       | EntidadX   | AsociaciónX  | RestricciónX  | Entidad2 ...   | 
|:-------|:-------|:-------|:-------|:-------|
| TABLA-1 |        |        |        |        |
| TABLA-2 |        |        |        |        |
| TABLA-3 |        |        |        |        |
| TABLA-4 |        |        |        |        |
| TRIG-1 |        |        |        |        |
| TRIG-2 | X      | X      |        | X      |
| TRIG-3 |        | X      |        | X      |
| TRIG-4 |        |        | X      |        |
| CONST-1 |        |        |        |        |
| CONST-2 | X      | X      |        | X      |
| CONST-3 |        | X      |        | X      |
| CONST-4 |        |        | X      |        |

Se consideran todo tipo de constraints declarativas (aquellas definidas durante el CREATE TABLE).
-- fin entregable 3 --

## Referencias


