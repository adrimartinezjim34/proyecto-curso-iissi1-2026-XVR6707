# ETSIILADOS.SL

## Miembros del grupo L7

1. Moya Delgado, Fidel
1. Martínez Jiménez, Adrián
1. Morón Iglesias, Manuel
1. Macías Sánchez, Marcos

## 1. Introducción al problema

  Somos los dueños de la empresa Etsiilados.SL la cual se basa en manejar un almacén de bebidas alcohólicas. Recibimos productos de distintos proveedores, los almacenamos y los distribuimos a múltiples establecimientos como bares, restaurantes y tiendas especializadas en nuestros productos.

  Construimos este proyecto con el objetivo de mejorar el control acerca de los productos que entran y salen de nuestras instalaciones, debido a que con el paso  del tiempo hemos notado que hay cierta deficiencia a la hora de saber con certeza el stock disponible. Esto genera ciertos problemas con nuestros clientes al concretar una fecha de entrega o con nosotros al cumplirla. Lo último que queremos es que busquen otros distribuidores,perdiendo ganancias.
Además, queremos encontrar una forma de controlar mejor la ubicación de nuestros productos, para así ser más ágiles y competitivos en el sector.

Para solucionar estos problemas, se propone desarrollar un sistema de gestión que centralice toda la información relacionada con los productos, los lotes, los proveedores, los clientes, las ubicaciones y los movimientos de mercancía.

## 2. Glosario de términos

La terminología del tema elegido, no da lugar a confusión y los términos son generales.

## 3. Visión general del sistema

### 3.1. Requisitos generales
RG-01. Mantener el catálogo del almacén
  Como responsable del almacén, quiero mantener organizada la información de las referencias y sus proveedores, para identificar correctamente los productos que gestiona la empresa.
  
RG-02. Controlar las existencias
  Como responsable del almacén, quiero conocer las existencias por referencia, lote y ubicación, para disponer de un inventario fiable y localizar la mercancía.
  
RG-03. Conservar la trazabilidad de los movimientos
  Como responsable del almacén, quiero conservar la trazabilidad de las entradas y salidas de mercancía, para poder reconstruir los movimientos de cada lote y conocer quién los registró.
  
RG-04. Facilitar la supervisión del almacén
  Como responsable del almacén, quiero consultar la situación del inventario y las necesidades de reposición, para detectar incidencias y planificar el abastecimiento.

### 3.2. Usuarios del sistema
Gestor de tienda
Responsable del almacén

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


