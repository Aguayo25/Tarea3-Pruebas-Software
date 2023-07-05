# Tarea 3 de pruebas de software

#### Integrantes:  
Javier Aguayo - Daniel Roco

#### Requisitos:
* ##### Tener instalado java
* ##### Utilizar EclipseIDE

### Instalación:
#### 1. Clonar repositorio:
    $ git clone https://github.com/Aguayo25/Tarea3-Pruebas-Software.git o descargar el .zip
    $ cd Tarea3-Pruebas-Software

#### 3. Ejecutar programa (con eclipse):
* ##### Importar archivo:
    * Ir a File
    * Import
    * General
    * Existing Proyects into Workspace
    * Select archive file -> Browse (a la derecha del select) (Se elige el archivo .zip descargado)
* ##### Ejecutar arcihvo general:
    * Click derecho sobre carpeta principal, "run as"
* ##### Ejecutar pruebas unitarias:
    * Abrir carpeta raiz
    * Abrir carpeta src
    * Abrir carpeta test
    * Abrir carpeta java
    * Abrir carpeta proyectoUnit
    * Abrir cada archivo de test con doble click, ir a la ventana derecha donde está el código de la prueba y apretar "ctrl" + "R"

#### 4. Consideraciones:
* ##### El cliente no necesita credenciales para interacturar con su menú, pero el administrador sí debe ingresar sus credenciales para poder interacturar con su menú, estas son:
    * user: admin
    * password: 123
* ##### El programa maneja 3 variables globales: 
    * totalbuy: almacena la cantidad total de compras, tanto por el cliente como por el administrador.
    * totalSales: almacena la cantidad global de ventas, que para este caso, solo lo hace el administrador de la tienda.
    * totalPurchases: almacena el flujo de dinero que se va generando el cliente y administrador en la sesión del código, tanto para las compras del cliente/administrador como para las ventas del administrador Esta variable sería la ganancia de la tienda que luego se ve reflejado en el reporte.  
    
* ##### Para el caso de las compras:
    * cuando el cliente compra juegos de la tienda, lo hace al precio normal del juego y la variable totalbuy y totalPurchases incrementan.
    * cuando el administrador compra un juego, este lo hace por un precio menor al valor original, más en específico, un 20% menos del valor original, para así cuando los quiera vender, el negocio tenga ganancias. (Oferta y Demanda). Luego de esto la variable totalPurchases va a decrementar su valor, esto porque la variable totalPurchases ve las ganancias de la tienda, por lo que, cuando la tienda compra juegos está dejando dinero (invirtiendo), lo que, cuando los pueda vender ahi recien se transforma en ganancia.
    * Cuando el cliente compra juegos, la cantidad de inventario del juego comprado decrementa.
    * Cuando el administrador compra juegos, la cantidad de inventario del juego comprado incrementa.
* ##### Para el caso de las ventas:
    * Sólo lo hace el administrador del negocio, vende los juegos por el precio normal del juego y la variable totalSales incrementa.
    * Cuando el administrador vende juegos, el inventario del juego vendido decrementa.

* ##### Según lo analizado entre los participantes de esta tarea, se cumplen todas las funcionalidades principales que se mencionan en el enunciado de la tarea, tanto para el usuario cliente como para el usuario administrador de tienda.

* ##### Nos faltó completar mas cobertura en el archivo main, ya que faltó testear las distintas opcionesc que tiene el menú, puesto que solo se ocuparon algunas (catálogo), pero en total tenemos un 86% aproximado de cobertura del proyecto, lo cual se puede mejorar posteriormente haciendo pruebas para cada uno de los accesos del menú, tanto para el cliente como para el administrador.
