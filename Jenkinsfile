pipeline {
  agent {
        docker {
            image 'node:6-alpine' 
            args '-p 3000:3000' 
        }
    }
  stages {
    stage('Checkout') {
      steps {
        echo 'checkout'
        git(url: 'https://github.com/angel-moveapps/dummy-proyect.git', branch: 'master', credentialsId: 'github')
      }
    }

    stage('Listing workspace') {
      steps {
        sh 'ls'
      }
    }

    stage('Build') {
      steps {
        sh '''cd my-app
npm build'''
      }
    }

  }
}