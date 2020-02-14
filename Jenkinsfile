pipeline{
 agent any
 stages {
 	stage ('Build'){
 		steps {
 			
 				bat 'mvn clean install'
 		}
 	}
 	
 	stage ('Deploy'){
 		steps {
 			
 				bat 'mvn clean package deploy -Dusername=max356 -Dpassword=@@Gaga356@@ -Dcloudhub.environment=Sandbox -Dworkers=1 -Dworker.type=Micro -Dapplication.name=greeting-API -DmuleDeploy'
 			}
 		}
 	}
 }