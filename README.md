Proyecto Final – Programación III

BancoAppWeb + Pruebas Automatizadas con Selenium

Este repositorio contiene el desarrollo completo del Proyecto Final de la asignatura Programación III (ITLA), compuesto por:
	1.	BancoAppWeb: aplicación web desarrollada en ASP.NET Core MVC.
	2.	BancoAppWeb_SeleniumTests: suite de pruebas automatizadas con Java, Selenium WebDriver y TestNG.
	3.	Planificación del proyecto utilizando la metodología Scrum en Jira.
	4.	Documentación técnica, plan de pruebas, capturas y entregables requeridos por el profesor.

El objetivo general es implementar un sistema funcional y validarlo mediante pruebas manuales y automatizadas, aplicando buenas prácticas de ingeniería de software y control de calidad.

⸻

1. Descripción General

BancoAppWeb es una aplicación web que simula funcionalidades básicas de un sistema bancario. El usuario puede:
	•	Autenticarse de forma segura.
	•	Registrar, editar, listar, filtrar y eliminar clientes.
	•	Registrar tarjetas de crédito asociadas a clientes.

En paralelo, se desarrolló un proyecto independiente de pruebas automatizadas utilizando Selenium WebDriver, con casos alineados a las historias de usuario definidas en Jira.

⸻

2. Tecnologías Utilizadas

Backend / Aplicación Web
	•	ASP.NET Core MVC
	•	C#
	•	Entity Framework Core
	•	SQLite / SQL Server
	•	Identity para autenticación de usuarios

Automatización de Pruebas
	•	Java 17
	•	Selenium WebDriver
	•	TestNG
	•	Maven
	•	Page Object Model (POM)

Gestión Scrum
	•	Jira Software
	•	Sprint backlog
	•	Historias de usuario
	•	Tablero Kanban
	•	Burndown Chart

⸻

3. Funcionalidades Principales
	•	Inicio de sesión con validaciones completas.
	•	CRUD de clientes con validaciones de negocio.
	•	Búsqueda y filtros por nombre, cédula y estado.
	•	Registro de tarjetas de crédito con requisitos de formato.
	•	Validación de campos obligatorios y numéricos.
	•	Pruebas automatizadas end-to-end alineadas al Sprint 0.

⸻

4. Estructura del Repositorio

ProyectoFinal_P3/
│
├── BancoAppWeb/                     
│   ├── Controllers/
│   ├── Services/
│   ├── Models/
│   ├── Views/
│   ├── wwwroot/
│   └── appsettings.json
│
├── BancoAppWeb_SeleniumTests/       
│   ├── src/test/java/pages/
│   ├── src/test/java/tests/
│   ├── src/test/resources/TestSuite.xml
│   ├── reports/TestReport.html
│   └── reports/screenshots/
│
└── ProyectoFinal_P3.docx            


⸻

5. Datos Importantes

Dirección por defecto: http://localhost:5243/

Usuario semilla (solo en Development):
	•	Correo: pedrodavid@hotmail.com
	•	Contraseña: DevSecure!123

⸻

6. Ejecución de Pruebas Automatizadas

Desde BancoAppWeb_SeleniumTests:
	1.	Ejecute BancoAppWeb:

dotnet run

	2.	Ejecute la suite de pruebas:

mvn -Dsurefire.suiteXmlFiles=src/test/resources/TestSuite.xml test

	3.	Ubicación de reportes:

	•	reports/TestReport.html
	•	reports/screenshots/

⸻

7. Metodología Scrum

El proyecto fue gestionado mediante Scrum utilizando Jira, con:
	•	Cuatro épicas principales.
	•	Quince historias de usuario (HU01–HU15).
	•	Sprint backlog del Sprint 0.
	•	Tablero Kanban con estados To Do, In Progress, In Review y Done.
	•	Burndown Chart del sprint.

Todas las evidencias se encuentran en el documento final adjunto.

⸻

8. Pruebas Implementadas

La suite de pruebas automatizadas incluye:

Historia	Prueba Automatizada	                   Archivo
HU01	    Login exitoso	                       LoginTest.java
HU02	    Registro de cliente	                   ClientesTest.java
HU07	    Validación de campos vacíos	           ValidacionesTest.java
HU08	    Validación de formato de correo	       ValidacionesTest.java
HU09	    Búsqueda por nombre	                   ClientesTest.java
HU13	    Validación de campos numéricos	       ValidacionesTest.java
HU15	    Ejecución de suite unificada	       TestSuite.xml


⸻

9. Documentación Incluida

El repositorio incluye:
	•	Documento ProyectoFinal_P3.docx con:
	•	Épicas y HU.
	•	Sprint backlog y tablero Scrum.
	•	Burndown chart.
	•	Plan de pruebas.
	•	Casos manuales y automatizados.
	•	Evidencias de Jira, GitHub, VS Code y Selenium.
	•	Reportes HTML y capturas de pantallas de pruebas.
	•	Código del sistema y de las pruebas automatizadas.

⸻

11. Autor

Luis Emilio Cedano Martínez
Matrícula: 2024-0128
Instituto Tecnológico de las Américas (ITLA)

⸻

12. Accesos del Profesor

Se otorgó acceso a:
- ktejada@itla.edu.do
- 20186927@itla.edu.do
