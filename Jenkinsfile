pipeline {
  agent any
  tools { 
    maven 'DHT_MVN' 
    jdk 'DHT_SENSE' 
  }
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/eric-gan25/maven-samples', branch: 'master')
      }
    }

    stage('run') {
      steps {
        sh 'mvn verify'
      }
    }

  }
}
