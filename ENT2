-----------------------------------------------------------------
--BODEGA TECH - SCRIPT DE INVENTARIO--
--Autor: Emiliano Rodriguez--
--Fecha: 01-07-2026--

-----------------------------------------------------------------
--SECCION DDL--
CREATE DATABASE BodegaTech

USE BodegaTech

DROP TABLE IF EXISTS inventario;

--CREACION DE TABLA INVENTARIO--

CREATE TABLE inventario(
id_producto INT NOT NULL IDENTITY(1,1) PRIMARY KEY, --INT porque almacena un número entero único; IDENTITY genera el valor automáticamente--
nombre_producto VARCHAR(100) NOT NULL,
categoria VARCHAR(50) NOT NULL,
precio_unitario DECIMAL(10,2) NOT NULL, --DECIMAL(10,2) permite guardar importes con dos decimales, evitando errores de precisión--
stock_actual INT NOT NULL,
stock_minimo INT NOT NULL,
fecha_ingreso DATE NOT NULL, ---- DATE es suficiente porque solo se necesita la fecha de ingreso, sin la hora--
activo TINYINT
);

SELECT * FROM Inventario

-----------------------------------------------------------------
--SECCION DML--

--CARGA DE INFORMACION EN LA BASE DE DATO--

INSERT INTO inventario
(nombre_producto, categoria, precio_unitario, stock_actual, stock_minimo, fecha_ingreso, activo)
VALUES
('Laptop Pro 15', 'Computación', 1200.00, 15, 3, '2024-01-10', 1),
('Mouse Inalámbrico', 'Accesorios', 28.00, 80, 10, '2024-01-15', 1),
('Monitor 4K 27"', 'Computación', 450.00, 12, 2, '2024-01-20', 1),
('Teclado Mecánico', 'Accesorios', 95.00, 40, 5, '2024-01-25', 1),
('Laptop Basic 14', 'Computación', 650.00, 20, 3, '2024-02-05', 1),
('Auriculares BT Pro', 'Audio', 120.00, 35, 5, '2024-02-10', 1),
('Hub USB-C 7 puertos', 'Accesorios', 45.00, 60, 10, '2024-02-15', 1),
('Webcam HD 1080p', 'Accesorios', 85.00, 25, 5, '2024-02-20', 1),
('SSD Externo 1TB', 'Almacenamiento', 130.00, 18, 3, '2024-03-01', 1),
('Parlante Bluetooth', 'Audio', 60.00, 45, 8, '2024-03-05', 1);

--UPDATE PARA MODIFICAR LINEAS DENTRO DE LA ESTRUTURA--

UPDATE inventario SET stock_actual=stock_actual-3 
WHERE id_producto=1; 

UPDATE inventario SET stock_actual=stock_actual-12 
WHERE id_producto=2;

UPDATE inventario SET stock_actual=stock_actual-5 
WHERE id_producto=6;

--UPDATE PARA DISCONTINUAR UN PRODUCTO--

UPDATE inventario SET activo=0
WHERE id_producto=8

SELECT * FROM inventario
