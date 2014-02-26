AST-Parent-Pom
==============
The *A*lessandro *ST*aniscia MAVEN *parent pom*  used for all software made by me. I work as [Software Specialist](http://www.staniscia.net/work-experience/), but software, technology are also my preferred hobbies. So, often I act as *garage-developer* and I have fun in producing code.

|Line        |Build Status|Version|
|------------|------------|------------|
|Master      |[![Build Status](https://travis-ci.org/Odyno/AST-Parent-Pom.png?branch=master)](https://travis-ci.org/Odyno/AST-Parent-Pom)|1.0.3|
|Develop     |[![Build Status](https://travis-ci.org/Odyno/AST-Parent-Pom.png?branch=developer)](https://travis-ci.org/Odyno/AST-Parent-Pom)|1.0.4-SNAPSHOT|


My public maven repository
--------------------------
You can download the compiled artifacts with the link on owned page or with the link into the downloads page. For the maven nature project you can add my repository in your info
```
setting.xml
```
with this simple code (more info on my article [Creare un repository Maven con server ftp e http ](http://www.staniscia.net/807-creare-un-repository-maven-con-server-ftp-e-http/))


```xml
<?xml version="1.0" encoding="UTF-8"?>
<settings >
...
  <profiles>
   ...
   <profile>
     <id>staniscia-repository</id>
     <repositories>
       <!-- STABLE ARTIFACTs -->
       <repository>
         <id>release-staniscia-rep</id>
         <name>Staniscia Software Release Repository</name>
         <url>http://www.staniscia.net/repository/release</url>
         <releases>
           <enabled>true</enabled>
         </releases>
       </repository>
       <!-- DEVELOP ARTIFACTs -->
       <repository>
         <id>snapshot-staniscia-rep</id>
         <name>Staniscia Software Snapshot Repository</name>
         <url>http://www.staniscia.net/repository/snapshot</url>
         <releases>
            <enabled>false</enabled>
         </releases>
         <snapshots>
            <enabled>true</enabled>
         </snapshots>
        </repository>
      </repositories>
   </profile>
   ...
</profiles>
<activeProfiles>
   ...
   <activeProfile>staniscia-repository</activeProfile>
   ...
</activeProfiles>
...
</settings>
```
