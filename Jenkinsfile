pipeline {
	agent any   
	stages {
		stage('Preparacion') { // for display purposes
		      // Get some code from a GitHub repository
		      steps {
				git 'https://github.com/masterunir17/CI_ACT3.git'
			}		
		   }
		stage('Compilar') { // Genera los ficheros .class con los fuentes .java
			steps {
				sh '/usr/local/src/apache-maven-3.5.2/bin/mvn compile'
			     	
				}			
			}
		stage('Test') { // Ejecuta los comandos de JUnt - Pruebas unitarias
			steps {
				sh '/usr/local/src/apache-maven-3.5.2/bin/mvn test'
			}		     
		    }
		stage('Empaquetado') { // Crear el .Jar validado
			steps {
				sh '/usr/local/src/apache-maven-3.5.2/bin/mvn package'
			}		     
		    }
		
	}
}
