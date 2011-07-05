1. Create your repo by forking from jinnbaba/eligybility repo.

2. There are three eclipse projects in this repository. Please import them all into your eclipse. One project is server side business and second project is web. Third is parent of these two.

3. Make sure you have correct environment variables set. Please refer to setenv.sh to see what needs to be set.

4. Build the application with mvn -Dmaven.test.skip=true clean install from the eligybility-parent project

5. Step above should create eligybility-web.war in eligybility-web/target folder

6. Before you can deploy this war, copy JDBC driver jar into the lib folder of tomcat. Project by default uses HSQLDB. Go to your local maven repository and then within that go to hsqldb/hsqldb/1.8.0.1/ and copy hsqldb-1.8.0.1.jar to the lib directory of your tomcat installation.

7. Drop this war into the webapps directory of apache tomcat. I have tested this with jdk 1.6 and tomcat 6.0.32

8. Go to http://localhost:8080/eligybility-web/ and mouse over 'Planet' link on the left top. This should popup a menu where you can do some CRUD operations.