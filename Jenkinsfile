pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/eric-gan25/maven-samples', branch: 'master')
      }
    }

    stage('test') {
      steps {
        sh 'mvn test'
      }
    }

    stage('verify') {
      steps {
        sh 'mvn verify'
      }
    }

    stage('clean') {
      steps {
        sh 'mvn clean'
      }
    }

  }
  tools {
    maven 'DHT_MVN'
    jdk 'DHT_SENSE'
  }
}