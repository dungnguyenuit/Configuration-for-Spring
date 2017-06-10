# Configuration-for-Spring
- The code in web.xml will map DispatcherServlet with url pattern

- The code in spring-servlet.xml configuration file:
  + we have defined a tag <context:component-scan> in bean configuration file, it means, enable auto scanning feature in Spring.
  The base-package is indicate where are your components stored, Spring will scan this folder and find out the bean
  + This will allow Spring to load all the components from package com.spring controller and all its child packages
  + This bean will resolve the view and add prefix string /WEB-INF/jsp/  and suffix .jsp to the view in ModelAndView
  + <mvc:annotation-driven /> declares explicit support for annotation-driven MVC controllers (i.e. @RequestMapping, @Controller, although support for those is the default behaviour)
  + <mvc:default-servlet-handler /> The DefaultServletHttpRequestHandler will attempt to auto-detect the default Servlet for the container at startup time
