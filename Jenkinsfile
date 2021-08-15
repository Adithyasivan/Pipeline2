pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        withMaven(jdk: 'jdk11', maven: 'maven3') {
          sh 'mvn compile'
        }

      }
    }

    stage('') {
      steps {
        withMaven(jdk: 'jdk11', maven: 'maven3') {
          sh 'mvn test'
        }

      }
    }

  }
  environment {
    AUTHOR = 'Adithya'
  }
}