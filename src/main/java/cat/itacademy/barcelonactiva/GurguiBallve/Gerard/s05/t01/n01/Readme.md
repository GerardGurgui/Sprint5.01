
# S5.01 - Api Rest Spring boot + Aplicación web


Tenemos una entidad llamada Sucursal, que dispone de las siguientes propiedades:

- Integer pk_SucursalID

- String nombreSucursal

- String paisSucursal

 

También tenemos una DTO llamada SucursalDTO, que tendrá las mismas propiedades que la entidad Sucursal, añadiendo una:

- String tipoSucursal.

Esta propiedad, en función del país de la sucursal, deberá indicar si es “UE” o “Fuera UE”. Para ello puedes tener una lista privada en la misma DTO (por ejemplo: List<String> países), con los países que forman parte de la UE.

Aprovechando la especificación JPA, deberás persistir a la entidad Sucursal en una base de datos MySql, siguiendo el patrón MVC.

El consejo es que SucursalDTO la utilices en el Controller y la Vista, y Sucursal en el Repository. La capa de servicios será la encargada de realizar la traducción entre ambas.

Para ello, dependiendo del package principal, crearás una estructura de packages, donde ubicarás las clases que necesites:

- cat.itacademy.barcelonactiva.apellidos.nombre.s05.t01.n01.controllers

- cat.itacademy.barcelonactiva.apellidos.nombre.s05.t01.n01.model.domain

- cat.itacademy.barcelonactiva.apellidos.nombre.s05.t01.n01.model.dto

- cat.itacademy.barcelonactiva.apellidos.nombre.s05.t01.n01.model.services

- cat.itacademy.barcelonactiva.apellidos.nombre.s05.t01.n01.model.repository

La clase ubicada en el paquete controllers (SucursalController, por ejemplo), deberá ser capaz de dar respuesta a las siguientes peticiones para actualizar y consultar información:

http://localhost:9000/sucursal/add

http://localhost:9000/sucursal/update

http://localhost:9000/sucursal/delete/{id}

http://localhost:9000/sucursal/getOne/{id}

http://localhost:9000/sucursal/getAll

 

Como puedes ver, en el archivo application.properties, deberás configurar que el puerto a utilizar sea el 9000.

La vista deberá estar desarrollada con Thymeleaf.

Para que sea más atractiva, puedes usar opcionalmente alguna librería CSS que te lo facilite, como bootstrap, tailwind, material, etc.

  Muy Importante

Además del enlace a Git de la tarea resuelta, deberás incluir al menos dos enlaces, distintos de los recursos que te hemos proporcionado en el campus, que te hayan servido o hubiesen podido hacerlo, para resolver la totalidad de la tarea o algunas partes.
