pipeline {
  agent {
    docker {
      image 'node:10-alpine'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh '''node --version
'''
      }
    }

    stage('Cucumber Tests') {
      steps {
        sh './jenkins/scripts/test.sh'
      }
    }

  }
}