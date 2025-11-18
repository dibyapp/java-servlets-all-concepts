# ☕ Java Servlets - Complete Concepts Tutorial

<div align="center">

![Java Servlets](https://img.shields.io/badge/Servlet%20API-4.0-blue?logo=oracle)
![Java](https://img.shields.io/badge/Java-SE%208-orange?logo=java)
![Tomcat](https://img.shields.io/badge/Tomcat-9.0-yellow?logo=apachetomcat)
![JDBC](https://img.shields.io/badge/JDBC-Oracle-red?logo=oracle)
![License](https://img.shields.io/badge/License-MIT-blue)
![Contributions](https://img.shields.io/badge/Contributions-Welcome-success)

**Master Java Servlets with 26+ hands-on projects covering every concept from basics to advanced patterns**

*From your first servlet to production-ready web applications with MVC architecture, session management, and event listeners*

[Getting Started](#-getting-started) • [Project Catalog](#-project-catalog) • [Learning Path](#-learning-path) • [Contributing](#-contributing)

</div>

---

## 📖 Table of Contents

- [About This Repository](#-about-this-repository)
- [Why This Repository?](#-why-this-repository)
- [What You'll Learn](#-what-youll-learn)
- [Prerequisites](#-prerequisites)
- [Getting Started](#-getting-started)
- [Project Catalog](#-project-catalog)
  - [Database Operations](#1-database-operations)
  - [Configuration & Context](#2-configuration--context)
  - [Request Handling](#3-request-handling)
  - [Session Management](#4-session-management)
  - [Scope & Attributes](#5-scope--attributes)
  - [File Operations](#6-file-operations)
  - [Event Listeners](#7-event-listeners)
  - [Advanced Patterns](#8-advanced-patterns)
- [Learning Path](#-learning-path)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Configuration Approaches](#-configuration-approaches)
- [Contributing](#-contributing)
- [Author](#-author)
- [License](#-license)

---

## 🎯 About This Repository

This repository is a **comprehensive hands-on guide to Java Servlets** featuring **26+ independent projects** that demonstrate every essential servlet concept. Each project is self-contained and focuses on one specific concept, making it perfect for step-by-step learning and reference.

### 🎓 Perfect For:

- **Students** learning Java web development fundamentals
- **Developers** preparing for Java EE certification exams
- **Backend Engineers** transitioning to Java web technologies
- **Interview Preparation** - covers common servlet interview questions
- **Teams** looking for servlet best practices and patterns
- **Anyone** building the foundation for Spring MVC or Jakarta EE

---

## 💡 Why This Repository?

### ✨ What Makes This Special?

| Feature | Description |
|---------|-------------|
| 🎯 **One Concept Per Project** | Each project isolates a single concept for crystal-clear learning |
| 🔄 **Multiple Approaches** | XML config, Annotations, and Programmatic configuration |
| 🏗️ **Production Patterns** | MVC, DAO, DTO/VO patterns with layered architecture |
| 📚 **Complete Coverage** | 26+ projects covering Servlet API 4.0 features |
| 🧩 **Real-World Examples** | GST calculator, employee management, file upload/download |
| 🚀 **Modern Standards** | Servlet 4.0, Java 8, annotation-driven development |
| 💼 **Enterprise Ready** | Connection pooling, listeners, cross-context communication |
| 📖 **Beginner Friendly** | Progressive learning from basic to advanced concepts |

---

## 📚 What You'll Learn

<details open>
<summary><b>Core Servlet Fundamentals</b></summary>

- ✅ HttpServlet lifecycle (init, service, destroy)
- ✅ HttpServletRequest and HttpServletResponse
- ✅ GET and POST request handling
- ✅ ServletConfig (servlet-specific initialization)
- ✅ ServletContext (application-wide context)
- ✅ RequestDispatcher (forward and include)
- ✅ SendRedirect for client-side redirection
- ✅ Content types and response headers
- ✅ PrintWriter for output generation
</details>

<details open>
<summary><b>Session Management Techniques</b></summary>

- ✅ HttpSession API
- ✅ Cookies (creation, retrieval, deletion)
- ✅ URL Rewriting (session tracking without cookies)
- ✅ Hidden Form Fields
- ✅ Session timeout configuration
- ✅ Session attribute management
- ✅ Comparing all session tracking techniques
</details>

<details open>
<summary><b>Advanced Servlet Features</b></summary>

- ✅ Event Listeners (ServletContextListener, HttpSessionListener, ServletRequestListener)
- ✅ Cross-Context Communication (getContext, getRequestDispatcher)
- ✅ Dynamic Servlet Registration (programmatic approach)
- ✅ Resource Injection with @Resource
- ✅ Annotation-based configuration (@WebServlet, @WebListener)
- ✅ Thread safety considerations (SingleThreadModel)
- ✅ ServletContainerInitializer
- ✅ File upload and download
</details>

<details open>
<summary><b>Database Integration</b></summary>

- ✅ JDBC with Servlets
- ✅ Connection pooling with DataSource
- ✅ PreparedStatement for SQL injection prevention
- ✅ ResultSet processing
- ✅ Database operations (CRUD)
- ✅ DAO pattern implementation
- ✅ Response downloading (export to files)
</details>

<details open>
<summary><b>Design Patterns & Architecture</b></summary>

- ✅ MVC Pattern (Model-View-Controller)
- ✅ DAO Pattern (Data Access Object)
- ✅ DTO/VO Pattern (Data Transfer Objects)
- ✅ Front Controller Pattern
- ✅ Layered Architecture (Presentation → Service → DAO → Database)
- ✅ Service Locator Pattern
</details>

---

## 🔧 Prerequisites

Before you begin, ensure you have:

- ☕ **Java JDK 8** or higher
- 🌐 **Apache Tomcat 9.0** or any Servlet 4.0+ compatible server
- 🛠️ **Eclipse IDE for Java EE Developers** (recommended) or IntelliJ IDEA
- 🗄️ **Oracle Database** (11g XE or higher) for database examples
- 📖 Basic understanding of:
  - Java programming (OOP, collections, exceptions)
  - HTML forms and HTTP protocol
  - SQL and relational databases

---

## 🚀 Getting Started

### Quick Start

```bash
# Clone the repository
git clone https://github.com/dibyapp/java-servlets-all-concepts.git

# Import into Eclipse
File → Import → Existing Projects into Workspace
Select the cloned directory

# Configure Tomcat in Eclipse
Window → Preferences → Server → Runtime Environments
Add Apache Tomcat 9.0

# Run a project
Right-click project → Run As → Run on Server
Select Tomcat 9.0 → Finish
```

### Running Individual Projects

Each project is a standalone web application:

1. **Import** the project into Eclipse
2. **Configure** Oracle Database connection (if required)
   - Update JDBC URL, username, password in servlet code
3. **Deploy** to Tomcat server
4. **Access** via browser at `http://localhost:8080/ProjectName`

### Database Setup (For JDBC Projects)

```sql
-- Create a sample employee table
CREATE TABLE employees (
    emp_id NUMBER PRIMARY KEY,
    emp_name VARCHAR2(50),
    emp_salary NUMBER(10,2),
    emp_dept VARCHAR2(30)
);

-- Insert sample data
INSERT INTO employees VALUES (101, 'John Doe', 50000, 'IT');
INSERT INTO employees VALUES (102, 'Jane Smith', 60000, 'HR');
COMMIT;
```

---

## 📁 Project Catalog

### 1️⃣ Database Operations

Master JDBC integration with servlets.

| Project | Concept | Key Learning |
|---------|---------|-------------|
| `DatabaseApp` | Basic JDBC operations | Connecting to DB, executing queries |
| `DatabaseApp-AnnotationDriven` | @WebServlet configuration | Annotation-based servlet mapping |
| `DatabaseApp-Annotations-Resource` | @Resource injection | DataSource injection for connection pooling |
| `DatabaseApp-ServletConfig` | ServletConfig parameters | Servlet-specific initialization params |
| `DatabaseApp-ServletConext` | ServletContext parameters | Application-wide configuration |
| `DatabaseApp-ResponseDownloading` | Export to file | Download query results as MS Word document |

**💡 Key Learning:** Integrate databases with servlets using JDBC and connection pooling for production applications.

**Example: Basic Database Query**
```java
@WebServlet("/employees")
public class EmployeeServlet extends HttpServlet {

    protected void doGet(HttpServletRequest request,
                        HttpServletResponse response)
                        throws ServletException, IOException {

        response.setContentType("text/html");
        PrintWriter out = response.getWriter();

        try {
            Class.forName("oracle.jdbc.driver.OracleDriver");
            Connection con = DriverManager.getConnection(
                "jdbc:oracle:thin:@localhost:1521:xe", "system", "password");

            Statement stmt = con.createStatement();
            ResultSet rs = stmt.executeQuery("SELECT * FROM employees");

            out.println("<table border='1'>");
            while(rs.next()) {
                out.println("<tr>");
                out.println("<td>" + rs.getInt(1) + "</td>");
                out.println("<td>" + rs.getString(2) + "</td>");
                out.println("</tr>");
            }
            out.println("</table>");

            con.close();
        } catch(Exception e) {
            out.println("Error: " + e.getMessage());
        }
    }
}
```

---

### 2️⃣ Configuration & Context

Learn servlet configuration and context management.

| Project | Concept | Use Case |
|---------|---------|----------|
| `DatabaseApp-ServletConfig` | ServletConfig | Servlet-level init parameters (DB URL, driver) |
| `DatabaseApp-ServletConext` | ServletContext | Application-level shared data |

**💡 Key Learning:** Use ServletConfig for servlet-specific settings and ServletContext for application-wide resources.

**ServletConfig Example:**
```xml
<!-- web.xml -->
<servlet>
    <servlet-name>DBServlet</servlet-name>
    <servlet-class>com.dib.servlet.DatabaseServlet</servlet-class>
    <init-param>
        <param-name>driver</param-name>
        <param-value>oracle.jdbc.driver.OracleDriver</param-value>
    </init-param>
    <init-param>
        <param-name>url</param-name>
        <param-value>jdbc:oracle:thin:@localhost:1521:xe</param-value>
    </init-param>
</servlet>
```

```java
public void init(ServletConfig config) throws ServletException {
    String driver = config.getInitParameter("driver");
    String url = config.getInitParameter("url");
    // Use configuration
}
```

**ServletContext Example:**
```java
// Store application-wide data
ServletContext context = getServletContext();
context.setAttribute("hitCount", 0);

// Access from any servlet
Integer hitCount = (Integer) context.getAttribute("hitCount");
```

---

### 3️⃣ Request Handling

Master request dispatching and redirection.

| Project | Technique | Behavior |
|---------|-----------|----------|
| `DatabaseApp-RequestDispatcher-Forward` | forward() | Server-side, same request object |
| `DatabaseApp-RequestDispatcher-Include` | include() | Includes response, continues processing |
| `SendRedirection-SendRedirect` | sendRedirect() | Client-side, new request |
| `SendRedirection-UsingLinks` | Hyperlinks | Navigation via HTML links |
| `Application-DynamicForm` | Dynamic forms | Generate forms based on user input |

**💡 Key Learning:** Understand when to use forward, include, or redirect for optimal application flow.

**The Difference:**

| Feature | forward() | include() | sendRedirect() |
|---------|-----------|-----------|----------------|
| **Location** | Server-side | Server-side | Client-side |
| **Request Object** | Same | Same | New |
| **URL in Browser** | Unchanged | Unchanged | Changes |
| **Use Case** | MVC pattern | Headers/footers | After POST (PRG) |
| **Speed** | Fast | Fast | Slower (2 requests) |

**Forward Example:**
```java
@WebServlet("/controller")
public class ControllerServlet extends HttpServlet {
    protected void doGet(HttpServletRequest request,
                        HttpServletResponse response)
                        throws ServletException, IOException {

        // Process data
        List<Employee> employees = employeeService.getAll();
        request.setAttribute("employees", employees);

        // Forward to view
        RequestDispatcher rd = request.getRequestDispatcher("/view.jsp");
        rd.forward(request, response);
    }
}
```

**Redirect Example:**
```java
@WebServlet("/save")
public class SaveServlet extends HttpServlet {
    protected void doPost(HttpServletRequest request,
                         HttpServletResponse response)
                         throws ServletException, IOException {

        // Save data
        employeeService.save(employee);

        // Redirect to prevent double submission
        response.sendRedirect("success.html");
    }
}
```

---

### 4️⃣ Session Management

Master all session tracking techniques.

| Project | Technique | When to Use |
|---------|-----------|-------------|
| `SessionTracking-HttpSession & Cookies` | HttpSession + Cookies | Standard session management |
| `SessionTracking-HttpSession & URL Rewriting` | URL Rewriting | When cookies are disabled |
| `Cookie-Application-SessionTracking` | Cookies only | Simple data persistence |
| `SessionTracking-Using-HiddenFormFields` | Hidden fields | Multi-step forms |

**💡 Key Learning:** Choose the right session tracking technique based on requirements and browser support.

**HttpSession Example:**
```java
@WebServlet("/login")
public class LoginServlet extends HttpServlet {
    protected void doPost(HttpServletRequest request,
                         HttpServletResponse response)
                         throws ServletException, IOException {

        String username = request.getParameter("username");
        String password = request.getParameter("password");

        if(authenticate(username, password)) {
            // Create session
            HttpSession session = request.getSession();
            session.setAttribute("user", username);
            session.setMaxInactiveInterval(30 * 60); // 30 minutes

            response.sendRedirect("dashboard");
        } else {
            response.sendRedirect("login.html?error=true");
        }
    }
}
```

**Cookie Example:**
```java
// Creating a cookie
Cookie userCookie = new Cookie("username", "john");
userCookie.setMaxAge(24 * 60 * 60); // 1 day
userCookie.setPath("/");
response.addCookie(userCookie);

// Reading cookies
Cookie[] cookies = request.getCookies();
if(cookies != null) {
    for(Cookie cookie : cookies) {
        if(cookie.getName().equals("username")) {
            String username = cookie.getValue();
        }
    }
}
```

**URL Rewriting Example:**
```java
// Encode URL with session ID
String encodedURL = response.encodeURL("dashboard");
out.println("<a href='" + encodedURL + "'>Dashboard</a>");

// Or for redirects
String encodedRedirectURL = response.encodeRedirectURL("dashboard");
response.sendRedirect(encodedRedirectURL);
```

---

### 5️⃣ Scope & Attributes

Understand servlet scopes and attribute sharing.

| Project | Scope | Lifespan | Use Case |
|---------|-------|----------|----------|
| `ServletAtributes-RequestScope` | Request | Single request-response cycle | Passing data to JSP |
| `ServletAtributes-SessionScope` | Session | User session | User-specific data |
| `ServletAtributes-ApplicationScope` | Application | Entire application | Shared counters, config |

**💡 Key Learning:** Choose the appropriate scope to minimize memory usage and ensure data isolation.

**Scope Comparison:**
```java
// REQUEST SCOPE - Lives for one request only
request.setAttribute("message", "Hello");
RequestDispatcher rd = request.getRequestDispatcher("view.jsp");
rd.forward(request, response); // 'message' available in view.jsp

// SESSION SCOPE - Lives across multiple requests for a user
HttpSession session = request.getSession();
session.setAttribute("cart", shoppingCart); // Available until session expires

// APPLICATION SCOPE - Lives for entire application
ServletContext context = getServletContext();
context.setAttribute("visitCount", 1000); // Shared by all users
```

---

### 6️⃣ File Operations

Handle file uploads and downloads.

| Project | Operation | Technology |
|---------|-----------|------------|
| `FileUploadApp - JavaZoomAPI` | File upload | JavaZoom Upload API |
| `ResourceDownloadApp` | File download | Response streaming |
| `DatabaseApp-ResponseDownloading` | Export results | Generate downloadable files |

**💡 Key Learning:** Implement secure file upload with validation and efficient file download with proper MIME types.

**File Upload Example:**
```java
@WebServlet("/upload")
@MultipartConfig(maxFileSize = 1024 * 1024 * 5) // 5MB max
public class FileUploadServlet extends HttpServlet {

    protected void doPost(HttpServletRequest request,
                         HttpServletResponse response)
                         throws ServletException, IOException {

        Part filePart = request.getPart("file");
        String fileName = filePart.getSubmittedFileName();

        // Validate file type
        if(!fileName.endsWith(".pdf") && !fileName.endsWith(".jpg")) {
            response.getWriter().println("Invalid file type!");
            return;
        }

        // Save file
        String uploadPath = getServletContext().getRealPath("") + "uploads";
        File uploadDir = new File(uploadPath);
        if(!uploadDir.exists()) uploadDir.mkdir();

        filePart.write(uploadPath + File.separator + fileName);

        response.getWriter().println("File uploaded successfully!");
    }
}
```

**File Download Example:**
```java
@WebServlet("/download")
public class DownloadServlet extends HttpServlet {

    protected void doGet(HttpServletRequest request,
                        HttpServletResponse response)
                        throws ServletException, IOException {

        String fileName = request.getParameter("file");
        String filePath = getServletContext().getRealPath("") + "files/" + fileName;

        File file = new File(filePath);

        // Set response headers
        response.setContentType("application/octet-stream");
        response.setHeader("Content-Disposition",
            "attachment; filename=\"" + fileName + "\"");
        response.setContentLengthLong(file.length());

        // Stream file
        try(FileInputStream in = new FileInputStream(file);
            OutputStream out = response.getOutputStream()) {

            byte[] buffer = new byte[4096];
            int bytesRead;
            while((bytesRead = in.read(buffer)) != -1) {
                out.write(buffer, 0, bytesRead);
            }
        }
    }
}
```

---

### 7️⃣ Event Listeners

Monitor application, session, and request lifecycle events.

| Project | Listener Type | Events Tracked |
|---------|--------------|----------------|
| `SessionTracking-Listeners` | ServletContextListener | Application startup/shutdown |
| `SessionTracking-Listeners` | HttpSessionListener | Session creation/destruction |
| `SessionTracking-Listeners` | ServletRequestListener | Request received/completed |

**💡 Key Learning:** Use listeners for resource initialization, performance monitoring, and cleanup operations.

**ServletContextListener Example:**
```java
@WebListener
public class AppInitializer implements ServletContextListener {

    @Override
    public void contextInitialized(ServletContextEvent sce) {
        System.out.println("Application started at: " + new Date());

        ServletContext context = sce.getServletContext();

        // Initialize database connection pool
        DataSource ds = createDataSource();
        context.setAttribute("dataSource", ds);

        // Load configuration
        Properties config = loadConfig();
        context.setAttribute("config", config);

        // Initialize counters
        context.setAttribute("visitorCount", 0);
    }

    @Override
    public void contextDestroyed(ServletContextEvent sce) {
        System.out.println("Application stopped at: " + new Date());

        // Cleanup resources
        DataSource ds = (DataSource) sce.getServletContext()
                                        .getAttribute("dataSource");
        closeDataSource(ds);
    }
}
```

**HttpSessionListener Example:**
```java
@WebListener
public class SessionMonitor implements HttpSessionListener {

    private static int activeSessions = 0;

    @Override
    public void sessionCreated(HttpSessionEvent se) {
        activeSessions++;
        System.out.println("Session created. Active sessions: " + activeSessions);

        // Set session timeout
        se.getSession().setMaxInactiveInterval(30 * 60); // 30 minutes
    }

    @Override
    public void sessionDestroyed(HttpSessionEvent se) {
        activeSessions--;
        System.out.println("Session destroyed. Active sessions: " + activeSessions);

        // Cleanup session data
        HttpSession session = se.getSession();
        // Perform cleanup operations
    }
}
```

**ServletRequestListener Example:**
```java
@WebListener
public class PerformanceMonitor implements ServletRequestListener {

    @Override
    public void requestInitialized(ServletRequestEvent sre) {
        long startTime = System.currentTimeMillis();
        sre.getServletRequest().setAttribute("startTime", startTime);

        System.out.println("Request received: " +
            ((HttpServletRequest)sre.getServletRequest()).getRequestURI());
    }

    @Override
    public void requestDestroyed(ServletRequestEvent sre) {
        long startTime = (Long) sre.getServletRequest()
                                    .getAttribute("startTime");
        long endTime = System.currentTimeMillis();
        long duration = endTime - startTime;

        System.out.println("Request completed in: " + duration + "ms");
    }
}
```

---

### 8️⃣ Advanced Patterns

Enterprise-grade patterns and architectures.

| Project | Pattern | Description |
|---------|---------|-------------|
| `LayeredApplication-EmployeeRegistration` | MVC + DAO | Complete layered architecture |
| `CentralGSTApp-CrossContextCommunication` | Cross-Context | Communication between web apps |
| `StateGSTApp-CrossContextCommunication` | Cross-Context | Inter-application data sharing |
| `DynamicRegistration-ProgrammaticApproach` | Dynamic Registration | Servlet 3.0+ programmatic config |
| `TestApp-ThreadSafety` | SingleThreadModel | Thread safety demonstration |

**💡 Key Learning:** Build production-ready applications with proper separation of concerns and enterprise patterns.

**Layered Architecture Example:**

```
LayeredApplication-EmployeeRegistration/
├── Presentation Layer (Servlets)
│   ├── ControllerServlet.java      # Front Controller
│   ├── RegisterServlet.java        # Registration handler
│   └── ListServlet.java            # Display employees
│
├── Service Layer
│   ├── EmployeeService.java        # Business logic interface
│   └── EmployeeServiceImpl.java    # Implementation
│
├── DAO Layer
│   ├── EmployeeDAO.java            # Data access interface
│   └── EmployeeDAOImpl.java        # JDBC implementation
│
├── DTO/VO Layer
│   ├── EmployeeDTO.java            # Data transfer object
│   ├── EmployeeVO.java             # Value object
│   └── EmployeeBO.java             # Business object
│
└── View Layer (HTML)
    ├── register.html
    └── list.html
```

**MVC Controller Example:**
```java
@WebServlet("/controller")
public class MainController extends HttpServlet {

    private EmployeeService service = new EmployeeServiceImpl();

    protected void doPost(HttpServletRequest request,
                         HttpServletResponse response)
                         throws ServletException, IOException {

        String action = request.getParameter("action");

        switch(action) {
            case "register":
                registerEmployee(request, response);
                break;
            case "list":
                listEmployees(request, response);
                break;
            case "delete":
                deleteEmployee(request, response);
                break;
            default:
                response.sendRedirect("index.html");
        }
    }

    private void registerEmployee(HttpServletRequest request,
                                  HttpServletResponse response)
                                  throws IOException {
        // Create DTO from request
        EmployeeDTO dto = new EmployeeDTO();
        dto.setName(request.getParameter("name"));
        dto.setSalary(Double.parseDouble(request.getParameter("salary")));
        dto.setDept(request.getParameter("dept"));

        // Call service layer
        String result = service.registerEmployee(dto);

        // Send response
        response.setContentType("text/html");
        response.getWriter().println("<h2>" + result + "</h2>");
    }
}
```

**Cross-Context Communication Example:**
```java
// CentralGSTApp
@WebServlet("/calculateGST")
public class CentralGSTServlet extends HttpServlet {
    protected void doGet(HttpServletRequest request,
                        HttpServletResponse response)
                        throws ServletException, IOException {

        double amount = Double.parseDouble(request.getParameter("amount"));
        double centralGST = amount * 0.09; // 9% CGST

        // Get StateGST from another context
        ServletContext stateContext = getServletContext()
                                        .getContext("/StateGSTApp");
        RequestDispatcher rd = stateContext
                                .getRequestDispatcher("/calculateSGST");

        request.setAttribute("cgst", centralGST);
        rd.include(request, response);

        // Calculate total
        double stateGST = (Double) request.getAttribute("sgst");
        double totalGST = centralGST + stateGST;

        response.getWriter().println("Total GST: " + totalGST);
    }
}
```

**Dynamic Servlet Registration:**
```java
@HandlesTypes({MyService.class})
public class AppInitializer implements ServletContainerInitializer {

    @Override
    public void onStartup(Set<Class<?>> classes, ServletContext ctx)
                         throws ServletException {

        // Register servlet dynamically
        ServletRegistration.Dynamic servlet =
            ctx.addServlet("dynamicServlet", new MyDynamicServlet());

        servlet.setInitParameter("config", "value");
        servlet.addMapping("/dynamic");
        servlet.setLoadOnStartup(1);

        // Register filter dynamically
        FilterRegistration.Dynamic filter =
            ctx.addFilter("myFilter", new MyFilter());
        filter.addMappingForUrlPatterns(null, false, "/*");

        System.out.println("Dynamic registration completed!");
    }
}
```

---

## 🗺️ Learning Path

### 🌱 Beginner Track (Start Here!)

**Week 1: Servlet Basics**
```
1. DatabaseApp (Basic servlet structure)
   ↓
2. DatabaseApp-AnnotationDriven (Modern annotations)
   ↓
3. DatabaseApp-ServletConfig (Configuration)
   ↓
4. DatabaseApp-ServletConext (Application context)
```

**Week 2: Request Handling**
```
1. DatabaseApp-RequestDispatcher-Forward
   ↓
2. DatabaseApp-RequestDispatcher-Include
   ↓
3. SendRedirection-SendRedirect
   ↓
4. Application-DynamicForm
```

**Week 3: Session Management**
```
1. Cookie-Application-SessionTracking
   ↓
2. SessionTracking-HttpSession & Cookies
   ↓
3. SessionTracking-HttpSession & URL Rewriting
   ↓
4. SessionTracking-Using-HiddenFormFields
```

### 🚀 Intermediate Track

**Focus Areas:**
- Servlet scopes and attributes
- Event listeners
- File operations
- Resource injection

**Recommended Projects:**
1. `ServletAtributes-RequestScope`
2. `ServletAtributes-SessionScope`
3. `ServletAtributes-ApplicationScope`
4. `SessionTracking-Listeners`
5. `FileUploadApp - JavaZoomAPI`
6. `ResourceDownloadApp`
7. `DatabaseApp-Annotations-Resource`

### 🎓 Advanced Track

**Master These:**
- Layered architecture and MVC pattern
- Cross-context communication
- Dynamic servlet registration
- Thread safety
- Performance monitoring

**Expert Projects:**
1. `LayeredApplication-EmployeeRegistration` (Complete MVC)
2. `CentralGSTApp-CrossContextCommunication`
3. `StateGSTApp-CrossContextCommunication`
4. `DynamicRegistration-ProgrammaticApproach`
5. `TestApp-ThreadSafety`
6. `DatabaseApp-ResponseDownloading`

---

## 🛠️ Tech Stack

### Core Technologies

```yaml
Java: SE 8 (JavaSE-1.8)
Servlet API: 4.0 (javax.servlet)
JDBC: Oracle JDBC Driver
Server: Apache Tomcat 9.0
```

### Database

```yaml
Oracle Database: 11g XE / 18c XE
Connection: JDBC Thin Driver
Connection URL: jdbc:oracle:thin:@localhost:1521:xe
Connection Pooling: DataSource with @Resource
```

### Development Tools

```yaml
IDE: Eclipse IDE for Java EE Developers
Build: Maven-compatible structure
Deployment: WAR (Web Application Archive)
```

### Third-Party Libraries

```yaml
JavaZoom Upload API: File upload functionality
Apache Commons IO: IOUtils for file operations
```

---

## 📂 Project Structure

### Repository Organization

```
java-servlets-all-concepts/
├── Database Operations/
│   ├── DatabaseApp/
│   ├── DatabaseApp-AnnotationDriven/
│   ├── DatabaseApp-Annotations-Resource/
│   ├── DatabaseApp-ServletConfig/
│   └── DatabaseApp-ResponseDownloading/
│
├── Request Handling/
│   ├── DatabaseApp-RequestDispatcher-Forward/
│   ├── DatabaseApp-RequestDispatcher-Include/
│   ├── SendRedirection-SendRedirect/
│   └── Application-DynamicForm/
│
├── Session Management/
│   ├── SessionTracking-HttpSession & Cookies/
│   ├── SessionTracking-HttpSession & URL Rewriting/
│   ├── Cookie-Application-SessionTracking/
│   └── SessionTracking-Using-HiddenFormFields/
│
├── File Operations/
│   ├── FileUploadApp - JavaZoomAPI/
│   └── ResourceDownloadApp/
│
├── Event Listeners/
│   └── SessionTracking-Listeners/
│
└── Advanced Patterns/
    ├── LayeredApplication-EmployeeRegistration/
    ├── CentralGSTApp-CrossContextCommunication/
    ├── StateGSTApp-CrossContextCommunication/
    └── DynamicRegistration-ProgrammaticApproach/
```

### Typical Project Structure

```
ProjectName/
├── .settings/                   # Eclipse IDE settings
│   ├── org.eclipse.jdt.core.prefs
│   └── org.eclipse.wst.common.project.facet.core.xml
│
├── build/                       # Compiled classes
│   └── classes/
│       └── com/dib/servlet/
│
├── src/                        # Source code
│   └── com/dib/
│       ├── servlet/            # Servlet classes
│       │   ├── ControllerServlet.java
│       │   └── ...
│       ├── dao/                # Data Access Objects
│       │   ├── EmployeeDAO.java
│       │   └── EmployeeDAOImpl.java
│       ├── service/            # Service layer
│       │   └── EmployeeService.java
│       ├── dto/                # Data Transfer Objects
│       │   └── EmployeeDTO.java
│       ├── vo/                 # Value Objects
│       │   └── EmployeeVO.java
│       ├── bo/                 # Business Objects
│       │   └── EmployeeBO.java
│       └── listener/           # Event Listeners
│           └── AppListener.java
│
├── WebContent/                 # Web resources
│   ├── META-INF/
│   │   └── MANIFEST.MF
│   ├── WEB-INF/
│   │   ├── web.xml            # Deployment descriptor
│   │   └── lib/               # JAR dependencies
│   ├── index.html             # Welcome page
│   ├── register.html          # Forms
│   └── css/                   # Stylesheets
│
├── .classpath                 # Eclipse classpath
└── .project                   # Eclipse project file
```

---

## ⚙️ Configuration Approaches

This repository demonstrates **3 different configuration approaches**:

### 1. XML-Based Configuration (web.xml)

**Traditional approach using deployment descriptor**

```xml
<?xml version="1.0" encoding="UTF-8"?>
<web-app xmlns="http://xmlns.jcp.org/xml/ns/javaee"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://xmlns.jcp.org/xml/ns/javaee
         http://xmlns.jcp.org/xml/ns/javaee/web-app_4_0.xsd"
         version="4.0">

    <!-- Servlet Declaration -->
    <servlet>
        <servlet-name>EmployeeServlet</servlet-name>
        <servlet-class>com.dib.servlet.EmployeeServlet</servlet-class>
        <init-param>
            <param-name>driver</param-name>
            <param-value>oracle.jdbc.driver.OracleDriver</param-value>
        </init-param>
        <load-on-startup>1</load-on-startup>
    </servlet>

    <!-- Servlet Mapping -->
    <servlet-mapping>
        <servlet-name>EmployeeServlet</servlet-name>
        <url-pattern>/employees</url-pattern>
    </servlet-mapping>

    <!-- Context Parameters -->
    <context-param>
        <param-name>dbURL</param-name>
        <param-value>jdbc:oracle:thin:@localhost:1521:xe</param-value>
    </context-param>

    <!-- Session Timeout (in minutes) -->
    <session-config>
        <session-timeout>30</session-timeout>
    </session-config>

    <!-- Welcome Files -->
    <welcome-file-list>
        <welcome-file>index.html</welcome-file>
    </welcome-file-list>
</web-app>
```

**Pros:**
- Externalized configuration
- No recompilation needed
- Industry standard

**Cons:**
- Verbose
- Type-safety issues
- More files to manage

---

### 2. Annotation-Based Configuration (Servlet 3.0+)

**Modern approach using annotations**

```java
@WebServlet(
    name = "EmployeeServlet",
    urlPatterns = {"/employees", "/emp"},
    initParams = {
        @WebInitParam(name = "driver", value = "oracle.jdbc.driver.OracleDriver"),
        @WebInitParam(name = "url", value = "jdbc:oracle:thin:@localhost:1521:xe")
    },
    loadOnStartup = 1
)
public class EmployeeServlet extends HttpServlet {

    @Override
    public void init() throws ServletException {
        String driver = getInitParameter("driver");
        // Initialize
    }

    @Override
    protected void doGet(HttpServletRequest request,
                        HttpServletResponse response)
                        throws ServletException, IOException {
        // Handle request
    }
}
```

**Listener Annotation:**
```java
@WebListener
public class AppListener implements ServletContextListener {
    public void contextInitialized(ServletContextEvent sce) {
        // App startup
    }

    public void contextDestroyed(ServletContextEvent sce) {
        // App shutdown
    }
}
```

**Resource Injection:**
```java
@WebServlet("/employees")
public class EmployeeServlet extends HttpServlet {

    @Resource(name = "jdbc/MyDB")
    private DataSource dataSource;

    protected void doGet(HttpServletRequest request,
                        HttpServletResponse response)
                        throws ServletException, IOException {

        try(Connection con = dataSource.getConnection()) {
            // Use connection from pool
        }
    }
}
```

**Pros:**
- Less verbose
- Co-located with code
- Type-safe
- Modern standard

**Cons:**
- Requires recompilation
- Less flexible at runtime

---

### 3. Programmatic Configuration (ServletContainerInitializer)

**Dynamic registration at runtime**

```java
@HandlesTypes({MyService.class})
public class AppInitializer implements ServletContainerInitializer {

    @Override
    public void onStartup(Set<Class<?>> classes, ServletContext ctx)
                         throws ServletException {

        System.out.println("Programmatic configuration starting...");

        // Register servlet dynamically
        ServletRegistration.Dynamic employeeServlet =
            ctx.addServlet("employeeServlet", EmployeeServlet.class);
        employeeServlet.addMapping("/employees");
        employeeServlet.setInitParameter("driver", "oracle.jdbc.driver.OracleDriver");
        employeeServlet.setLoadOnStartup(1);

        // Register filter
        FilterRegistration.Dynamic authFilter =
            ctx.addFilter("authFilter", AuthFilter.class);
        authFilter.addMappingForUrlPatterns(
            EnumSet.of(DispatcherType.REQUEST), true, "/*");

        // Register listener
        ctx.addListener(AppListener.class);

        // Set context parameters
        ctx.setInitParameter("appName", "Employee Management");

        System.out.println("Dynamic registration completed!");
    }
}
```

**Pros:**
- Maximum flexibility
- Runtime decisions
- Programmatic control
- Plugin architecture

**Cons:**
- More complex
- Harder to debug
- Advanced feature

---

## 🎯 Servlet API Comparison

### Servlet Versions Evolution

| Version | Released | Key Features |
|---------|----------|--------------|
| **Servlet 2.5** | 2005 | web.xml required, minimal annotations |
| **Servlet 3.0** | 2009 | @WebServlet, @WebFilter, @WebListener, async support |
| **Servlet 3.1** | 2013 | Non-blocking I/O, HTTP upgrade |
| **Servlet 4.0** | 2017 | HTTP/2 server push, new APIs |

**This repository uses Servlet 4.0** with all modern features!

---

## 🤝 Contributing

Contributions make the open-source community an amazing place to learn and create!

### How to Contribute

1. 🍴 **Fork** the repository
2. 🌿 **Create** your feature branch (`git checkout -b feature/AmazingFeature`)
3. ✍️ **Commit** your changes (`git commit -m 'Add some AmazingFeature'`)
4. 📤 **Push** to the branch (`git push origin feature/AmazingFeature`)
5. 🔃 **Open** a Pull Request

### Contribution Ideas

- 📝 **Add JSP examples** (Model 1 vs Model 2 architecture)
- 🔒 **Add filter examples** (Authentication, logging, compression)
- 🆕 **Add async servlet** examples (Servlet 3.0+)
- 🌐 **Add WebSocket** examples (Servlet 3.1+)
- ✅ **Add unit tests** with JUnit and Mockito
- 🐛 **Fix bugs** or improve existing examples
- 📚 **Enhance documentation** with diagrams
- 🎨 **Add frontend frameworks** (Bootstrap, jQuery)
- 🔄 **Add REST API** examples
- 🐳 **Add Docker** configurations
- 📊 **Add monitoring** examples (JMX, metrics)

---

## 👨‍💻 Author

**Dibyaprakash Pradhan**

- GitHub: [@dibyapp](https://github.com/dibyapp)
- Repository: [java-servlets-all-concepts](https://github.com/dibyapp/java-servlets-all-concepts)

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

You are free to:
- ✅ Use for learning and education
- ✅ Use in personal and commercial projects
- ✅ Modify and distribute
- ✅ Create derivative works

---

## ⭐ Star History

If this repository helped you master Java Servlets, please give it a ⭐!

[![Star History Chart](https://api.star-history.com/svg?repos=dibyapp/java-servlets-all-concepts&type=Date)](https://star-history.com/#dibyapp/java-servlets-all-concepts&Date)

---

## 🙏 Acknowledgments

- **Java Community Process (JCP)** for Servlet specifications
- **Apache Software Foundation** for Tomcat servlet container
- **Oracle** for Java platform and documentation
- **Open-source community** for continuous inspiration
- **All contributors** who help improve this repository

---

## 📚 Related Resources

### Other Tutorial Repositories by the Same Author
- 🌸 [Spring Core Concepts](https://github.com/dibyapp/spring-core-all-concepts-tutorial) - Master Spring IoC and DI (64+ projects)
- 🌐 [Spring MVC Concepts](https://github.com/dibyapp/spring-mvc-all-concepts-tutorial) - Master Spring MVC (44+ projects)

### Official Documentation
- 📖 [Java Servlet Specification](https://jakarta.ee/specifications/servlet/)
- 📖 [Apache Tomcat Documentation](https://tomcat.apache.org/tomcat-9.0-doc/)
- 📖 [Oracle Java EE Tutorial](https://docs.oracle.com/javaee/7/tutorial/)
- 📖 [JDBC Documentation](https://docs.oracle.com/javase/tutorial/jdbc/)

### Recommended Books
- 📚 "Head First Servlets and JSP" by Bryan Basham
- 📚 "Professional Java for Web Applications" by Nicholas S. Williams
- 📚 "Java EE 8 Application Development" by David R. Heffelfinger

---

## 📞 Support

### Found This Helpful?

- ⭐ **Star** this repository
- 🍴 **Fork** and contribute
- 📢 **Share** with Java developers
- 🐛 **Report** bugs via issues
- 💡 **Suggest** new examples or improvements

### Need Help?

- 📖 Check existing examples for similar patterns
- 💬 Open an issue for questions
- 📧 Contact through GitHub

---

## 📊 Repository Stats

- 📁 **26+ Projects** covering every Servlet API 4.0 concept
- 🔧 **3 Configuration Styles** (XML, Annotations, Programmatic)
- 🗄️ **Database Integration** with JDBC and connection pooling
- 📝 **Session Tracking** - 4 different techniques demonstrated
- 🎧 **Event Listeners** - Application, Session, and Request lifecycle
- 🏗️ **Design Patterns** - MVC, DAO, DTO/VO, Front Controller
- 🎯 **100% Working Code** - All examples tested on Tomcat 9.0

---

## 🚀 Next Steps After Mastering Servlets

Once you've mastered servlets, progress to:

1. **JSP (JavaServer Pages)** - View layer technology
2. **JSTL & EL** - JSP Standard Tag Library and Expression Language
3. **Spring MVC** - Modern web framework ([check this repo!](https://github.com/dibyapp/spring-mvc-all-concepts-tutorial))
4. **Spring Boot** - Rapid application development
5. **REST APIs** - RESTful web services
6. **Microservices** - Distributed architecture

---

<div align="center">

### ☕ Master Java Servlets One Concept at a Time 🚀

**Build the Foundation for Modern Java Web Development**

Made with ❤️ by the Java Developer Community

[![GitHub stars](https://img.shields.io/github/stars/dibyapp/java-servlets-all-concepts?style=social)](https://github.com/dibyapp/java-servlets-all-concepts/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/dibyapp/java-servlets-all-concepts?style=social)](https://github.com/dibyapp/java-servlets-all-concepts/network/members)
[![GitHub watchers](https://img.shields.io/github/watchers/dibyapp/java-servlets-all-concepts?style=social)](https://github.com/dibyapp/java-servlets-all-concepts/watchers)

**[⬆ Back to Top](#-java-servlets---complete-concepts-tutorial)**

</div>
