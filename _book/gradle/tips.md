* You run a Gradle build using the gradle command. 
* The gradle command looks for a file called build.gradle in the current directory. 
* The runnable actions of a task are doFirst and doLast
* The "<<" operator is an alias for the "doLast" method
* In gradle, the task execution order is not deterministic. e.g you cannot guarantee that in the example below first will always be executed before second

    third.dependsOn([first, second])

* In a task, any stuff that is not within doFirst or doLast is executed in the configuration phase


How to declare dependencies
===========================

     dependencies {
        compile 'org.hibernate:hibernate-core:3.6.7.Final'
     }



How to define a repo
====================


      repositories {
          mavenCentral()
      }


Define maven remote repository
==============================

     repositories {
        maven {
           url "http://repo.mycompany.com/maven2"
        }
     }

Define an ivy remote repo
=========================

      repositories {
        ivy {
           url "http://repo.mycompany.com/repo"
        }
      }


Publishing to a maven repo
==========================

      apply plugin: 'maven'

      uploadArchives {
         repositories {
             mavenDeployer {
                 repository(url: "file://localhost/tmp/myRepo/")
             }
         }
      }



Command line
============
============

Define a System property
------------------------

 -Dproperty=value


change log level to debug or info
=================================
 
 --debug OR -d

 --info  OR -i


suppress output
---------------

* --quiet or -q


Emit all the properties of the build’s Project object
======================================================

* gradle properties 


Emit a list of all tasks available in the current build file
=============================================================

* tasks


view dependencies
=================
* gradle dependencies

init project (archetype equivalent)
===================================
* gradle init --type java-library


