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
				sh 'mvn compile'
			     	
				}			
			}
		stage('Test') { // Ejecuta los comandos de JUnt - Pruebas unitarias
			steps {
				sh 'mvn test'
			}		     
		    }
		stage('Empaquetado') { // Crear el .Jar validado
			steps {
				sh 'mvn package'
			}		     
		    }
		stage('Instalacion') { // Crear el .Jar validado
			steps {
				sh 'mvn clean install'
			}		     

		}

	}
}
