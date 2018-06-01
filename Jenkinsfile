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
        sh 'ls -ln'
      }
    }
    stage('mvn-package') {
      agent {
        docker {
          image 'jenkins-agent-mvn:0.1'
        }

      }
      steps {
        dir(path: 'bwce_ws3/helloworld.application.parent') {
          sh '''pwd
ls -ln'''
          sh 'mvn package'
        }

      }
    }
  }
}