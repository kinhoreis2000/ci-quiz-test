pipeline {
  agent any

  tools {
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
        // A MUDANÇA É AQUI!
        sh 'mvn -B -q test'
      }
    }
  }
}