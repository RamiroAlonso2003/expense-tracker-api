# expense-tracker-api
Expense Tracker UI:
![image](https://github.com/user-attachments/assets/538c80f0-bd88-4db8-896e-6f9a1e48d292)

Envía solicitudes como Sign-up, Log-in y otras operaciones relacionadas con el manejo de gastos.
Se comunica con la API a través de solicitudes HTTP.
Expenses API:

Maneja las solicitudes provenientes de la interfaz de usuario.
Implementa autenticación usando JWT para validar las operaciones.
Se conecta a la base de datos para realizar operaciones CRUD.
Database:

Contiene dos tablas principales: Users y Tasks (en este caso, podrían ser Expenses).
Responde con datos estructurados en JSON hacia la API.
Este esquema es totalmente compatible con un desarrollo usando Go. Podrías implementar el flujo así:

Autenticación JWT:

La API valida cada solicitud asegurándose de que el cliente incluya un JWT válido en los encabezados (Authorization: Bearer token).
Rutas CRUD:

/signup: Crear un nuevo usuario en la tabla Users.
/login: Validar credenciales y devolver un JWT.
/expenses:
POST: Agregar un nuevo gasto.
GET: Listar o filtrar gastos.
PUT: Actualizar un gasto existente.
DELETE: Eliminar un gasto.
Base de datos:

Definir tablas para usuarios y gastos, con relaciones (user_id en la tabla de gastos).

comando Docker: docker run --name some-postgres -e POSTGRES_USER=fazt -e POSTGRES_PASSWORD=mysecretpassword -p 5432:5432 -d postgr