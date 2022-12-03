pipeline {
  agent any
  stages {
    stage('CheckoutCode') {
      steps {
        git(url: 'https://github.com/dangol/curriculum-app', branch: 'dev')
      }
    }

    stage('list directory') {
      parallel {
        stage('list directory') {
          steps {
            sh 'ls -la'
          }
        }

        stage('front end unit test') {
          steps {
            sh 'cd curriculum-front && npm i && npm run test:unit'
          }
        }

      }
    }

    stage('Build') {
      steps {
        sh 'docker build -f curriculum-front/Dockerfile .'
      }
    }

  }
}