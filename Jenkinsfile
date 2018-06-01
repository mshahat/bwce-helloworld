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
    stage('list-repo') {
      agent {
        docker {
          image 'jenkins-agent-mvn:0.1'
        }

      }
      steps {
        sh 'find .'
      }
    }
    stage('mvn-package') {
      agent {
        docker {
          image 'jenkins-agent-mvn:0.1'
        }

      }
      steps {
        sh 'mvn package'
      }
    }
  }
}