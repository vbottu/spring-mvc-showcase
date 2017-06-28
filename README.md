Spring MVC Showcase
-------------------
Demonstrates the capabilities of the Spring MVC web framework through small, simple examples.
After reviewing this showcase, you should have a good understanding of what Spring MVC can do and get a feel for how easy it is to use.
Includes project code along with a supporting slideshow and screen cast.

In this showcase you'll see the following in action:

* The simplest possible @Controller
* Mapping Requests
* Obtaining Request Data
* Generating Responses
* Message Converters
* Rendering Views
* Type Conversion
* Validation
* Forms
* File Upload
* Exception Handling

To get the code:
-------------------
Clone the repository:

    $ git clone git://github.com/SpringSource/spring-mvc-showcase.git

If this is your first time using Github, review http://help.github.com to learn the basics.

To run the application:
-------------------	
From the command line with Maven:

    $ cd spring-mvc-showcase
    $ mvn tomcat7:run [-Dmaven.tomcat.port=<port no.>] (In case 8080 is busy] 

To Deploy on Tomcat using Jenkins:
----------------------------------
To deploy the war file directly to the tomcat automatically using jenkins 
        mvn tomcat7:redeploy

<p>Add the following to the pom.xml</p>
        &ltplugin&gt<br/>
             &ltgroupId&gtorg.apache.tomcat.maven&lt/groupId&gt<br/>
            &ltartifactId&gttomcat7-maven-plugin&lt/artifactId&gt<br/>
            &ltversion&gt${tomcat7-maven-plugin.version}&lt/version&gt<br/>
            &ltconfiguration&gt<br/>
                &lturl&gt<host-ip>/manager/text&lt/url&gt<br/>
                &ltserver&gttomcat&lt/server&gt<br/>
                &ltusername&gtusername&lt/username&gt<br/>
                &ltpassword&gtpassword&lt/password&gt<br/>
                &ltpath&gt/${project.artifactId}&lt/path&gt<br/>
                &ltupdate&gttrue&lt/update&gt<br/>
            &lt/configuration&gt<br/>
       &lt/plugin&gt <br/>
-------------------------------------------------------------------------------------------------------------

or

In your preferred IDE such as SpringSource Tool Suite (STS) or IDEA:

* Import spring-mvc-showcase as a Maven Project
* Drag-n-drop the project onto the "SpringSource tc Server Developer Edition" or another Servlet 2.5 or > Server to run, such as Tomcat.

Access the deployed web application at: http://localhost:8080/spring-mvc-showcase/

Note:
-------------------

This showcase originated from a [blog post](http://blog.springsource.com/2010/07/22/spring-mvc-3-showcase/) and was adapted into a SpringOne presentation called [Mastering MVC 3](http://www.infoq.com/presentations/Mastering-Spring-MVC-3).

A screen cast showing the showcase in action is [available in QuickTime format](http://s3.springsource.org/MVC/mvc-showcase-screencast.mov).
