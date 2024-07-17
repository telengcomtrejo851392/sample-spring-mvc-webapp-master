# sample-spring-mvc-webapp
sample project using spring framework with maven

Steps to create this project in eclipse

1. File->New->Maven Project
2. Choose "Create a simple project (skip archetype selection)"
3. Choose packaging as "war" (this will create both webapp and java folders)
4. Create the project after specifying group id and artifact id
5. Update pom.xml with java and compiler versions, then right click on project, select Maven->Update project
6. If the project is not faceted form (Its not in faceted form if on expanding project in Project explorer, it doesn't show details such as "Deployment Descriptor" and "JAX-WS Web Services", this happened in one of my eclipse installation and i had no clue why), then do the following steps  
    1. right click on project, go to Properties, click on Project Facets, convert to faceted form, choose correct "Dynamic Web Module" version, enable the checkbox and also choose correct Java Facet version. Click on the project in "Project Explorer" and refresh(hit F5).
    2. "Further configuration available" gets displayed in that window, click on it and specify WebContent folder. (replace WebContent by src/main/webapp)  
    3. If you want to run the application in servers configured in eclipse, then specify maven dependencies to be deployed in "Deployment Assembly". If "Deployment Assembly" menu is not present in project properties then add "Web properties" project nature. This will deploy maven "provided" dependencies also, but i think its fine for testing. For actual distribution, you can supply war file generated from maven package.  
