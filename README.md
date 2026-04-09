# 🗄️ Sistema de Gestión de Ventas – SQL

## 🚀 Descripción
Este proyecto consiste en el desarrollo de una base de datos relacional para gestionar ventas de una empresa ficticia llamada "Comercio Ya". La solución permite registrar clientes, productos y transacciones, facilitando el almacenamiento y análisis de la información.

---

## 🎯 Objetivo
Reemplazar el uso de planillas por un sistema estructurado que permita mejorar la integridad de los datos, reducir errores y facilitar consultas analíticas mediante SQL.

---

## 🛠️ Tecnologías utilizadas
- SQL  
- Base de datos relacional  
- SQLite  

---

## 🧠 Modelo de datos
El sistema se basa en tres entidades principales:

- **Clientes**
- **Productos**
- **Ventas**

La tabla ventas actúa como tabla transaccional, vinculando clientes y productos mediante claves foráneas.

---

## 📊 Funcionalidades implementadas

### 🔹 Creación de tablas
- Definición de claves primarias y foráneas  
- Estructura relacional normalizada  

### 🔹 Inserción de datos
- Registro de clientes, productos y ventas  

### 🔹 Consultas SQL
- Consultas simples (`SELECT`)  
- Filtros (`WHERE`)  
- JOIN entre tablas  
- Agregaciones (`SUM`, `AVG`)  
- Consultas agrupadas  
- Subconsultas  

### 🔹 Manipulación de datos
- Actualización de registros (`UPDATE`)  
- Eliminación de datos (`DELETE`)  

### 🔹 Automatización
- Trigger para actualización automática de stock después de una venta  

---

## 💡 Ejemplo de consulta

```sql
SELECT c.nombre AS cliente,
       p.nombre AS producto,
       v.fecha
FROM Ventas v
JOIN Clientes c ON v.id_cliente = c.id_cliente
JOIN Productos p ON v.id_producto = p.id_producto;
