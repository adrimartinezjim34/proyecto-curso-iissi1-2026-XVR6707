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
Los clientes sólo podían ser atendidos por llamada y durante el horario de oficina, impidiendoles conocer el stock de productos disponibles, y una vez habiendo realizado el pedido, no podían conocer el estado del mismo sin consultar a la empresa por teléfono.

  Los trabajadores no podían conocer el stock disponible con certeza y tenían que revisar albaranes o contar a mano, provocando errores, pérdidas de tiempo y la aceptación de pedidos que contienen productos agotados, además la atención de las llamadas produce interrupciones en el flujo de trabajo y facilitaba las equivocaciones al contar inventario y apuntar pedidos.
  
  Todo esto genera retrasos, errores y clientes insatisfechos. Por eso Etsiilados necesita un sistema informático que gestione el stock en tiempo real y permita a los clientes hacer y seguir sus pedidos de forma sencilla. 


## 2. Glosario de términos

Albarán: Nota de entrega que firma la persona que recibe una mercancía

## 3. Visión general del sistema
  El sistema de gestión ETSIILADOS a desarrollar deberá centralizar la información necesaria para controlar el almacén de bebidas destiladas. Gestionará productos con sus datos comerciales y su stock mínimo; lotes y ubicaciones para conocer la procedencia y la posición física de cada unidad; existencias para calcular la cantidad disponible de cada lote en cada ubicación; clientes y empleados con sus datos identificativos y de contacto; pedidos realizados por los clientes; y movimientos de entrada y salida con la fecha, el empleado responsable y el detalle de los productos afectados.

  La información se almacenará de forma centralizada y segura, de modo que el stock se actualice al confirmar cada movimiento y pueda consultarse en tiempo real. El sistema conservará el historial de operaciones para garantizar la trazabilidad de la mercancía y evitar descuadres de inventario.

  La aplicación deberá ofrecer una interfaz sencilla e intuitiva, accesible únicamente para todos los usuarios, dando mayor control respecto a los movimientos según sean o no autorizados. Según su rol(cliente o empleado), podrán realizar pedidos únicamente o gestionar y actualizar el almacen.

### 3.1. Requisitos generales
#### RG-01. Digitalización del almacén. 
Como administrador del almacén Etsiilados, quiero disponer de un sistema completamente digital para gestionar el almacén y eliminar procesos manuales.

#### RG-02. Pedidos online
Como Cliente, quiero realizar pedidos online y disponer de su seguimiento para conocer el estado de este sin realizar llamadas extra.

#### RG-03. Control de proveedores.
Como Gestor de tienda, quiero conocer la información de los proveedores, para tener un catálogo fiable.

#### RG-04. Atención al cliente
Como cliente, quiero poder mantener contacto con el personal del almacén para la consulta de dudas o incidencias en los pedidos.
  

### 3.2. Usuarios del sistema
Gestor de tienda
Responsable del almacén
Cliente

## 4. Catálogo de requisitos

### 4.1. Requisitos funcionales

#### R.F.01. Título requisito funcional

Como [tipo de usuario]
quiero [servicio]
para [razón]

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- Se debe aplicar la regla de negocio R.N.XX.
- ...

#### 4.1.1. Requisitos de información

##### R.I.01. Título requisito de información

Como [tipo de usuario]
quiero [servicio]
para [razón]

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- ...

#### 4.1.2. Reglas de negocio

##### R.N.01. Título regla negocio

Descripción de la regla de negocio.

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


