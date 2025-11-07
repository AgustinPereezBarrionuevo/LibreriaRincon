# 📚 Librería Rincón

Sistema de gestión de una librería desarrollado con **C#**, **.NET** y **Entity Framework Core**, siguiendo una arquitectura en capas.  
El proyecto incluye dos aplicaciones principales:

- **LibreriaApi** → API REST desarrollada con .NET y Entity Framework Core.
- **LibreriaDesktop** → Aplicación de escritorio (Windows Forms) que consume la API.

---

## 🚀 Funcionalidades principales

### 🖥️ Aplicación de escritorio (LibreriaDesktop)
- Listado de libros con su información (título, autor, precio, stock, etc.).
- Alta, baja y modificación de libros.
- Registro de préstamos con fecha de devolución.
- Cálculo de intereses por mora.
- Interfaz sencilla e intuitiva para el operador.

### 🌐 API REST (LibreriaApi)
- CRUD completo de libros y préstamos.
- Lógica de negocio y validaciones centralizadas.
- Persistencia con **Entity Framework Core** y base de datos **SQL Server**.
- Documentación con **Swagger UI** para probar los endpoints fácilmente.

---

## 🧩 Estructura del repositorio

📂 LibreriaRincon
├── 📁 LibreriaApi
│ ├── Controllers/
│ ├── Models/
│ ├── Services/
│ ├── Data/
│ └── Program.cs
│
├── 📁 LibreriaDesktop
│ ├── Forms/
│ ├── Controllers/
│ ├── Services/
│ └── Program.cs
│
├── 📄 LibreriaRincon.sln
└── 📄 README.md

---

## ⚙️ Requisitos

- [Visual Studio 2022](https://visualstudio.microsoft.com/es/)
- [.NET 8 SDK o superior](https://dotnet.microsoft.com/en-us/download)
- [SQL Server](https://www.microsoft.com/es-es/sql-server/sql-server-downloads) o [SQL Server Express](https://www.microsoft.com/es-es/sql-server/sql-server-editions-express)
- Entity Framework Core Tools (`dotnet ef`)

---

## 🛠️ Cómo ejecutar el proyecto

### 1️⃣ Clonar el repositorio

```bash
git clone https://github.com/<TU_USUARIO>/LibreriaRincon.git
cd LibreriaRincon
2️⃣ Ejecutar la API
Abrí Visual Studio.

Establecé LibreriaApi como proyecto de inicio.

Presioná F5 o clic en ▶️ “Ejecutar”.

Se abrirá Swagger UI en tu navegador (por ejemplo: https://localhost:5001/swagger).

Desde ahí podés probar los endpoints:

GET /api/libros

POST /api/libros

PUT /api/libros/{id}

DELETE /api/libros/{id}

POST /api/prestamos etc.

3️⃣ Ejecutar la aplicación de escritorio
Establecé LibreriaDesktop como proyecto de inicio.

Asegurate de que la API esté corriendo (no cierres Swagger).

Presioná F5.

La aplicación se conectará automáticamente a la API (por la URL configurada en el código).

🧠 Notas técnicas
Arquitectura en capas: Controladores → Servicios → Repositorio → Base de datos

Patrón SOLID aplicado.

Base de datos generada automáticamente al ejecutar la API por primera vez (gracias a EF Migrations).

Incluye validaciones de negocio en la capa de servicio.

🧰 Tecnologías utilizadas
Tecnología	Uso
C# (.NET 8)	Lenguaje principal
Windows Forms	Interfaz de usuario
ASP.NET Core Minimal API	Backend REST
Entity Framework Core	ORM para base de datos
SQL Server	Persistencia
Swagger	Pruebas de endpoints
Git / GitHub	Control de versiones


👨‍💻 Autor

Agustín Pérez 
Proyecto académico desarrollado con fines educativos.
📧 Contacto: agustin_0100@hotmail.com
💻 GitHub: https://github.com/AgustinPereezBarrionuevo