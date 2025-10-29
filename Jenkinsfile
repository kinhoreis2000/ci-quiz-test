pipeline {
  agent any

  tools {
    // Verifique se o nome 'Maven 3.9.9' bate com o nome
    // configurado no seu Jenkins em "Global Tool Configuration"
    maven 'Maven 3.9.9'
  }

  options { timestamps() }

  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }

    stage('Test') {
      steps {
        // Usa 'bat' para comandos do Windows
        bat 'mvn -B -q test'
      }
    }
  }
}