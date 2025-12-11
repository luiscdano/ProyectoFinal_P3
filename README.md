# ProyectoFinal_P3 - BancoAppWeb

## Descripción General
BancoAppWeb es una aplicación web que simula un módulo básico de banca digital.  
El sistema permite autenticación de usuarios, gestión de clientes (crear, listar, editar, eliminar), registro de tarjetas, validaciones de datos y pruebas automatizadas con Selenium.

Este proyecto fue desarrollado como entrega final de la asignatura Programación III en el Instituto Tecnológico de las Américas (ITLA), aplicando la metodología Agile-Scrum.

---

## Tecnologías Utilizadas
**Backend / Web**
- ASP.NET Core MVC  
- Entity Framework Core  
- SQLite  

**Frontend**
- HTML5  
- CSS  
- Bootstrap  

**Automatización de Pruebas**
- Java 17  
- Selenium WebDriver  
- TestNG  
- Maven  

**Gestión y Control de Versiones**
- Jira Software  
- GitHub  
- Visual Studio Code  

---

## Objetivo del Proyecto
Desarrollar un sistema web funcional acompañado de un conjunto de pruebas automatizadas profesionales, aplicando correctamente la metodología Scrum y asegurando calidad mediante QA manual y automatizado.

---

## Alcance
**Incluye:**
- Login de usuarios  
- CRUD de clientes  
- Registro de tarjetas  
- Validaciones de datos  
- Suite completa de pruebas automatizadas con Selenium  

**No incluye:**
- Pagos reales  
- Transferencias reales  

---

## Cronograma de Trabajo
| Actividad              | Fecha        | Responsable   |
|-------------------------|-------------|---------------|
| Requerimientos          | 29-30 nov   | Luis Cedano   |
| Configuración repos     | 30 nov      | Luis Cedano   |
| Desarrollo web          | 1-5 dic     | Luis Cedano   |
| QA manual               | 3-6 dic     | Luis Cedano   |
| Selenium Tests          | 5-8 dic     | Luis Cedano   |
| Evidencias              | 9-10 dic    | Luis Cedano   |
| Documento final         | 10 dic      | Luis Cedano   |

---

## Primer Release
La primera versión del sistema incluye:
- Login de usuarios  
- CRUD de clientes  
- Validaciones principales  
- Registro de tarjetas  
- Suite Selenium completa  
- Evidencias de ejecución
  
---

## Metodología Scrum
**Equipo de Trabajo**
- Product Owner: Luis Cedano  
- Scrum Master: Luis Cedano  
- Developer: Luis Cedano  
- QA Engineer: Luis Cedano  

**Épicas**
- EPIC-01: Autenticación  
- EPIC-02: Gestión de clientes  
- EPIC-03: Registro de tarjetas  
- EPIC-04: Pruebas automatizadas Selenium  

**Ceremonias**
- Sprint Planning: 29 de noviembre  
- Daily Scrum: 1 al 10 de diciembre (9:00 AM)  
- Sprint Review: 8 de diciembre  
- Sprint Retrospective: 10 de diciembre (2:00 PM)  

---

## Historias de Usuario
Se definieron 15 historias de usuario, cada una con criterios de aceptación, criterios de rechazo y estimación en puntos de historia.  
Ejemplos:
- HU01: Inicio de sesión exitoso  
- HU02: Registrar nuevo cliente  
- HU05: Eliminar un cliente  
- HU08: Validación de formato de correo electrónico  
- HU15: Ejecutar todas las pruebas automatizadas desde una suite unificada  

---

## Plan de Pruebas
**Requerimientos probados:**
- RF01: Autenticación  
- RF02: Registro de clientes  
- RF03: Edición y eliminación  
- RF04: Búsqueda y filtrado  
- RF05: Registro de tarjetas  
- RF06: Validaciones  
- RF07: Automatización Selenium  

**Requerimientos no funcionales:**
- RNF01: Seguridad básica  
- RNF02: Usabilidad  
- RNF03: Mantenibilidad  
- RNF04: Evidencia automatizada  

**Herramientas de Pruebas**
- Selenium WebDriver  
- TestNG  
- Maven  

**Automatización**
- Ejecución completa mediante `mvn -Dsurefire.suiteXmlFiles=src/test/resources/TestSuite.xml test`  
- Reportes HTML y capturas automáticas generadas en cada ejecución

### Estucturas
**BancoAppWeb (Aplicación Web)**

BancoAppWeb/
│
├── Program.cs
├── appsettings.json
├── appsettings.Development.json
│
├── Data/
│   └── ApplicationDbContext.cs
│
├── Migrations/
│   └── (...archivos Identity + Clientes + Productos...)
│
├── Models/
│   ├── Cliente.cs
│   ├── Producto.cs
│   ├── Divisa.cs
│   └── Usuario.cs
│
├── Services/
│   ├── IClienteService.cs
│   ├── ClienteService.cs
│   ├── DatabaseSeeder.cs
│   └── DivisaService.cs
│
├── Controllers/
│   ├── ClientesController.cs
│   ├── ProductosController.cs
│   ├── DivisasController.cs
│   ├── HomeController.cs
│   └── SimuladorController.cs
│
├── ViewModels/
│   └── ClienteFormViewModel.cs
│
├── Views/
│   ├── Shared/
│   │   └── _Layout.cshtml
│   │
│   ├── Home/
│   │   ├── Index.cshtml
│   │   ├── Privacy.cshtml
│   │   ├── Security.cshtml
│   │   └── FAQ.cshtml
│   │
│   ├── Clientes/
│   │   ├── Index.cshtml
│   │   ├── Create.cshtml
│   │   ├── Edit.cshtml
│   │   └── Delete.cshtml
│   │
│   ├── Productos/
│   │   └── Index.cshtml
│   │
│   ├── Divisas/
│   │   ├── Index.cshtml
│   │   └── (usa wwwroot/js/divisas.js y wwwroot/css/divisas-cards.css)
│   │
│   └── Simulador/
│       ├── Index.cshtml
│       └── Resultado.cshtml
│
├── Areas/
│   └── Identity/
│       └── Pages/
│           └── Account/
│               ├── Login.cshtml
│               ├── Register.cshtml
│               └── (...otros scaffolds...)
│
└── wwwroot/
    ├── css/
    ├── js/
    └── images/
	
**BancoAppWeb_SeleniumTests (Pruebas Automatizadas)**

BancoAppWeb_SeleniumTests/
│
├── pom.xml
│
├── reports/
│   ├── TestReport.html
│   └── screenshots/
│       └── index.html
│       └── (...capturas...)
│
└── src/
    └── test/
        ├── java/
        │   ├── pages/
        │   │   ├── BasePage.java
        │   │   ├── LoginPage.java
        │   │   ├── RegisterPage.java
        │   │   ├── RegistrarUsuarioPage.java
        │   │   ├── RegistrarClientePage.java
        │   │   ├── ListarClientesPage.java
        │   │   ├── EditClientePage.java
        │   │   └── DeleteClientePage.java
        │   │
        │   └── tests/
        │       ├── BaseTest.java
        │       ├── LoginTest.java
        │       ├── ErrorLoginTest.java
        │       ├── RegistrarUsuarioTest.java
        │       ├── RegistrarClienteTest.java
        │       ├── ListarClientesTest.java
        │       ├── EditarClienteTest.java
        │       └── EliminarClienteTest.java
        │
        ├── utils/
        │   ├── ReportManager.java
        │   ├── ScreenshotUtils.java
        │
        ├── listeners/
        │   ├── ReportListener.java
        │   └── ScreenshotListener.java
        │
        └── resources/
            └── TestSuite.xml

---

## Entregables
- Documento PDF con todos los puntos requeridos  
- Repositorio de código: [GitHub - ProyectoFinal_P3](https://github.com/luiscdano/ProyectoFinal_P3)  
- Herramienta de gestión: [Jira - SCRUM Board](https://luiscdano.atlassian.net/jira/software/projects/SCRUM/boards/1)  
- Código de pruebas automatizadas en Java + Selenium  

---

## Conclusión
BancoAppWeb cumple con los objetivos planteados en la asignatura, demostrando la aplicación práctica de la metodología Scrum, el desarrollo de un sistema web funcional y la implementación de pruebas automatizadas.  
Este proyecto refleja un ciclo completo de planificación, desarrollo, validación y documentación, alineado con los estándares académicos y profesionales.

---

## Autor
**Luis Emilio Cedano Martínez**  
Matrícula: 2024.0128  
Instituto Tecnológico de las Américas (ITLA)  
Profesor: Kelyn Tejada Belliard  
Fecha: 10 de diciembre de 2025

---

## Accesos solo otorgado a:

- ktejada@itla.edu.do
- 20186927@itla.edu.do
