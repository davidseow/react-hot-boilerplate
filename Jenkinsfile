pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''export PATH=PATH:/usr/local/bin

npm i'''
      }
    }
    stage('Lint') {
      parallel {
        stage('Lint') {
          steps {
            sh 'npm run lint'
          }
        }
        stage('Unit Test') {
          steps {
            echo 'Unit Test'
          }
        }
      }
    }
    stage('Functional tests') {
      parallel {
        stage('Q > GB - Specific') {
          steps {
            echo 'F'
          }
        }
        stage('Go > Shared - A') {
          steps {
            echo 'F'
          }
        }
        stage('Go > Shared - B') {
          steps {
            echo '1'
          }
        }
        stage('Go > GB - Specific') {
          steps {
            echo '2'
          }
        }
        stage('Go > Italy') {
          steps {
            echo '3'
          }
        }
        stage('Go > Germany') {
          steps {
            echo '3'
          }
        }
      }
    }
  }
}