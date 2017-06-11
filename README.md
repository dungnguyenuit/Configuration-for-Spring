# Configuration-for-Spring
A. Let’s Setup Environment
  1. Tomcat 8.0.37 – Download latest Apache Tomcat from this link.
  https://tomcat.apache.org/download-80.cgi and then extract file

  2. Make sure you download Eclipse IDE for Java EE Developers (Neon v4.6) – Download link.
  http://www.eclipse.org/downloads/packages/eclipse-ide-java-ee-developers/marsr

  3. Spring 4.3.7 (No download required) – we will use Maven dependency

  4. JDK 1.8 – Download link.
  https://docs.oracle.com/cd/E19182-01/820-7851/inst_cli_jdk_javahome_t/

B. Step by step with demo Hello SpringMVC:
  Step 1: Open Eclipse and create a Dynamic Web Project.
  Step 2: Convert this project to Maven project
  Step 3: Open pom.xml file and add below jar dependencies to projec
  Step 4: Create new Spring Configuration Bean file: /WebContent/WEB-INF/spring-servlet.xml
  Step 5: Config file web.xml
  Step 6; Create file hello.jsp
  Step 7: Create package and add new class Controller
  Step 8: Setup Tomcat and run project

C. Description:
- The code in web.xml will map DispatcherServlet with url pattern

- The code in spring-servlet.xml configuration file:
  + we have defined a tag <context:component-scan> in bean configuration file, it means, enable auto scanning feature in Spring.
  The base-package is indicate where are your components stored, Spring will scan this folder and find out the bean
  + This will allow Spring to load all the components from package com.spring controller and all its child packages
  + This bean will resolve the view and add prefix string /WEB-INF/jsp/  and suffix .jsp to the view in ModelAndView
  + <mvc:annotation-driven /> declares explicit support for annotation-driven MVC controllers (i.e. @RequestMapping, @Controller, although support for those is the default behaviour)
  + <mvc:default-servlet-handler /> The DefaultServletHttpRequestHandler will attempt to auto-detect the default Servlet for the container at startup time
