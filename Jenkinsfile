pipeline {
  agent any
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

  }
}