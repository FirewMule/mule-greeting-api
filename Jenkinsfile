pipeline{
 agent any

 stages {
 	stage ('Build'){
 		steps {
 			withMaven(maven:'maven'){
 				sh 'mvn -f mule-maven-ci-cd-demoFlow/pom.xml clean install'
 			}
 		}
 	}
 	stage ('Deploy'){
 		steps {
 			withMaven(maven:'maven'){
 				sh 'mvn -f mule-maven-ci-cd-demoFlow/pom.xml clean package deploy -Dusername=max356 -Dpassword=@@Gaga356@@ -Dcloudhub.environment=Sandbox -Dworkers=1 -Dworker.type=Micro -Dapplication.name=greeting-API -DmuleDeploy'
 			}
 		}
 	}
 }

}