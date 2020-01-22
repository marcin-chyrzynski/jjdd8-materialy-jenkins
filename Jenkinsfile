pipeline {
  agent {
    docker {
      args '-v /root/.m2:/root/.m2'
      image 'maven:3-alpine'
    }

  }
  stages {
    stage('Alignment') {
      steps {
        sh 'mvn clean'
        sh 'mvn --projects biojava-alignment test'
      }
    }
    stage('Whatever') {
      steps {
        sh 'echo "Hello from jenkins"'
      }
  }
}
