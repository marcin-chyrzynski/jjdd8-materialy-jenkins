pipeline {
  agent {
    docker {
      image 'image: maven:3-alpine'
      args '-v /root/.m2:/root/.m2'
    }

  }
  stages {
    stage('Testing') {
      steps {
        sh 'mvn clean'
        sh 'mvn --projects biojava-alignment test'
      }
    }

  }
}