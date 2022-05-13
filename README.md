# bootcamp_final
Propio: Marisol Perez Lima

Proyecto.
Avances de las primeras 3 versiones hecho con Mauricio Ccasani.

Instrucciones de uso:
- Levantar los servicios del repositorio con la siguiente instruccion
mvn spring-boot:run con el siguiente orden:

1. Config-server
2. Registry-service
3. Gateway-service
4. Type Product
5. Customer
6. Type Customer
7. Product
8. Admin

Rutas para pruebas con Postman, los ids de las tablas se generan automáticamente en MongoDB:

Agregar nuevo cliente:
http://localhost:8882/customers		POST
Ingresar el sgte json:
{
    "name": "Mary",
    "surname": "Perez"
}

Listar clientes:
http://localhost:8882/customers/	GET

Buscar cliente por id:
http://localhost:8882/customers/{id}	GET

Borrar cliente:
http://localhost:8882/customers/{id}	DELETE

_____________________________________________________

Agregar nuevo tipo cliente:
http://localhost:8882/type-customers/	POST
Ingresar el sgte json:
{
    "description": "personal",
    "status": "activo",
    "idCustomer": "idCustomer"
}

Listar tipo clientes:
http://localhost:8882/type-customers/	GET

_______________________________________________________

Agregar nuevo tipo producto:
http://localhost:8882/type-products		POST
Ingresar el sgte json:
{
    "type": "pasivo",
	"account": "ahorro",
	"status": true
}

Listar tipo producto:
http://localhost:8882/type-products/	GET

Buscar tipo producto por id:
http://localhost:8882/type-products/{id}	GET

Borrar tipo producto:
http://localhost:8882/type-products/{id}	DELETE

___________________________________________________________

Agregar nuevo producto:
http://localhost:8882/products		POST
Ingresar el sgte json:
{
    "commission": 0.0,
	"numberOfMovements": 0,
	"numberOfCredit": 0,
	"amount": 236.0,
	"limitCredit": 0,
	"action": "deposito",
	"idTypeProduct": "627d1fa06c9d6749358be8a0",
	"idCustomer": "627d1cc726b7d84bbc5c2c3f"
}

Listar producto:
http://localhost:8882/products/	GET

Buscar producto por id:
http://localhost:8882/products/{id}	GET

Borrar producto:
http://localhost:8882/products/{id}	DELETE

________________________________________________________________

Operaciones en general:

Consultar saldo:
http://localhost:8882/servicios/saldo/{id_producto}	GET

Hacer operaciones de retiro, depósito, etc:
http://localhost:8882/servicios/	POST
Ingresar el sgte json:
{
	"id": "id_prroducto",
    "amount":50.0,
    "action": "retiro"
}
