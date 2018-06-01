pipeline {
  agent none
  stages {
    stage('validate-mvn') {
      agent {
        docker {
          image 'jenkins-agent-mvn:0.1'
        }

      }
      steps {
        echo 'init pipeline'
        sh 'mvn --version'
      }
    }
  }
}