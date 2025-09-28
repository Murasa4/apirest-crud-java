# APIREST para practicar un CRUD

Una API REST simple para gestión de **productos**, creada solamente de práctica para spring boot.

---

## 🛠 Tecnologías usadas

- **Java**  
- **Spring Boot**  
- **Docker**  
- **PostgreSQL (imagen)**  
- **Visual Studio Code**  
- **Postman**  
- **Hibernate**  

---

## 🚀 Instalación y ejecución

1. Clonar el repositorio:  
   ```bash
   git clone https://github.com/Murasa4/apirest-crud-java.git
   cd apirest-crud-java
Crear un archivo .env con las credenciales de la base de datos:

```postgresql
SPRING_DATASOURCE_URL=jdbc:postgresql://localhost:5432/bd

SPRING_DATASOURCE_USERNAME=admin

SPRING_DATASOURCE_PASSWORD=admin

SPRING_DATASOURCE_DB=bd
```
Levantar la base de datos con Docker Compose:

```bash
docker-compose up -d
```
Ejecutar la API desde Spring Boot:

```bash
./mvnw spring-boot:run
```
La API estará disponible en http://localhost:8080.

📚 Endpoints principales
Listar todos los productos
URL: /productos

Método: GET
```json

[
  {
    "id": 1,
    "nombre": "Producto1",
    "precio": 100.0
  },
  {
    "id": 2,
    "nombre": "Producto2",
    "precio": 150.0
  }
]
```
Obtener un producto por ID
```json
URL: /productos/{id}
```
Método: GET


```json
{
  "id": 1,
  "nombre": "Producto1",
  "precio": 100.0
}
```
Crear un nuevo producto
```bash
URL: /productos
```

Método: POST
```json

{
  "nombre": "Producto3",
  "precio": 200.0
}
```

```json
{
  "id": 3,
  "nombre": "Producto3",
  "precio": 200.0
}
```
Estructura del proyecto
```bash
apirest-practica/
├── src/
│   ├── main/java/com/tuusuario/apirest/
│   └── main/resources/
├── docker-compose.yml
├── .env
├── pom.xml
└── README.md
```






