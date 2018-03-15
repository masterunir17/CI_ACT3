pipeline {
agent any   
stage('Preparacion') { // for display purposes
      // Get some code from a GitHub repository
      git 'https://github.com/masterunir17/CI_ACT3.git'
   }
stage('Compilar') { // Genera los ficheros .class con los fuentes .java
        sh 'mvn compile'
     }
stage('Test') { // Ejecuta los comandos de JUnt - Pruebas unitarias
        sh 'mvn test'
     
    }
stage('Empaquetado') { // Crear el .Jar validado
        sh 'mvn package'
     
    }
}

