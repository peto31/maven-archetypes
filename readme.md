# Maven archetypes for spring project mvc
This is sample project for Maven Archetype: Spring Project MVC Template

## Setup

Clone:
	
	git clone https://github.com/peto31/maven-achetypes.git
	cd maven-achetypes

Build and install archetype into local repo:
	
	mvn clean install
	
You will get:	
	
	$ mvn clean install
	[INFO] Scanning for projects...
	[INFO] ------------------------------------------------------------------------
	[INFO] Reactor Build Order:
	[INFO]
	[INFO] Maven Archetype for Spring MVC Project Template
	[INFO] Maven Archetype
	[INFO]
	[INFO] ------------------------------------------------------------------------
	[INFO] Building Maven Archetype for Spring MVC Project Template 1.1-SNAPSHOT
	[INFO] ------------------------------------------------------------------------
	[INFO]
	[INFO] --- maven-clean-plugin:2.4.1:clean (default-clean) @ mvc ---
	[INFO] Deleting C:\...
	[INFO]
	[INFO] --- maven-resources-plugin:2.6:resources (default-resources) @ mvc ---
	[INFO] Using 'UTF-8' encoding to copy filtered resources.
	[INFO] Copying 5 resources
	[INFO]
	[INFO] --- maven-resources-plugin:2.6:testResources (default-testResources) @ mvc ---
	[INFO] Using 'UTF-8' encoding to copy filtered resources.
	[INFO] skip non existing resourceDirectory C:\...
	[INFO]
	[INFO] --- maven-archetype-plugin:2.0:jar (default-jar) @ mvc ---
	[INFO]
	[INFO] --- maven-archetype-plugin:2.0:add-archetype-metadata (default-add-archetype-metadata) @ mvc ---
	[INFO]
	[INFO] --- maven-archetype-plugin:2.0:integration-test (default-integration-test) @ mvc ---
	[INFO]
	[INFO] --- maven-install-plugin:2.4:install (default-install) @ mvc ---
	[INFO] Installing C:\...\mvc-1.1-SNAPSHOT.jar
	[INFO] Installing C:\...\mvc-1.1-SNAPSHOT.pom
	[INFO]
	[INFO] --- maven-archetype-plugin:2.0:update-local-catalog (default-update-local-catalog) @ mvc ---
	[INFO]
	[INFO] ------------------------------------------------------------------------
	[INFO] Building Maven Archetype 1.1-SNAPSHOT
	[INFO] ------------------------------------------------------------------------
	[INFO]
	[INFO] --- maven-clean-plugin:2.4.1:clean (default-clean) @ mvc-top ---
	[INFO]
	[INFO] --- maven-install-plugin:2.3.1:install (default-install) @ mvc-top ---
	[INFO] Installing c:\...\mvc-top-1.1-SNAPSHOT.pom
	[INFO] ------------------------------------------------------------------------
	[INFO] Reactor Summary:
	[INFO]
	[INFO] Maven Archetype for Spring MVC Project Template ... SUCCESS [...]
	[INFO] Maven Archetype ................................... SUCCESS [...]
	[INFO] ------------------------------------------------------------------------
	[INFO] BUILD SUCCESS
	[INFO] ------------------------------------------------------------------------
	[INFO] Total time: ...
	[INFO] Finished at: ...
	[INFO] Final Memory: ...
	[INFO] ------------------------------------------------------------------------

## Usage

	$ mvn archetype:generate -DgroupId=maven.archetypes -DartifactId=mvc -Dversion=1.1-SNAPSHOT -DarchetypeCatalog=local -Dpackage=com.company

You can parametrize the following:
	
	-Dpackage as name(path) of your packaging (eg. com.company)

You will get:

	[INFO] Scanning for projects...
	[INFO] ------------------------------------------------------------------------
	[INFO] Reactor Build Order:
	[INFO]
	[INFO] Maven Archetype for Spring MVC Project Template
	[INFO] Maven Archetype
	[INFO]
	[INFO] ------------------------------------------------------------------------
	[INFO] Building Maven Archetype 1.1-SNAPSHOT
	[INFO] ------------------------------------------------------------------------
	[INFO]
	[INFO] >>> maven-archetype-plugin:2.2:generate (default-cli) @ mvc-top >>>
	[INFO]
	[INFO] <<< maven-archetype-plugin:2.2:generate (default-cli) @ mvc-top <<<
	[INFO]
	[INFO] --- maven-archetype-plugin:2.2:generate (default-cli) @ mvc-top ---
	[INFO] Generating project in Interactive mode
	[INFO] No archetype defined. Using maven-archetype-quickstart (org.apache.maven.archetypes:maven-archetype-quickstart:1.0)
	Choose archetype:
	1: local -> maven.archetypes:mvc (Maven Archetype for Spring MVC Project Template)
	Choose a number or apply filter (format: [groupId:]artifactId, case sensitive contains): :

Choose archetype -> choose a number:

	1

You will get:

	Choose archetype:
	1: local -> maven.archetypes:mvc (Maven Archetype for Spring MVC Project Template)
	Choose a number or apply filter (format: [groupId:]artifactId, case sensitive contains): : 1
	Downloading: http://.../maven-metadata.xml
	[INFO] Using property: groupId = maven.archetypes
	[INFO] Using property: artifactId = mvc
	[INFO] Using property: version = 1.1-SNAPSHOT
	[INFO] Using property: package = com.company
	Confirm properties configuration:
	groupId: maven.archetypes
	artifactId: mvc
	version: 1.1-SNAPSHOT
	package: com.company
	 Y: :

Confirm properties configuration with:
	
	y

You will get:

 	Y: : y
	[INFO] ----------------------------------------------------------------------------
	[INFO] Using following parameters for creating project from Archetype: mvc:1.1-SNAPSHOT
	[INFO] ----------------------------------------------------------------------------
	[INFO] Parameter: groupId, Value: maven.archetypes
	[INFO] Parameter: artifactId, Value: mvc
	[INFO] Parameter: version, Value: 1.1-SNAPSHOT
	[INFO] Parameter: package, Value: com.company
	[INFO] Parameter: packageInPathFormat, Value: com/company
	[INFO] Parameter: package, Value: com.company
	[INFO] Parameter: version, Value: 1.1-SNAPSHOT
	[INFO] Parameter: groupId, Value: maven.archetypes
	[INFO] Parameter: artifactId, Value: mvc
	[INFO] Parent element not overwritten in c:\...\pom.xml
	[INFO] project created from Archetype in dir: c:\...\maven-archetypes\mvc
	[INFO] ------------------------------------------------------------------------
	[INFO] Reactor Summary:
	[INFO]
	[INFO] Maven Archetype for Spring MVC Project Template ... SKIPPED
	[INFO] Maven Archetype ................................... SUCCESS [...]
	[INFO] ------------------------------------------------------------------------
	[INFO] BUILD SUCCESS
	[INFO] ------------------------------------------------------------------------
	[INFO] Total time: ...
	[INFO] Finished at: ...
	[INFO] Final Memory: ...
	[INFO] ------------------------------------------------------------------------
		
Results with:
	
	.
	|____pom.xml
	|____src
	| |____main
	| | |____resources
	| | | |____archetype-resources
	| | | | |____pom.xml
	| | | | |____src
	| | | | | |____main
	| | | | | | |____java
	| | | | | | | |____HomeController.java
	| | | | | | |____resources
	| | | | | | | |____META-INF
	| | | | | | | | |____spring
	| | | | | | | | | |____app-context.xml
	| | | | | |____test
	| | | | | | |____java
	| | | | | | |____resources
	| | | | | | | |____log4j.xml
	| | | |____META-INF
	| | | | |____maven
	| | | | | |____archetype-metadata.xml

Basically it is the same as structure created by STS Wizard (Version: 3.2.0.)

##Import to eclipse:

	To import project build by mvn eclipse:eclipse correctly to STS you have to delete all classpath entries which has kind attribute with value set as var. 

	

	