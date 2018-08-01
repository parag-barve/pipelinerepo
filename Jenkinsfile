pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git 'https://github.com/parag-barve/pipelinerepo.git'
      }
    }
    stage('Unit Test') {
      parallel {
        stage('Unit Test') {
          steps {
            sh 'echo unit tests running...'
          }
        }
        stage('Functional Test') {
          steps {
            sh 'echo functional testing...'
          }
        }
      }
    }
    stage('System Test') {
      steps {
        sh 'echo system testing in progress...'
      }
    }
    stage('Deploy to QA') {
      steps {
        sh 'echo deploying to QA...'
      }
    }
  }
}