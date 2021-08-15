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

    stage('Unit Test') {
      steps {
        withMaven(jdk: 'jdk11', maven: 'maven3') {
          sh 'mvn test'
        }

      }
    }

    stage('Publish test result') {
      steps {
        withMaven(jdk: 'jdk11', maven: 'maven3') {
          junit 'target/**/*.xml'
        }

      }
    }

  }
  environment {
    AUTHOR = 'Adithya'
  }
}