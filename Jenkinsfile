pipeline {
  agent any
  stages {
    stage('CheckoutCode') {
      steps {
        git(url: 'https://github.com/dangol/curriculum-app', branch: 'dev')
      }
    }

    stage('list directory') {
      steps {
        sh 'ls -la'
      }
    }

  }
}
