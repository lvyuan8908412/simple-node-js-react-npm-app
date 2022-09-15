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
npm install'''
      }
    }

    stage('Cucumber Tests') {
      steps {
        sh 'npm run acceptance:tests'
      }
    }

  }
}